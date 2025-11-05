cmake_minimum_required(VERSION 3.12)

project(ModernCppFaturesAnalysis)

# 设置 C++ 标准（如 C++17）
set(CMAKE_CXX_STANDARD 14)
# 强制使用指定的标准，不允许编译器扩展（可选，推荐严格遵循标准）
set(CMAKE_CXX_STANDARD_REQUIRED ON)
# 禁用编译器特定扩展（如 -std=gnu++17 会包含 GCC 扩展，此选项关闭后为 -std=c++17）
set(CMAKE_CXX_EXTENSIONS OFF)

add_compile_options(
    $<$<CXX_COMPILER_ID:GNU>:-O0>
)

add_subdirectory(06.rvalueReference)