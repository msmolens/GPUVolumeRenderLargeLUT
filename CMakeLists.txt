
cmake_minimum_required(VERSION 2.8)

PROJECT(GPUVolumeRenderLargeLUT)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})

add_executable(GPUVolumeRenderLargeLUT MACOSX_BUNDLE GPUVolumeRenderLargeLUT)

if(VTK_LIBRARIES)
  target_link_libraries(GPUVolumeRenderLargeLUT ${VTK_LIBRARIES})
else()
  target_link_libraries(GPUVolumeRenderLargeLUT vtkHybrid vtkWidgets)
endif()
