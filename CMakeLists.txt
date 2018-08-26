cmake_minimum_required(VERSION 2.8.3)
project(rospy_gevent)

find_package(catkin REQUIRED COMPONENTS
  rospy
)

catkin_package()

catkin_install_python(
  PROGRAMS
        scripts/greenlet_simple
        scripts/patched_publisher
        scripts/patched_subscriber
        scripts/patched_threads
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(
  DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
  FILES_MATCHING PATTERN "*.launch"
)
