==========================
Building FTLSDK on Windows
==========================
testings
++++++++++++
Dependancies
++++++++++++
Visual Studio 2015 (Community is fine, older versions might work also but are untested)
Microsoft Build Tools (if you want to build outside of Visual Studio on command line: https://www.microsoft.com/en-us/download/details.aspx?id=48159)
cmake 3.5.2 (or greater: https://cmake.org/download/)

+++++++++++++++++++++
Visual Studio Project
+++++++++++++++++++++
mkdir build
cd build
cmake -G "Visual Studio 14 2015 Win64" ..

+++++++++++++++++++++++++
Building in Visual Studio
+++++++++++++++++++++++++
open build\libftl.sln in Visual Studio

+++++++++++++++++++++++++
Building in Command Prompt
+++++++++++++++++++++++++
cd build
msbuild /p:Configuration=Release,Platform=x64 ALL_BUILD.vcxproj
*compiled dll and ftp_app.exe will be in \Release\

++++++++++++
Test Files
++++++++++++
For your convenience there are test files available to stream:
sintel.h264: https://dl.dropboxusercontent.com/u/20701844/sintel.h264
sintel.opus: https://dl.dropboxusercontent.com/u/20701844/sintel.opus

++++++++++++++++++++++++
Running Test Application
++++++++++++++++++++++++
ftl_app.exe -i ingest-sea.beam.pro -s "<beam stream key>" -v c:\test\sintel.h264 -a c:\test\sintel.opus -f 24
