#include <iostream>
#include <vector>
using namespace std;

class Stack {
private:
    vector<int> stack;

public:
    void push(int data) {
        stack.push_back(data);
    }
    void pop() {
        if (!isEmpty()) {
            stack.pop_back();
        } else {
            cout << "Stack is empty! Cannot pop." << endl;
        }
    }

    int top() {
        if (!isEmpty()) {
            return stack.back();
        } else {
            cout << "Stack is empty!" << endl;
            return -1; 
        }
    }

    bool isEmpty() {
        return stack.empty();
    }
    int size() {
        return stack.size();
    }
};
int main() {
    Stack s;
    s.push(10);
    s.push(20);
    s.push(30);
    cout << "Top element: " << s.top() << endl; 
    s.pop();
    cout << "Top element after pop: " << s.top() << endl;
    return 0;
}
