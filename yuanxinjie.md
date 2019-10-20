## 2.23

不可以，指针不知道是否有效

## 2.24

因为lp的类型不是int,而void定义了一个空指针，可以接受任何类型的对象

## 2.25

（a)ip是一个int类指针型的，i是一个int型的变量，r是一个int型的引用

（b）i是一个int型的变量，ip是一个空指针。

（c）ip是一个int类型的指针，ip2是一个int类型的变量。

## 2.35

第一个auto  j  类型为int

第二个auto  &k 类型为const int &

第三个auto *p类型为const int *

第四个auto j2类型为const int

第五个auto &k2 类型为const int&

## 3.20

``` cpp

#include<iostream>

#include<string>

#include<vector>

using namespace std;

void main()

{

vector<int>My_vector;

int a[10];

for(int i=0;i<10;i++)

{

cin>>a[i];

}

for(int j=0;j<10;j++)

{

My_vector.push_back(a[j]);

}

int sum[10];

for(int k=0;k<10;k++)

{

sum[k]=My_vector[k]+My_vector[k+1];

cout<<sum[k]<<endl;

k++;

}

}

```

## 3.23

``` cpp

#include<iostream>

#include<string>

#include<vector>

using namespace std;

void main()

{

void<int>text(10,5);

for(auto it=text.begin();it!=text.end();it++)

{

*it=*it*2;

cout<<*it<<endl;

}

}

```

## 3.4

## 字符串比较：

```cpp

#include<iostream>

#include<string>

using namespace std;

void main()

{

string mystring1,mystring2;

cin>>mystring1>>mystring2;

if(mystring1!=mystring2)

{

cout<<(mystring1>=mystring2?mystring1:mystring2)<<endl;

}

}

```

## 字符串长度比较:

```cpp

#include<iostream>

#include<string>

using namespace std;

void main()

{

string mystring1,mystring2;

cin>>mystring1>>mystring2;

if(mystring1.size()!=mystring2.size())

{

cout<<(mystring1.size()>=mystring2.size()?mystring1:mystring2)<<endl;

}

else

{

cout<<"The length of these strings are the same!"<<endl;

}

}

```

## 3.5

## 连接：

```cpp

#include <iostream>

#include <string>

using namespace std;

void main()

{
 
string mystring;

string sumstring;

while (getline(cin ,mystring))

{

sumstring += mystring;

cout<<sumstring<<endl;

}

}

```

## 分隔：

```cpp

#include <iostream>

#include <string>

using namespace std;

void main()

{ 

string mystring;

string sumstring;

while (getline(cin ,mystring))

{

sumstring = sumstring+mystring+" ";

cout<<sumstring<<endl;

}

}

```

## 6.10

```cpp

#include <iostream>

#include <string>

#include <vector>

using namespace std;

int exchange(int &val1, int &val2) 

{

int a;

a = val1;

val1 = val2;

val2 = a;

return 0;

}

void main()

{ 

cout<<"请输入需要交换的两整数:";

int val1,val2;

cin>>val1>>val2;

cout<<"交换之前的两数："<<val1<<" "<<val2<<endl;

exchange(val1,val2);

cout<<"交换之后的两数："<<val1<<" "<<val2<<endl;

}

```

## 6.19

(a)：函数只有一个参数，传入两个不合法

(b)：合法

(c)：合法

(d)：合法

## 6.39

(a)：错误，只是重复生命了

(b)：错误

(c)：正确

## 7.16

private隐藏类的相关实现细节，实现封装。访问说明符的作用域是开始知道下一个访问说明符或者类结束。不想被使用该类的程序看到的代码细节，都要private.

## 7.27

myScreen.move(4, 0).set(&apos;#&apos;).display(std::cout);

## 7.49

(a)合法 

(b)不合法，Salesdata&类型与Salesdata类型之间不可转换 

(c)不合法，const不对，因为combine本身是需要改变传入参数的

## 7.59

rate是否应该被声明为const对象呢？因为其是利率，但是实际情况中它也是可变的吧。而vec也不需要在类内就定义好大小，在另一个.h文件中声明大小就好了
