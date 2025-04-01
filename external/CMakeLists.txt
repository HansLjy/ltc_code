add_library(external_libraries INTERFACE)

add_subdirectory(glm)
target_link_libraries(external_libraries INTERFACE glm)

find_package(X11 REQUIRED)

message(STATUS "X11_FOUND = ${X11_FOUND}")
message(STATUS "X11_INCLUDE_DIR = ${X11_INCLUDE_DIR}")
message(STATUS "X11_LIBRARIES = ${X11_LIBRARIES}")


target_include_directories(external_libraries INTERFACE ${X11_INCLUDE_DIR})
target_link_libraries(external_libraries INTERFACE ${X11_LIBRARIES})
target_include_directories(external_libraries INTERFACE CImg)
