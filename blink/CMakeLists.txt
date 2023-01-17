add_executable(blink
        blink.c
        )

# pull in common dependencies
target_link_libraries(blink 
        pico_stdlib # Needed for core functionality
        pico_cyw43_arch_none # Only used in this project to access the GPIO
        )

# create map/bin/hex file etc.
pico_add_extra_outputs(blink)