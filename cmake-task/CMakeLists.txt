cmake_minimum_required(VERSION 3.16)

project(calculator LANGUAGES C)

# TODO: create an executable target named calculator
add_executable(calculator
    src/main.c
    src/calculator.c
)
# Hint: sources are in src/main.c and src/calculator.c

# TODO: add the include directory for the calculator target
target_include_directories(calculator PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
set_target_properties(calculator PROPERTIES
    C_STANDARD 99
    C_STANDARD_REQUIRED YES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}
)
