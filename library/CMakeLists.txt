# For more information about using CMake with Android Studio, read the
# documentation: https://d.android.com/studio/projects/add-native-code.html

# Sets the minimum version of CMake required to build the native library.

cmake_minimum_required(VERSION 3.4.1)

#set *.h source path
include_directories(src/main/cpp/lamemp3)


#set *.so files output path，please add this before add_library
set(jnilibs "${CMAKE_SOURCE_DIR}/src/main/jniLibs")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${jnilibs}/${ANDROID_ABI})

ADD_SUBDIRECTORY(${CMAKE_SOURCE_DIR}/src/main/cpp)