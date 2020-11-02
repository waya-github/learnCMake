# CMakeList.txt: 顶层 CMake 项目文件，在此处执行全局配置
# 并包含子项目。
#
cmake_minimum_required (VERSION 3.8)

project ("CMakeProject")

FIND_PACKAGE(OpenGL)
FIND_PACKAGE(openThreads)
FIND_PACKAGE(osg)
FIND_PACKAGE(osgDB)
FIND_PACKAGE(osgUtil)
FIND_PACKAGE(osgGA)
FIND_PACKAGE(osgViewer)
FIND_PACKAGE(osgText)
FIND_PACKAGE(osgAnimation)
FIND_PACKAGE(osgShadow)
FIND_PACKAGE(osgTerrain)

include_directories(${OSGVIEWER_INCLUDE_DIR})



# 包含子项目。
add_subdirectory ("CMakeProjectDemo")
add_subdirectory ("APP")
add_subdirectory ("testMatrix")

 