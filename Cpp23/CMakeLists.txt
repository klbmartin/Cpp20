set(CMAKE_CXX_SCAN_FOR_MODULES ON)

# Create a library
add_library(foo)
# Add the module file to the library
target_sources(foo
  PUBLIC
    FILE_SET CXX_MODULES FILES
      math1.ixx
)
# Create an executable
add_executable(client2 client2.cpp)
# Link to the library foo
target_link_libraries(client2 foo)