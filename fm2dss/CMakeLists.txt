enable_language(Fortran)
file ( GLOB fm2dss_fortran_functions *.f* )
find_package(Python REQUIRED COMPONENTS Interpreter Development.Module)
Python_add_library(libfm2dss MODULE WITH_SOABI ${fm2dss_fortran_functions})

install(TARGETS libfm2dss DESTINATION ./pyfm2dss)
