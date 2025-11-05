add_executable(APP 6-4.cpp)

target_compile_options(APP PRIVATE
    $<$<CXX_COMPILER_ID:GNU>:-fno-elide-constructors>
)

# C++17 引入了 “强制复制省略”，对于某些场景，编译器必须省略拷贝 / 移动，此时即使使用 -fno-elide-constructors 也无法禁用。