project(soil)

set(PROJ_NAME soil)
set(PROJ_FOLDER ${CMAKE_CURRENT_SOURCE_DIR})

set(SOURCES
    ${PROJ_FOLDER}/src/image_dxt.c
    ${PROJ_FOLDER}/src/image_helper.c
    ${PROJ_FOLDER}/src/soil.c
    ${PROJ_FOLDER}/src/stb_image_aug.c
)	

set(HEADERS
    ${PROJ_FOLDER}/include/SOIL/image_dxt.h
    ${PROJ_FOLDER}/include/SOIL/image_helper.h
    ${PROJ_FOLDER}/include/SOIL/SOIL.h
    ${PROJ_FOLDER}/include/SOIL/stb_image_aug.h
    ${PROJ_FOLDER}/include/SOIL/stbi_dds_aug_c.h
    ${PROJ_FOLDER}/include/SOIL/stbi_dds_aug.h
)

add_library(${PROJ_NAME} ${SOURCES} ${HEADERS})
set_target_properties(${PROJ_NAME} PROPERTIES FOLDER "xclass/libs/3rdParty")

target_include_directories(${PROJ_NAME} PRIVATE ${PROJ_FOLDER}/include)
