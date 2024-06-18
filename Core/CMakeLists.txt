add_library(Core "")

target_sources(Core 
  PRIVATE
    Core.hpp
    Core.cpp
)
target_include_directories(Core PUBLIC ${CMAKE_CURRENT_LIST_DIR})