cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(test_project C CXX ASM)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
pico_sdk_init()

add_executable(pico-midi-test
  pico-midi-test.c
  usb_descriptors.c
)

pico_enable_stdio_usb(pico-midi-test 0)
pico_enable_stdio_uart(pico-midi-test 1)

target_include_directories(pico-midi-test PRIVATE ${CMAKE_CURRENT_LIST_DIR})

pico_add_extra_outputs(pico-midi-test)
target_link_libraries(pico-midi-test PRIVATE pico_stdlib tinyusb_device tinyusb_board)
