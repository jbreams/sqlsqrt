add_subdirectory(variant-1.4.0)
add_subdirectory(fmt-7.1.3)
add_subdirectory(hat-trie-0.6.0)

add_library(linenoise STATIC linenoise-master/linenoise.c)
target_include_directories(linenoise INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/linenoise-master)

add_library(odpi STATIC odpi-4.1.0/embed/dpi.c)
target_include_directories(odpi PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/odpi-4.1.0/include)
