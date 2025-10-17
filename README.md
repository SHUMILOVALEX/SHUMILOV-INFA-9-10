Task 9.1
#include<iostream>
#include<vector>
#include<ctime>
#include<algorithm>
using namespace std;
int main(){
    srand(time(0));
    int start = 1;
    int end = 9;
    int sizez;
    cout<<"Input size of range "<< endl;;
    cin>>sizez;
    vector<int> baza(sizez);
    vector<int> baza2; 
    cout<<"vector before sort ";
    for (int i = 0; i!=sizez; i++){
        int x = rand() % (end - start + 1) + start;
        baza[i]=x;
        cout<<baza[i];
    }
    sort(baza.begin(),baza.end());
    cout<<"\n "<<"vector after sort ";
    for (int i = 0; i!=sizez;i++){
            if (baza[i]!=baza[i+1]){
            baza2.push_back(baza[i]);
                
}
            
  }
    for (int j : baza2){
        cout<<j;
    }
}
Task 9.2

#include <cstring>
#include<iostream>
#include<cctype>
using namespace std;
bool str(string a, string b){
    for (size_t i = 0; i!=a.size(); i++ ) { 
        a[i] = tolower(a[i]);
    }
    for (size_t i = 0; i!=b.size(); i++ ) { 
        b[i] = tolower(b[i]);
    }
    if (a.size() == b.size()){
    for (size_t i = 0; i != a.size(); i++) {
        if (a[i] == b[i]){
             return true;
        }
        else{
            return false;
        }
    }
    }
}

int main(){
    string row,roW;
    cout<<"input row"<<endl;
    cin>> row ;
    string row1 = row;
    cout<<"input row2"<<endl;
    cin>> roW;
    bool c = str(row,roW);
    if (c==0){
        cout<<"False";
    }
    else{
        cout<<"True";
    }
}

Task 9.3
#include<iostream>
using namespace std;
int vozved(int a, int n){
    if (n == 0){
        return 1;
    }
    else{
        int c = a;
    for (int i = 1; i != n ; ++i){
        c *= a;
    }
    return c;
}
    
}


int main(){
    int num,num1;
    cout<<"first num "<<endl;
    cin>>num;
    cout<<"second num "<<endl;
    cin>>num1;
    cout<<vozved(num,num1);
}
Task 9.4
#include<iostream>
#include<string>
using namespace std;
int stroka(string str){
    int k;
    for (char i : str){
        k++;
    }
    return k;
    
}

int main(){
    string a;
    getline(cin,a);
    int b = stroka(a);
cout<<"\n"<<"volume of num = "<<b;
    
}

Task 9.5
#include<iostream>
#include<cmath>
using namespace std;
bool del(int n){
    if (n<2){
        return false;
    }
        for (size_t i = 2; i!=sqrt(n);i++){
            if (n % i == 0){
                return false;
            }
            else{
                return true;
            }
        }
    }

int main(){
    int N;
    cout<<"input N";
    cin>>N;
    cout<<"simple num";
    for (size_t i = 1; i <= N;i++){
        int num = i;
        if (del(num) == true){
            cout<<i<<" ";
            
}
}
}
