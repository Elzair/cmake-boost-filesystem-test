if(APPLE)
  cmake_minimum_required(VERSION 2.8.11 FATAL_ERROR)
else()
  cmake_minimum_required(VERSION 2.8.7 FATAL_ERROR)
endif()

add_subdirectory(libs)

project(TestFilesystem)

include_directories(${BOOST_INCLUDE_DIRS})

add_executable(test-filesystem test.cpp)

message(STATUS "Boost headers: ${BOOST_INCLUDE_DIRS}")
message(STATUS "Boost libraries: ${BOOST_LIBRARIES}")

target_link_libraries(test-filesystem ${BOOST_LIBRARIES})
set_property(TARGET test-filesystem PROPERTY CXX_STANDARD 11)
set_property(TARGET test-filesystem PROPERTY CXX_STANDARD_REQUIRED ON)
