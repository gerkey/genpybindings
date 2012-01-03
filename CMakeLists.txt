cmake_minimum_required(VERSION 2.8)
project(genpybindings)

find_package(catkin)

add_subdirectory(scripts)

catkin_project(genpybindings
  VERSION 0.0.0
  CFG_EXTRAS genpybindings-extras.cmake
  )

file(WRITE ${CMAKE_CURRENT_BINARY_DIR}/genpybindings "Boost.Python bindings to C++")
install(FILES ${CMAKE_CURRENT_BINARY_DIR}/genpybindings
  DESTINATION etc/langs
  )

