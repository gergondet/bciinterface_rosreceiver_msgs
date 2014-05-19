cmake_minimum_required(VERSION 2.8.3)
project(bciinterface_rosreceiver_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_message_files(
  DIRECTORY msg
  FILES
  BCICommand.msg
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package()

install(DIRECTORY include/${PROJECT_NAME}/
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
  FILES_MATCHING PATTERN "*.h")
