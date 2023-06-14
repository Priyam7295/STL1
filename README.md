
#include <bits/stdc++.h>
using namespace std;

struct contain{
    string str;
    int num;
    double doub;
    char x;

    contain(string str_,int num_, double doub_, char x_){
        str=str_;
        num=num_;
        x=x_;
        doub=doub_;
    }


};

int arr[2];
//If you define an array globally then all garbage values are preset as 0.
// but if you define locally(say in int main) then there any garbage value will be stored

int main()
{
    //Create a data type to store int, double, char,string
    // 1 way to do is to make a class/structure
    contain pri("priyam",79,56.66,'p'); //pri is an instance of contain struct
    cout<<pri.str<<endl;

    int o=90;
    int* p = &o;
    cout<<p<<endl;
    cout<<*p<<endl;

    // right part is the  adress of o where 90 is stored



    contain* anotherone = new contain("Didi",98,98.98,'S');
    // new is giving a new instance of that struc named contain
    // 1. New operator is used to allocate a new memory for an object type of "contain". It returns a pointer to the allocated memory
    // 2.The adress of the allocated memory is asssigned to the pointer variable anotherone. The anotherone ppinter now points to the dynamically allocated "contain " ibject on the heap.
    cout<<anotherone->str;
    


cout<<endl;
    int arrayi[8];
    array<int,5>hj;
    hj.fill(8);
    
    for (int i = 0; i < 5; i++)
    {
        cout<<hj.at(i)<<" ";
    }


    /*--------------Iterators--------------*/
    // begin(),end(),rbegin(),rend().
    // begin()---- always points to the first element of array.
    //rbegin() --- points to the last .
    //end()--- right after the end, always points to the adress right after the last element of array.
    //rend()--- points to right before the first element. 

    array<int,5>my={1,3,4,5,6};
    cout<<endl;
    
    for (auto it= my.begin() ; it!= my.end() ; it++)
    {
        cout<<*it<<" ";
    }
    cout<<endl;
    for (auto it= my.rbegin() ; it>= my.rend() ; it++)
    {
        cout<<*it<<" ";
    }
    cout<<endl;
    for (auto it= my.end()-1 ; it>=my.begin() ; it--)
    {
        cout<<*it<<" ";
    }

    /*For each loop*/
    // Ex1
    cout<<endl;
    cout<<endl;
    cout<<"For each Loop"<<endl;
    int l[5]={3,4,5,2,3};
    for (auto i:l)
    {
        cout<<i<<" ";
    }

    //Ex2

    string s="Priyam";
    cout<<endl;
    //Maximum size of array is 10^6, but if declared globally then max size is 10^7.
    // If the data type is bool then max size is 10^7 and if declared globally max size is 10^8.  
    for (auto i:s)
    {
        cout<<i<<" ";
    }



    /*                           */
    /* ---------Vector---------- */
    /*                           */
    
    vector<int>v1;//Empty vector v1
    v1.push_back(3);//{3}
    v1.push_back(2); //{3,2}
    cout<<endl;
    // It dynamically increases size
    cout<<v1.size()<<endl;//2
    v1.pop_back();
    cout<<v1.size()<<endl;//1

    v1.push_back(34);
    v1.push_back(244);
    v1.push_back(12);
    v1.emplace_back(13);
    //Embace back is exactly same as push_back(),
    // But it takes slightly lesser time 

    //Printing the vectors
    cout<<"Printing Vectors:"<<endl;
    for (auto i = v1.begin(); i!= v1.end() ; i++)
    {
        cout<<*i<<" ";
    }
    //Size rule is same as that of array.
    
    // vector.clear()---Erases all elements and becomes empty\

    vector<int>myvector(4,0);//Here we have made a vector of size 4 with all its element as 0

    vector<int>v2(4);

    //We initialised the size of vector as 4,however we can keep increasing further also(obv unlike array)
    cout<<endl;
    cout<<v2.size()<<endl;

    // Copying the entire v1 into v3 and v4
    vector<int>v3(v1.begin(),v1.end());
    vector<int>v4(v1);
    
    // copying the first two elements of v1 into v5
    vector<int>v5(v1.begin(),v1.begin()+2);
    
    // swap(v1,v2)
    // begin(),end(),rbegin(),rend()-- applicable

    cout<<endl;
    cout<<endl;

    // 2D- vectors
    vector<vector<int>>vv1;
    vv1.resize(2);

    // instead we may define as
    vector<vector<int>>vecvec(2,vector<int>());
    vv1[0].push_back(2);
    vv1[0].push_back(23);
    vv1[0].push_back(22);
    vv1[1].push_back(89);
    vv1[1].push_back(9);

    //2d vectors another way
    vector<int>c1;
    c1.push_back(8);
    c1.push_back(88);
    c1.push_back(98);
    vector<int>c2;
    c2.push_back(2);
    c2.push_back(28);
    c2.push_back(3);
    
    vector<vector<int>>vv2;
    vv2.push_back(c1);
    vv2.push_back(c2);
    
    // Printing m1(traditional)
    for (int i = 0; i < vv1.size(); i++)
    {
        for (int j = 0; j < vv1[i].size() ; j++)
        {
            cout<<vv1[i][j]<<" ";
        }
        cout<<endl;   
    }
    
    // Printing m2
    for (auto i :vv1)
    {
        for (auto j :i)
        {
            cout<<j<<" ";
        }
        cout<<endl;
    }
    for (auto i :vv2)
    {
        for (auto j :i)
        {
            cout<<j<<" ";
        }
        cout<<endl;
    }


    //Define 10 x 20
    vector<vector<int>>vv4(10,vector<int>(20,0));

    //Defining an array of size 4 with all 4 elements as empty vector(as of now)
    vector<int>arr[4];
    
    // 3D VECTORS
    //  10 x 20 x 30 int arr[10][20][30]
    vector<vector<vector<int>>>vecvecvec(10,vector<vector<int>>(20,vector<int>(30,0)));

    


    
    
    

    return 0;
}
