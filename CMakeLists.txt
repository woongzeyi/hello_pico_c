cmake_minimum_required(VERSION 3.13)

# initialize pico-sdk from submodule
# note: this must happen before project()
include(pico-sdk/pico_sdk_init.cmake)

project(hello_pico_c)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# initialize the Raspberry Pi Pico SDK
pico_sdk_init()

add_executable(hello_pico_c
    src/main.c
)

# Add pico_stdlib library which aggregates commonly used features
target_link_libraries(hello_pico_c pico_stdlib)

# create map/bin/hex/uf2 file in addition to ELF.
pico_add_extra_outputs(hello_pico_c)
