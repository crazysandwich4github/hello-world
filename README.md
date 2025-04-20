# hello-world
my first repository


2025-4-22
1. how to build boost
核心问题：Boost 未针对你的 MSVC 版本（VS 2022）编译。
关键步骤：
用 toolset=msvc-14.3 重新编译 Boost。
在 CMake 中明确指定库路径和变体。
确保文件名包含 vc143 和 x64 标识。
解决方法： 
   .\b2 install   --prefix=C:\boost   toolset=msvc-14.3   address-model=64   variant=release,debug   link=static,shared   --with-system   --with-filesystem   --with-program_options   --with-regex
