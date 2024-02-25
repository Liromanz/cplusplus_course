cmake_minimum_required(VERSION 3.29)        #версия cmake

project(
    lession1                                #название проекта
    VERSION 1.0
    DESCRIPTION "первый проект"
    LANGUAGES CXX                           #cxx это с++
)

set(CMAKE_CXX_STANDARD 17)                  #условно, версия самого языка. внизу - проверка на то, что именно эта версия у нас стоит
set(CMAKE_CXX_STANDARD_REQUIRED ON)

#set(CMAKE_BUILD_TYPE RELEASE)

add_executable(lession1)                    #так делается экзешник
#add_library(lession1)                      #так делается либа, с SHARED она будет динамическая

set(sources                                 #файлы внутри проекта. sources считай как условное название хранилища для перечисленных файлов. имя не зависит от папки
    main.cpp
)

target_sources(lession1 PRIVATE ${sources}) #проект это файлы, которые мы перечислили