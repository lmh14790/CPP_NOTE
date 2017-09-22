# CPP_NOTE  
### 类型别名 typedef和using c++11推荐  
```c++
//1可读性更强
typedef int *P;
using  p = int *p;
typedef std::string (Foo::* fooMemFnPtr) (const std::string&);
//函数指针方面可读性更强
using fooMemFnPtr = std::string (Foo::*) (const std::string&);
//2模板别名
template <typename T>
using Vec = MyVector<T, MyAlloc<T>>;
Vec<int> vec;
```
### unsigned  使用的时候确保不会出现负值 否则结果错误  对于char类型会存在 unsigned char,signed char，char 根据机器不同char的符号不同
### decltype类型根据表达是的右值来推断类型  
```c++
const int ci = 0; &cj =  ci;  
decltype(ci) x = 0;  
decltype(cj) z = ci;  
std::sting getStr(){
return "ccc";
}
decltype(getStr()) str = "C++11类型推断";
```
