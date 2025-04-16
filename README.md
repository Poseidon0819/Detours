# Microsoft Research Detours Package

Detours is a software package for monitoring and instrumenting API calls on Windows. Detours
has been used by many ISVs and  is also  used by product teams at Microsoft. Detours is now available under
a standard open source  license ([MIT](https://github.com/microsoft/Detours/blob/master/LICENSE.md)).  This simplifies licensing for programmers using Detours
and allows the community to support Detours using open source tools and processes.

Detours is compatible with the Windows NT family of 
operating systems: Windows NT, Windows XP, Windows Server 2003, Windows 7,
Windows 8, and Windows 10.  It cannot be used by Windows Store apps
because Detours requires APIs not available to those applications. 
This repo contains the source code for version 4.0.1 of Detours.

For technical documentation on Detours, see the [Detours Wiki](https://github.com/microsoft/Detours/wiki).
For directions on how to build and run samples, see the
samples [README.txt](https://github.com/Microsoft/Detours/blob/master/samples/README.TXT) file.

## Contributing

The [`Detours`](https://github.com/microsoft/detours) repository is where development is done.
Here are some ways you can participate in the project:

* [Answer questions](https://github.com/microsoft/detours/issues) about using Detours.
* [Improve the Wiki](https://github.com/microsoft/detours/wiki).
* [Submit bugs](https://github.com/microsoft/detours/issues) and help us verify fixes and changes as they are checked in.
* Review [source code changes](https://github.com/microsoft/detours/pulls).

Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that
you have the right to, and actually do, grant us the rights to use your contribution.
For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Issues, questions, and feedback

* Open an issue on [GitHub Issues](https://github.com/Microsoft/detours/issues).

## Mailing list for announcements

The detours-announce mailing list is a low-traffic email list for important announcements 
about the project, such as the availability of new versions of Detours.  To join it, send 
an email to listserv@lists.research.microsoft.com with a 
message body containing only the text SUBSCRIBE DETOURS-ANNOUNCE.
To leave it, send an email to listserv@lists.research.microsoft.com with a 
message body containing only the text UNSUBSCRIBE DETOURS-ANNOUNCE.

## Compiling the source code 

* (Optional) Make it Work in Any Terminal ( Visual Studio 2022 compile-toolset: windows 10)

    - set INCLUDE=%INCLUDE%;C:\Program Files (x86)\Windows Kits\10\Include\10.0.19041.0\um;C:\Program Files (x86)\Windows Kits\10\Include\10.0.19041.0\ucrt;C:\Program Files (x86)\Windows Kits\10\Include\10.0.19041.0\shared

    - call "C:\Program Files\Microsoft Visual Studio\2022\Professional\VC\Auxiliary\Build\vcvars64.bat"

    move to src folder

	- cd /d D:\WorkSpace\Detours-main\src

    Then run 
    
    - nmake 
    
    command from there.


* (Optional) Make it Work in Any Terminal ( Visual Studio 2015 compile-toolset: windows xp )

    install Visual Studio 2015 vs_community.exe 

    make sure these are selected:

    * Visual C++

    * Common Tools for Visual C++ 2015

    Download Windows 10 SDk from this url : https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/index-legacy

    setup.exe download directly url : https://go.microsoft.com/fwlink/p/?LinkID=698771

    Add Visual C++ tools and Windows SDK paths manually:
        
    Open Command Prompt, and run this block:

    - set PATH=C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\bin;%PATH%

    - set INCLUDE=C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\include;C:\Program Files (x86)\Windows Kits\10\Include\10.0.10586.0\ucrt;C:\Program Files (x86)\Windows Kits\10\Include\10.0.10586.0\um;C:\Program Files (x86)\Windows Kits\10\Include\10.0.10586.0\shared;

    - set LIB=C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\lib;C:\Program Files (x86)\Windows Kits\10\Lib\10.0.10586.0\ucrt\x86;C:\Program Files (x86)\Windows Kits\10\Lib\10.0.10586.0\um\x86

    Confirm cl.exe and nmake.exe are available:

    - where cl

    - where nmake

    move to src folder

	- cd /d D:\WorkSpace\Detours\src

    Then run 
    
    - nmake 
    
    command from there.    

## Set environment ( use .h & .lib ) 

   https://www.artstation.com/blogs/rendord/WBB6q/adding-libraries-to-your-c-project-using-visual-studio

## Document:
================
This document describes the installation and usage of this version of the
Detours package.  In particular, it provides an updated API table.

Complete documentation for the Detours package, including a detailed API
reference can be found in the Detours.chm file.   

## License

Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the [MIT](LICENSE.md) License.
