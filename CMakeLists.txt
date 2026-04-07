cmake_minimum_required(VERSION 3.10)
project(LinkedHashMap)

set(CMAKE_CXX_STANDARD 14)

file(GLOB SOURCES "*.cpp")

if(SOURCES)
    add_executable(code ${SOURCES})
else()
    # Create a dummy main.cpp so cmake doesn't fail if there are no cpp files
    file(WRITE dummy.cpp "int main() { return 0; }")
    add_executable(code dummy.cpp)
endif()
