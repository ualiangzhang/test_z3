cmake_minimum_required(VERSION 3.19)
project(test_z3)

set(CMAKE_CXX_STANDARD 17)
#set(CMAKE_CXX_STANDARD_REQUIRED True)
#add_subdirectory(z3)
find_package(Z3 REQUIRED)

add_executable(test_z3 main.cpp)

#target_link_libraries(test_z3 PUBLIC z3)
#

target_include_directories(test_z3 PRIVATE ${Z3_CXX_INCLUDE_DIRS})
target_link_libraries(test_z3 PRIVATE ${Z3_LIBRARIES})

#target_link_libraries(test_z3 PUBLIC "${PROJECT_BINARY_DIR}")
#target_include_directories(test_z3 PUBLIC "${z3/src/api}")
#target_include_directories(test_z3 PUBLIC ${z3/src/api/c++})
