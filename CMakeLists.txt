set (TARGET_NAME libsds)
set (SRCS
  sds.c
)
set (C_INCLUDES
  ./
)
 
set (EXPORT_HEADER_FILES
  sds.h
)
set (EXPORT_HEADER_DIR libsds)
 
include_directories (${C_INCLUDES})
add_library (${TARGET_NAME} SHARED ${SRCS})
set_target_properties (${TARGET_NAME}
                       PROPERTIES PREFIX
                       "")
copy_headers (${TARGET_NAME} ${EXPORT_HEADER_DIR} "${EXPORT_HEADER_FILES}")
