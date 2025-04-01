add_library(fit_ltc dds.cpp)
target_include_directories(fit_ltc PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(fit_ltc PUBLIC external_libraries)