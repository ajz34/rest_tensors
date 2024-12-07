cmake_minimum_required(VERSION 3.10)

project(restmatr Fortran)

add_library(restmatr STATIC restmatr.f90)
set_property(TARGET restmatr PROPERTY POSITION_INDEPENDENT_CODE ON)
# target_link_libraries(restmatr PRIVATE openblas)

install(FILES ${CMAKE_BINARY_DIR}/librestmatr.a DESTINATION lib)

