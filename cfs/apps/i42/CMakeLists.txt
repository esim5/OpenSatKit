cmake_minimum_required(VERSION 2.6.4)
project(CFS_I42 C)

include_directories(fsw/mission_inc)
include_directories(fsw/platform_inc)
include_directories(${f42_MISSION_DIR}/fsw/platform_inc)
include_directories(${f42_MISSION_DIR}/fsw/src)
include_directories(${app_fw_lib_MISSION_DIR}/fsw/platform_inc)
include_directories(${app_fw_lib_MISSION_DIR}/fsw/mission_inc)

aux_source_directory(fsw/src APP_SRC_FILES)

# Create the app module
add_cfe_app(i42 ${APP_SRC_FILES})

