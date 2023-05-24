cmake_minimum_required(VERSION 3.10)
project(cuda_qujibian)
set(CMAKE_CUDA_COMPILER "/usr/local/cuda-10.2/bin/nvcc")
find_package(CUDA REQUIRED)
find_package(OpenCV REQUIRED)
set(CMAKE_CUDA_STANDARD 11)

cuda_add_executable(cuda_qujibian main.cu)

target_link_libraries(cuda_qujibian ${CUDA_LIBRARIES} ${OpenCV_LIBRARIES})

#适配车道线检测项目，以后的训练图片都可以从这边生成