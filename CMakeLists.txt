cmake_minimum_required(VERSION 3.12)

project(BreakOut    VERSION 0.0.1
                    DESCRIPTION "A simple BreakOut clone"
                    LANGUAGES CXX)

set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

set(SRCS
    main.cpp)

foreach(S ${SRCS})
    list(APPEND ALL_SRCS ${SRC_DIR}/${S})
endforeach()

add_executable(${PROJECT_NAME} ${ALL_SRCS})

target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_17)

