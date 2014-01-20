cmake_minimum_required (VERSION 2.8)
project (card_polling)

#file(GLOB_RECURSE SOURCE_TMP "*.c" )
#list(APPEND SRC ${SOURCE_TMP})


include_directories (
	"${PROJECT_SOURCE_DIR}/wiringPi"
	"${PROJECT_SOURCE_DIR}/NxpRdLib_PublicRelease/intfs"
    "${PROJECT_SOURCE_DIR}/NxpRdLib_PublicRelease/types"
    "${PROJECT_SOURCE_DIR}/NxpRdLib_PublicRelease/comps/phpalSli15693/src/Sw"
)


set(EXT_LIBS  pthread  m)

add_definitions(-g -O0)

list(APPEND SOURCE "${PROJECT_SOURCE_DIR}/main.c")
source_group(src "${PROJECT_SOURCE_DIR}/main.c")

file(GLOB_RECURSE SOURCE_TMP "${PROJECT_SOURCE_DIR}/NxpRdLib_PublicRelease/*.c" )
list(APPEND SOURCE ${SOURCE_TMP})
#source_group(wiringPi FILES ${SOURCE_TMP})

#list(REMOVE_ITEM SOURCE "${PROJECT_SOURCE_DIR}/NxpRdLib_PublicRelease/ex/NxpRdLib.c")


add_executable(${PROJECT_NAME} ${SOURCE})
target_link_libraries(${PROJECT_NAME} ${EXT_LIBS})
