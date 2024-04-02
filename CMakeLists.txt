cmake_minimum_required(VERSION 3.27)
project(imgui)
set(CMAKE_CXX_STANDARD 20)

add_executable(imgui-test
				examples/example_win32_directx11/main.cpp
				backends/imgui_impl_dx11.cpp
				backends/imgui_impl_win32.cpp
				imgui.cpp
				imgui_widgets.cpp
				imgui_tables.cpp
				imgui_draw.cpp
				imgui_demo.cpp
)

target_include_directories(imgui-test PUBLIC .)
target_include_directories(imgui-test PUBLIC backends)

target_link_libraries(imgui-test PUBLIC d3dcompiler d3d11 dxgi gdi32)

