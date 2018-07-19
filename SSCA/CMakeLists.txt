cmake_minimum_required(VERSION 3.7)
project(SSCA)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV REQUIRED)

set(SOURCE_FILES
    ctmf/ctmf.c
    ctmf/ctmf.h
    CAFilter/BFCA.cpp
    CAFilter/BFCA.h
    CAFilter/BilateralFilter.cpp
    CAFilter/BilateralFilter.h
    CAFilter/BoxCA.cpp
    CAFilter/BoxCA.h
    CAFilter/GFCA.cpp
    CAFilter/GFCA.h
    CAFilter/GuidedFilter.cpp
    CAFilter/GuidedFilter.h
    CANLC/NLCCA.cpp
    CANLC/NLCCA.h
    CANLC/qx_basic.cpp
    CANLC/qx_basic.h
    CANLC/qx_mst_kruskals_image.cpp
    CANLC/qx_mst_kruskals_image.h
    CANLC/qx_nonlocal_cost_aggregation.cpp
    CANLC/qx_nonlocal_cost_aggregation.h
    CANLC/qx_tree_filter.cpp
    CANLC/qx_tree_filter.h
    CAST/disjoint-set.h
    CAST/segment-graph.h
    CAST/SegmentTree.cpp
    CAST/SegmentTree.h
    CAST/STCA.cpp
    CAST/STCA.h
    CAST/StereoDisparity.cpp
    CAST/StereoDisparity.h
    CAST/StereoHelper.cpp
    CAST/StereoHelper.h
    CAST/Toolkit.cpp
    CAST/Toolkit.h
    CC/CenCC.cpp
    CC/CenCC.h
    CC/CGCC.cpp
    CC/CGCC.h
    CC/GrdCC.cpp
    CC/GrdCC.h
    PPSG/convolve.h
    PPSG/disjoint-set.h
    PPSG/filter.h
    PPSG/image.h
    PPSG/imconv.h
    PPSG/imutil.h
    PPSG/misc.h
    PPSG/pnmfile.h
    PPSG/segment-graph.h
    PPSG/segment-image.h
    PPSG/SGPP.cpp
    PPSG/SGPP.h
    PPWM/WMPP.cpp
    PPWM/WMPP.h
    CAMethod.h
    CCMethod.h
    CommFunc.h
    GetMehod.h
    main.cpp
    PPMethod.h
    SSCA.cpp
    SSCA.h)

add_executable(SSCA ${SOURCE_FILES})

target_link_libraries(SSCA ${OpenCV_LIBRARIES})
