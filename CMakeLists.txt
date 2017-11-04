cmake_minimum_required(VERSION 3.5.1)

project (bandit )

set(PROJECT_VERSION "1.0.0")

#--- Compiler options
if(CMAKE_COMPILER_IS_GNUCC)
   add_definitions(-Wall -Werror -pedantic -std=c99)
endif(CMAKE_COMPILER_IS_GNUCC)


file(GLOB SOURCES "src/*.c")

add_executable(bandit ${SOURCES})

target_link_libraries(bandit m)
