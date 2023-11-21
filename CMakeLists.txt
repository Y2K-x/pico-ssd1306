add_library(pico-ssd1306 INTERFACE)

target_sources(pico-ssd1306 INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/ssd1306.cpp
)

target_include_directories(pico-ssd1306 INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}
)

target_link_libraries(pico-ssd1306 INTERFACE
    pico_stdlib
    hardware_spi
    hardware_dma
    hardware_pio
    hardware_timer
    hardware_clocks
)
