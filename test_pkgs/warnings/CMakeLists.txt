cmake_minimum_required(VERSION 2.8.3)
project(warnings)

add_compile_options(-std=c++14)
find_package(catkin REQUIRED)

message(WARNING "Dummy cmake warning for unittest")

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

if(CATKIN_ENABLE_TESTING)
  catkin_add_gtest(${PROJECT_NAME} test.cpp)
endif()
