cmake_minimum_required(VERSION 3.10)
project(MultiFile_Step3 LANGUAGES C)

# 出编译命令数据库（可选）
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# 1. 设置变量存储源文件路径
# 我们手动列出所有源文件，这是最推荐的做法，因为清晰、可控
set(SOURCES 
    src/main.c 
    src/hello.c
)

# 2. 告诉 CMake 头文件在哪里
# 这样你在代码里写 #include "hello.h" 时，编译器就能在 include/ 目录下找到它
# target_include_directories 是“现代 CMake”推荐的做法
add_executable(multi_app ${SOURCES})

target_include_directories(multi_app PUBLIC include)