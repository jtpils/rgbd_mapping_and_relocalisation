#File Generated by Hans J. Johnson
#Please contact hans-johnson@uiowa.edu for making enhancments/corrections
PROJECT(NIFTILIB)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/../../zlib)
INCLUDE_DIRECTORIES(${ZNZLIB_SOURCE_DIR})
SET(NIFTILIB_SRC nifti1_io.c)

SET(NIFTI_NIFTILIB_NAME ${PACKAGE_PREFIX}niftiio)
ADD_LIBRARY(${NIFTI_NIFTILIB_NAME} ${NIFTILIB_SRC} )
TARGET_LINK_LIBRARIES( ${NIFTI_NIFTILIB_NAME} ${PACKAGE_PREFIX}znz)

IF(UNIX)
  TARGET_LINK_LIBRARIES(${NIFTI_NIFTILIB_NAME} -lm)
ENDIF(UNIX)


