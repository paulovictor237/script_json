#=====================================
# ... script_exe (2020) ...
#=====================================

# Comando para compilar e executar o arquivo
# cmake . && make && ./script_exe

cmake_minimum_required(VERSION 3.0.2)
project (script_exe)

set (CMAKE_CXX_STANDARD 14)
include_directories(${PROJECT_SOURCE_DIR})

add_executable(script_exe 
    src/main.cpp
    src/comum.cpp 
    src/matriz_pontos.cpp
    src/simulacao.cpp
)

add_custom_target(run
    COMMAND script_exe
    DEPENDS script_exe
    WORKING_DIRECTORY ${CMAKE_PROJECT_DIR}
)



