#  minimum required cmake version: 3.8.0
cmake_minimum_required(VERSION 3.8.0)

project(RealsenseExamples-Distance)

# Save the command line compile commands in the build output
set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

add_executable(rs-distance rs-distance.c ../example.h)
target_link_libraries(rs-distance ${DEPENDENCIES})
set_target_properties (rs-distance PROPERTIES
FOLDER "Examples/C"
)

install(
TARGETS

rs-distance

RUNTIME DESTINATION
${CMAKE_INSTALL_PREFIX}/bin
)

