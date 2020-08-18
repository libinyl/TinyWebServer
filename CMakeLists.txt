cmake_minimum_required(VERSION 3.0)
project(TinyWebServer CXX)

set(CMAKE_CXX_STANDARD 11)

file(GLOB SOURCEFILE *.cpp timer/*.cpp threadpool/*.cpp http/*.cpp log/*.cpp lock/*.cpp CGImysql/*.cpp)
add_executable(server ${SOURCEFILE})
target_link_libraries(server pthread mysqlclient)