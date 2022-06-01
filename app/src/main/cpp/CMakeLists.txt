cmake_minimum_required(VERSION 3.21)

project(love-android LANGUAGES C CXX)

if(TARGET oboe::oboe)
	message(WARNING "OBOE is target")
else()
	message(WARNING "OBOE is not target")
endif()
find_package(Oboe REQUIRED)
if(TARGET oboe::oboe)
	message(WARNING "OBOE is target")
else()
	message(WARNING "OBOE is not target")
endif()

set(MEGA_LOVE "${CMAKE_CURRENT_SOURCE_DIR}/love")

add_subdirectory(megasource)
