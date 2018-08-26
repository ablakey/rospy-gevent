cmake_minimum_required(VERSION 2.8.3)
project(rospy_gevent)

find_package(catkin REQUIRED COMPONENTS
  rospy
)

catkin_package()

catkin_install_python(
    PROGRAMS
        scripts/gevent_publisher
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
