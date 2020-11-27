file(GLOB SOURCES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.c *.h)
include_directories(${X11_INCLUDE_DIR})

add_executable(xidle  ${SOURCES})
target_link_libraries(xidle PUBLIC ${X11_Xscreensaver_LIB} ${X11_X11_LIB})

install(TARGETS xidle RUNTIME DESTINATION bin)
