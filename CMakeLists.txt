cmake_minimum_required(VERSION 3.13)

if(ESP_PLATFORM)
  file(GLOB_RECURSE PUBSUBCLIENT
    "src/*.*"
  )

  idf_component_register(
    SRCS ${PUBSUBCLIENT} 
    INCLUDE_DIRS src 
    REQUIRES arduino
  )

  return()
endif()
