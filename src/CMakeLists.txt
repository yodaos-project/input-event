aux_source_directory(. DIR_SRCS)

add_library(input-event SHARED input-event.c ${DIR_SRCS})
target_link_libraries(input-event rklog)
install( TARGETS input-event ${INSTALL_EXPORT}
     RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
     LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
     ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR})
