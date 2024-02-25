#顶层目录设定cmake版本
cmake_minimum_required(VERSION 3.20)

set(CMAKE_CXX_STANDARD 17)
#设定工程名字
project(one_week_ray_trace)

# 提取 "." 路径所有源文件 为DIR_SRC
aux_source_directory(. DIR_SRC)


# 所有源文件DIR_SRC 生成可执行文件
add_executable(owrt ${DIR_SRC} 
                include/vec3.h
                include/color.h
                include/ray.h
                include/ray_color.h
                include/hittable.h
                include/sphere.h
                include/hittable_list.h
                include/interval.h
                include/camera.h
)
