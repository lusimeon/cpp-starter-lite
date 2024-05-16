cmake_minimum_required(VERSION 3.16)

# ---- Add source files ----

# Note: globbing sources is considered bad practice as CMake's generators may not detect new files
# automatically. Keep that in mind when changing files, or explicitly mention them here.
file(GLOB_RECURSE headers CONFIGURE_DEPENDS "*.hpp")
file(GLOB_RECURSE sources CONFIGURE_DEPENDS "*.cpp")

# ---- Create library ----

# Note: for header-only libraries change all PUBLIC flags to INTERFACE and create an interface
# target: add_library(${PROJECT_NAME} INTERFACE)
add_library(lib${PROJECT_NAME} ${headers} ${sources})
target_include_directories(lib${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})