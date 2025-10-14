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
