cmake_minimum_required(VERSION 3.23)
project(database-programming-1)

set(CMAKE_CXX_STANDARD 20)

add_executable(database-programming-1 main.cpp mappers/account_mapper.hpp mappers/client_mapper.hpp mappers/deposit_mapper.hpp sql_executor.hpp entities/account.cpp entities/account.hpp entities/client.cpp entities/client.hpp entities/deposit.cpp entities/deposit.hpp)

target_include_directories(database-programming-1 PRIVATE .)

target_link_libraries(database-programming-1 odbc32)
