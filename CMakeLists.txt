cmake_minimum_required(VERSION 3.10.2)
project(ocs2_robotic_assets)

find_package(ament_cmake REQUIRED)

###################################
## catkin specific configuration ##
###################################

###########
## Build ##
###########

# Resolve for the package path at compile time.
configure_file (
  "${PROJECT_SOURCE_DIR}/include/${PROJECT_NAME}/package_path.h.in"
  "${PROJECT_SOURCE_DIR}/include/${PROJECT_NAME}/package_path.h" @ONLY
)

#############
## Install ##
#############

install(DIRECTORY include/
  DESTINATION include
)

install(DIRECTORY resources
  DESTINATION share/${PROJECT_NAME}
)

ament_package()