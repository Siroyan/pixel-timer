cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(pixel-timer_project C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
pico_sdk_init()

add_executable(pixel-timer
  src/main.cpp
)

pico_enable_stdio_usb(pixel-timer 1)
pico_enable_stdio_uart(pixel-timer 1)

pico_add_extra_outputs(pixel-timer)

target_link_libraries(pixel-timer pico_stdlib)