# CMakeList.txt: CMakeProject 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.8)

# 将源代码添加到此项目的可执行文件。
add_executable (testMatrix "testMatrix.cpp" "testMatrix.h")

TARGET_LINK_LIBRARIES(
		testMatrix
		${OPENGL_LIBRARIES}
		optimized ${OPENTHREADS_LIBRARY}	debug ${OPENTHREADS_LIBRARY_DEBUG}
		optimized ${OSG_LIBRARY}			debug ${OSG_LIBRARY_DEBUG}
		optimized ${OSGDB_LIBRARY}			debug ${OSGDB_LIBRARY_DEBUG}
		optimized ${OSGUTIL_LIBRARY}		debug ${OSGUTIL_LIBRARY_DEBUG}
		optimized ${OSGGA_LIBRARY}			debug ${OSGGA_LIBRARY_DEBUG}
		optimized ${OSGVIEWER_LIBRARY}		debug ${OSGVIEWER_LIBRARY_DEBUG}
		optimized ${OSGTEXT_LIBRARY}		debug ${OSGTEXT_LIBRARY_DEBUG}
		optimized ${OSGANIMATION_LIBRARY}	debug ${OSGANIMATION_LIBRARY_DEBUG}
		optimized ${OSGSHADOW_LIBRARY}		debug ${OSGSHADOW_LIBRARY_DEBUG}
		optimized ${OSGTERRAIN_LIBRARY}		debug ${OSGTERRAIN_LIBRARY_DEBUG}

)

# TODO: 如有需要，请添加测试并安装目标。


