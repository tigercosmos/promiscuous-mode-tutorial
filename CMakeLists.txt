cmake_minimum_required(VERSION 3.1)
project(MyPcapPlusPlusProject)

# Set C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)

# Find PcapPlusPlus library
find_package(PcapPlusPlus REQUIRED)

# Add your project source files
add_executable(hello_world hello_world.cpp)

# Link against PcapPlusPlus library
target_link_libraries(hello_world PcapPlusPlus::Packet++ PcapPlusPlus::Pcap++ PcapPlusPlus::Common++)

# Add your project source files
add_executable(capture capture.cpp)

# Link against PcapPlusPlus library
target_link_libraries(capture PcapPlusPlus::Packet++ PcapPlusPlus::Pcap++ PcapPlusPlus::Common++)