cmake_minimum_required(VERSION 3.4.1)


add_library(
        animated-webp
        SHARED

        src/main/cpp/BitmapDecoderJNI.cpp
        src/main/cpp/FrameSequence.cpp
        src/main/cpp/FrameSequence_gif.cpp
        src/main/cpp/FrameSequence_webp.cpp
        src/main/cpp/FrameSequenceJNI.cpp
        src/main/cpp/JNIHelpers.cpp
        src/main/cpp/Registry.cpp
        src/main/cpp/Stream.cpp
)

include_directories(src/main/cpp/include)

find_library(
              log-lib
              log )

target_link_libraries(
        animated-webp
                     ${log-lib} )