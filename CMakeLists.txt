cmake_minimum_required(VERSION 3.5)

project(ImageGuidedRoboticsSlicelet)

#-----------------------------------------------------------------------------
# Extension meta-information
# set(EXTENSION_HOMEPAGE "http://slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/IGRS")
# set(EXTENSION_CATEGORY "Examples")
set(EXTENSION_CONTRIBUTORS "Renjie Zhu (arcLAB @ UCSD)")
set(EXTENSION_DESCRIPTION "slicelet for image guided robotics for lung biopsy (slicelets)")
# set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/SimpleWorkflows.png")
# set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/SimpleWorkflows/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a space separated string, a list or 'NA' if any

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(QuickSegment)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})