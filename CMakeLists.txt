cmake_minimum_required(VERSION 3.0.0)
project(skillup VERSION 0.1.0 LANGUAGES CXX)

if (CMAKE_CXX_COMPILER_ID STREQUAL "Clang")
    set(CMAKE_CXX_FLAGS_RELEASE "-Ofast")
  # add_compile_options(-Ofast)
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    set(CMAKE_CXX_FLAGS_RELEASE "-Ofast")
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "Intel")
  # using Intel C++
else ()
  set(CMAKE_CXX_FLAGS_RELEASE "-Ox")
endif()

# Packagegs
# find_package(unofficial-sqlite3 CONFIG REQUIRED)

# Include dir
add_subdirectory(Core)
add_subdirectory(App)

# target_link_libraries(skillup PRIVATE unofficial::sqlite3::sqlite3)

include(CTest)
enable_testing()

