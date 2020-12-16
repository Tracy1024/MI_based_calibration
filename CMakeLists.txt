# SOURCE
set (SRC
  main.cpp 
  Calibration.cpp  Calibration.h
  )

add_executable (mi-extrinsic-calib ${SRC})
target_link_libraries (mi-extrinsic-calib
  ${Glib_LIBRARIES}
  ${GSL_LIBRARIES}
  ${OpenCV_LIBRARIES}
  ${PCL_LIBRARIES}
  common
  )
include_directories (${Glib_INCLUDE_DIRS}
  ${GSL_INCLUDE_DIR} 
  ${OpenCV_INCLUDE_DIRS}
  ${PCL_INCLUDE_DIRS}
  ${SRC_DIR}/common 
  )
add_definitions(${PCL_DEFINITIONS})
