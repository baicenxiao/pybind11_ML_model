# set(CMAKE_OSX_ARCHITECTURES "x86_64")

include_directories(
    /Users/baicenxiao/opt/anaconda3/envs/pybind_test/lib/python3.10/site-packages/pybind11/include
    /Library/Frameworks/Python.framework/Versions/3.10/include/python3.10
)
# link_directories(/Users/baicenxiao/opt/anaconda3/envs/pybind_test/lib)
aux_source_directory(. DIR_SRCS)
add_library(OtherModule SHARED ${DIR_SRCS})
# set_target_properties(OtherModule PROPERTIES SUFFIX ".pyd")
set_target_properties(OtherModule PROPERTIES
    OUTPUT_NAME "OtherModule.cpython-310-darwin.so"
)
set_target_properties(OtherModule PROPERTIES PREFIX "")
set_target_properties(OtherModule PROPERTIES SUFFIX "")
target_link_options(OtherModule PRIVATE -undefined dynamic_lookup)
# target_link_libraries(OtherModule)