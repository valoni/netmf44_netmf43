As some of you might have noticed, I have already published a .NET Micro Framework changes to make it running in Visual Studio 2017 on GitHub in June 2017 
- see the VS15.3 branch. So you can either compile your own installer following these steps:

make sure your favorite Visual Studio instance is of version 15.3 or newer, and has the Desktop development with C++ workload installed, as well as VC++ tools, 
that individual component is called VC++ 2017 version 15.8 v14.15 latest v141 tools in version 15.8;

clone the https://github.com/miloush/netmf-interpreter.git repository and checkout the VS15.3 branch;
install tools, CMSIS and the cryptographic libraries as explained on GitHubu;

run the Developer Command Prompt for VS 2017 — unlike in previous versions, 
the compilation has to be started from a developer command prompt of a particular Visual Studio instance, otherwise it will end up with ERROR: Visual Studio 2017 SDK 
(VSSDK) was not detected, this SDK is required to build the .NET Micro Framework SDK source code;
execute build_sdk.cmd in the command prompt.

Should the compilation be succesful, you can find the installer at %SPOCLIENT%\BuildOutput\public\Release\Server\msm\MicroFrameworkSDK.MSI 
and the Visual Studio extension at %SPOCLIENT%\BuildOutput\public\Release\Server\dll\NetmfVS15.vsix (you need to install both of these).


ReadME

Copy all those folder from
C:\Program Files (x86)\MSBuild\Microsoft\.NET Micro Framework

to 
C:\Program Files (X86)\Microsoft Visual Studio\2017\Enterprise\MSBuild\Microsoft\.NET Micro Framework

or 
C:\Program Files (X86)\Microsoft Visual Studio\2019\Enterprise\MSBuild\Microsoft\.NET Micro Framework