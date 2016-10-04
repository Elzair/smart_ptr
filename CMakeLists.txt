cmake_minimum_required(VERSION 3.3)

project(boost_smart_ptr)

add_library(boost_smart_ptr INTERFACE)

target_include_directories(boost_smart_ptr BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_smart_ptr DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::smart_ptr ALIAS boost_smart_ptr)
