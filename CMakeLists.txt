cmake_minimum_required(VERSION 3.8)
project(trailblazer_description)

# Find required ROS 2 packages
find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)

# Install directories
install(
  DIRECTORY
    meshes
    launch
    urdf
  DESTINATION share/${PROJECT_NAME}
)

# Install Python scripts
install(PROGRAMS
  scripts/multical_to_urdf.py
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()
