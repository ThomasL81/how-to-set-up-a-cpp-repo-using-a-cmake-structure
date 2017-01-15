cmake_minimum_required( VERSION 3.1.3 )

# Tell CMake we will be using are cmake subdirectory aswell for loading modules
set( CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake )

# Platform definitions. We use Linux and Windows, so let's determine them before-hand
if( UNIX AND NOT APPLE )
    if( CMAKE_SYSTEM_NAME MATCHES ".*Linux" )
        set( LINUX TRUE )    
    else()
        message( FATAL_ERROR "Unsupported system" )
    endif()
elseif( WIN32 )
    set( WINDOWS TRUE )
else()
    message( FATAL_ERROR "Unsupported system" )
endif()

# On Linux, make sure Debug mode actually sets the DEBUG definition.
if( LINUX )
    if( CMAKE_BUILD_TYPE STREQUAL "Debug" )
        add_definitions( -D_DEBUG=1 -DDEBUG=1 )
    endif()
endif( LINUX )

# Add the nested project subdirectories. Make sure CMake can find CMakeLists.txt files there
add_subdirectory( MyStaticLib )
add_subdirectory( MyHeaderOnlyLib )
add_subdirectory( MyApp )