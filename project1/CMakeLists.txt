cmake_minimum_required(VERSION 3.11)
SET(CMAKE_CXX_COMPILER /Users/iwahori/llvm/5.0.1/build/bin/clang++)
set(CMAKE_CXX_STANDARD 17)
project(clang-sandbox-test1)

include_directories(${Boost_INCLUDE_DIRS})
include_directories(~/llvm/5.0.1/llvm/tools/clang/include)
find_library(lib_clang NAMES libclang.dylib PATHS ~/llvm/5.0.1/build/lib)

add_executable(clang-sandbox-test1 main.cpp)
target_link_libraries(clang-sandbox-test1 ${lib_clang})

