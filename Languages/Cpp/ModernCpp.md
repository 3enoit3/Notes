# Modern C++
According to https://arne-mertz.de/2018/08/modern-c-newest-standard/:
* RAII
* Strong typing
* Compile time programming

# Features
* [Features](https://3enoit3.github.io/data_tools.js/lists/)
* Meyer
  * List: https://www.artima.com/shop/overview_of_the_new_cpp
  * Effective Modern C++: www.xavierlamorlette.fr/programmation/cpp/effective_modern_cpp/

## Constexpr
* possible to evaluate the value of the function or variable at compile time
http://b.atch.se/posts/constexpr-meta-container/
```c++
constexpr int var;
constexpr int f(int i) {...}
```
constexpr is a property of the function, not of the function's input

## Auto
https://herbsutter.com/2013/08/12/gotw-94-solution-aaa-style-almost-always-auto/
* Only way to type lambda
* auto to track (deduce) vs auto to stick (commit): https://www.fluentcpp.com/2018/09/28/auto-stick-changing-style/
* Force POD initialization

## Enum
An enumerator declared in class scope can be referred to using the class member access operators (::, . and ->)
```c++
namespace N { enum E { X }; }
::N::X; // all standards
::N::E::X; // C++11
```
## Literals
```c++
char b = 0b00110011; //C++14
```
## Delegated constructors
```c++
class C {
  C() {}
  C(int i) : C() {} // C++11 - only one member-initializer: "C(int i) : C(), j_(0) {}" is not valid
};
```
## Template
### Argument deduction
```c++
std::pair p{1, 2}; // C++17
```
### Using
```c++
template <typename T> using ptr = T*; 
ptr<int> x;
```
# Misc
## C++ is moving towards a “left to right” syntax
```c++
auto name = type_and_value;
using name = type;
auto f() -> type {}
```
## Design
* Modern JSON interface: https://github.com/nlohmann/json/tree/v3.3.0

# Links
* https://github.com/AnthonyCalandra/modern-cpp-features
* https://stackoverflow.com/questions/38060436/what-are-the-new-features-in-c17
* Some c++17 features: https://blog.jetbrains.com/rscpp/whats-new-in-resharper-cpp-2018-2/
* https://www.learncpp.com/cpp-tutorial/b-1-introduction-to-c11/
