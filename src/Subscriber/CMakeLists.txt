cmake_minimum_required(VERSION 2.8.3)
project(subscriber)

find_package(catkin REQUIRED
  roscpp
  std_msgs
)

catkin_package()

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(subscriberNode src/subscriber.cpp)
target_link_libraries(subscriberNode ${catkin_LIBRARIES})
