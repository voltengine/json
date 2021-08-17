cmake_minimum_required(VERSION 3.20)
project(JSON LANGUAGES CXX)

add_library(JSON INTERFACE)
add_library(JSON::JSON ALIAS JSON)

target_include_directories(APP PUBLIC
	"${CMAKE_CURRENT_SOURCE_DIR}/include/"
)

set_target_properties(APP PROPERTIES
    CXX_STANDARD 11
    OUTPUT_NAME "json"
)
