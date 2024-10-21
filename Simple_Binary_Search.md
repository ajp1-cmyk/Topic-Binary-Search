## Binary Search

// template to use

int binary_search(vector<int> &a, int query){
  int left = 0;
  int right = a.size()-1;

  while(left < right){
    int mid = left + (right-left)/2;
    if(a[mid] < query){
        left = mid+1;
      }else{
      
      }
  }
}



## stack question

#include<bits/stdc++.h>

using namespace std;

int main(){
    string exp;
    stack<char> buffer;
    stack<char> op;
    vector<char> PRN;
    cin >> exp;
    for(char ch: exp){
        if(ch == ')'){
            PRN.push_back(op.top());
            op.pop();
            while(buffer.top()!= '('){
                PRN.push_back(buffer.top());
                buffer.pop();
            }
            buffer.pop();
        }else if(ch == '+' || ch == '-' || ch == '*' || ch == '/' || ch == '^'){
            op.push(ch);
        }else{
            buffer.push(ch);
        }
    }
    
    for(int i = PRN.size()-1; i>=0; i--){
        cout<<PRN[i];
    }
}
