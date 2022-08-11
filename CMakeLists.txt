cmake_minimum_required(VERSION 3.24.0)

project(SFML_TUTORIAL)

add_executable(${PROJECT_NAME} main.cpp)


# Add SFML Lirary Path
add_subdirectory(Lib/SFML)
# Target Include Directory
target_include_directories(${PROJECT_NAME} PUBLIC Lib/SFML/include)
# Target Link Directories
target_link_directories(${PROJECT_NAME} PRIVATE Lib/SFML/src)
# Target Link Libraries
target_link_libraries(${PROJECT_NAME} sfml-graphics sfml-window sfml-system)
#${CMAKE_SOURCE_DIR}/out/bin/Lib/SFML/lib/Debug/sfml-main-d.lib
