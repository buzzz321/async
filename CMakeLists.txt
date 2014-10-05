project(async)

cmake_minimum_required(VERSION 2.6.2)
################################
# Compiler thingies
################################

#SET (CMAKE_C_COMPILER   "clang")
#SET (CMAKE_CXX_COMPILER "clang++")
list(APPEND CMAKE_CXX_FLAGS "-Wall --pedantic -O3 -std=c++0x  -pthread") #-fno-exceptions

################################
# Unit Tests
################################
# Add test cpp file
set (async_SRC async.cc
      )
add_executable( async ${async_SRC})
# Link test executable against gtest & gtest_main
#target_link_libraries(runUnitTests gtest gtest_main 
#                      ${QT_LIBRARIES}
#                      ${Boost_LIBRARIES})
#add_test( runUnitTests runUnitTests )
