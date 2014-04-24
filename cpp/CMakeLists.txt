include_directories(${CMAKE_CURRENT_LIST_DIR})

#== Library ==================================================================#
list(APPEND src sgp4ext.cpp)
list(APPEND src sgp4io.cpp)
list(APPEND src sgp4unit.cpp)
add_library(sgp4 ${src})
#=============================================================================#

#== Test Executable ==========================================================#
add_executable(test_sgp4 testcpp.cpp)
target_link_libraries(test_sgp4 sgp4)
#=============================================================================#

#== Install Targets ==========================================================#
install(FILES       sgp4unit.h
        DESTINATION usr/local/include)
install(TARGETS     sgp4 sgp4
        DESTINATION usr/local/lib)
#=============================================================================#
