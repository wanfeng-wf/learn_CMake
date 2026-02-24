# 导出编译命令数据库（可选）
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# 1. 指定 CMake 的最低版本要求
cmake_minimum_required(VERSION 3.10)

# 2. 定义项目名称和版本
project(HelloWorld VERSION 1.0 LANGUAGES C)

# 3. 指定生成的可执行程序名及其源码文件
add_executable(hello_cmake main.c)