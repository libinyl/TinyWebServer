cmake_minimum_required(VERSION 3.0)
project(TinyWebServer CXX)

set(CMAKE_CXX_STANDARD 11)

add_executable(server ./timer/lst_timer.cpp ./http/http_conn.cpp ./log/log.cpp ./CGImysql/sql_connection_pool.cpp  webserver.cpp config.cpp main.cpp)
target_link_libraries(server pthread mysqlclient)