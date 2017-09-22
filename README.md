# CPP_NOTE  
### typedef和using  
### unsigned  使用的时候确保不会出现负值 否则结果错误  对于char类型会存在 unsigned char,signed char，char 根据机器不同char的符号不同
### decltype类型根据表达是的右值来推断类型  
```c++
const int ci = 0; &cj =  ci;  
decltype(ci) x = 0;  
decltype(cj) z = ci;  
std::sting getStr(){
return "ccc";
}
dedlpty(getStr()) str = "C++11类型推断";
```c++
