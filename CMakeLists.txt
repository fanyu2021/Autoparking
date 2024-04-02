cmake_minimum_required(VERSION 3.12)

project(Q_learning_parking)

set(CMAKE_CXX_STANDARD 17)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src/thirdparty/allegro5.2.4/include)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/conf)

link_directories(${CMAKE_CURRENT_SOURCE_DIR}/src/thirdparty/allegro5.2.4/lib)

# aux_source_directory(SRC src/*.h src/*.cpp)
aux_source_directory(./src/ src_list)

add_executable(${PROJECT_NAME} ${src_list})
target_link_directories(${PROJECT_NAME} PUBLIC allegro allegro_primitives allegro_font allegro_ttf)

# add_executable(test_collision ${src_list})
# target_link_directories(${PROJECT_NAME} PUBLIC allegro allegro_primitives allegro_font allegro_ttf)

# add_executable(test_maneuver ${src_list})
# target_link_directories(${PROJECT_NAME} PUBLIC allegro allegro_primitives allegro_font allegro_ttf)

# add_executable(test_movements ${src_list})
# target_link_directories(${PROJECT_NAME} PUBLIC allegro allegro_primitives allegro_font allegro_ttf)

# add_executable(test_shapes ${src_list})
# target_link_directories(${PROJECT_NAME} PUBLIC allegro allegro_primitives allegro_font allegro_ttf)
