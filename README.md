# Лабораторная работа 3

**Задание №1**
```
touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(formatter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter STATIC formatter.cpp formatter.h)


cmake -H. -B_build
cmake --build _build
```
![](https://raw.githubusercontent.com/Sxeigumen/Lab3-TiMP/master/фото/1.png)

**Задание №2**
```
touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(formatter_ex)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter_ex STATIC formatter_ex.cpp formatter_ex.h)

include_directories(/mnt/c/Users/artem/workspace/Timp3/formatter_lib)
target_link_libraries(formatter_ex formatter)


cmake -H. -B_build
cmake --build _build
```
![](https://github.com/Sxeigumen/Lab3-TiMP/blob/master/фото/2.png)

**Задание №3**
```
touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(solver STATIC solver.cpp solver.h)


cmake -H. -B_build
cmake --build _build



touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hello_world hello_world.cpp)

include_directories(/mnt/c/Users/artem/workspace/Timp3/formatter_ex_lib)
target_link_libraries(hello_world formatter_ex)



touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(equation)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(equation equation.cpp)

include_directories(/mnt/c/Users/artem/workspace/Timp3/formatter_ex_lib)
include_directories(/mnt/c/Users/artem/workspace/Timp3/solver_lib)

target_link_libraries(equation formatter_ex)
target_link_libraries(equation solver)

```
![](https://github.com/Sxeigumen/Lab3-TiMP/blob/master/фото/3.1.png)
![](https://github.com/Sxeigumen/Lab3-TiMP/blob/master/фото/3.2.png)
![](https://github.com/Sxeigumen/Lab3-TiMP/blob/master/фото/3.2.1.png)
![](https://github.com/Sxeigumen/Lab3-TiMP/blob/master/фото/3.3.png)
