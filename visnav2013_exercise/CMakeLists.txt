cmake_minimum_required(VERSION 2.8)
project(visnav2013_exercise)

find_package(catkin REQUIRED roscpp std_msgs ardrone_autonomy)

catkin_package(
CATKIN_DEPENDS roscpp std_msgs 
)

include_directories(include ${catkin_INCLUDE_DIRS})
add_executable(ex1_ardrone_odometry src/main.cpp src/trajectory_visualizer.cpp)
target_link_libraries(ex1_ardrone_odometry ${catkin_LIBRARIES})
add_dependencies(ex1_ardrone_odometry ${catkin_EXPORTED_TARGETS})
