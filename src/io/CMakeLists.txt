# 生成静态库 cminus_io
add_library(cminus_io io.c)

# 将cminus_io添加在/lib目录下
install(
    TARGETS cminus_io
    ARCHIVE DESTINATION lib
)
