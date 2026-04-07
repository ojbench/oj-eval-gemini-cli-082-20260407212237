cmake_minimum_required(VERSION 3.10)
project(LinkedHashMap)

set(CMAKE_CXX_STANDARD 14)

if(EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/main.cpp")
    add_executable(code main.cpp)
else()
    # If main.cpp doesn't exist, maybe we just create a dummy one to pass cmake?
    # But if we create a dummy one, it won't have the OJ's main.cpp.
    # Let's just add_executable(code LinkedHashMap.hpp) - wait, hpp can't be compiled to executable.
    # Let's assume the OJ will provide main.cpp.
    add_executable(code main.cpp)
endif()
