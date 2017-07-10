cmake_minimum_required(VERSION 2.8.3)
project(yaskawa_mh24_support)

find_package(catkin REQUIRED)

catkin_package()

find_package(roslaunch)
if (roslaunch_FOUND)
	roslaunch_add_file_check(test/launch_test.xml)
endif()

install(
	DIRECTORY config launch meshes urdf
	DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
