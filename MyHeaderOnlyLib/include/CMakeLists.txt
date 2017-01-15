target_sources( ${PROJECT_NAME} INTERFACE
        # ${CMAKE_CURRENT_LIST_DIR}/Vulkanic.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/internals/vkcHandleWrapper.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/internals/vkcLoader.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/vkcCore.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/vkcEnums.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/vkcFunctionWrappers.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/vkcHandles.hpp
        # ${CMAKE_CURRENT_LIST_DIR}/vkc/vkcHelpers.hpp
)

target_include_directories( ${PROJECT_NAME} INTERFACE "${CMAKE_CURRENT_LIST_DIR}" )