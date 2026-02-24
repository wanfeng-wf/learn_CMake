cmake_minimum_required(VERSION 3.10)

project(C_Step2 VERSION 1.0 LANGUAGES C)

# 1. 设置 C 标准为 C11
set(CMAKE_C_STANDARD 11)
# 强制要求编译器支持该标准，如果不支持则报错，而不是降级处理
set(CMAKE_C_STANDARD_REQUIRED ON)
# 禁用编译器私有扩展（如 GCC 的 gnu11），确保代码的跨平台标准兼容性
set(CMAKE_C_STANDARD_EXTENSIONS OFF)

# 2. 使用变量管理源文件（当文件多起来时非常有用）
set(SRC_LIST main.c)

# 3. 引用变量使用 ${} 语法
add_executable(c_app ${SRC_LIST})