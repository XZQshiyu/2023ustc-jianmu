# 生成可执行程序 cminusfc
# 依赖为 cminusfc.cpp cimusf_builder.cpp
add_executable(
    cminusfc
    cminusfc.cpp
    cminusf_builder.cpp
)
# 链接动态库
# 将 IR_lib,common,syntax, codegen, stdc++fs, opt_lib链接到 cminusfc
target_link_libraries(
    cminusfc
    IR_lib
    common
    syntax
    codegen
    stdc++fs
    opt_lib
    sysy
)

# 添加为全局路径,可以在任意路径下执行cminusfc,默认将cminusf添加到 /usr/local/bin路径下
install(
    TARGETS cminusfc
    RUNTIME DESTINATION bin
)
