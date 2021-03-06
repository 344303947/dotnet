# Microsoft.NETCore.UniversalWindowsPlatform NuGet Package Releases

You can learn about Microsoft.NETCore.UniversalWindowsPlatform [releases](#releases), below. See [resources](#resources) for additional information.

## Release Notes

You can see what was included in each Microsoft.NETCore.UniversalWindowsPlatform release.

### 5.3.4 (August 4, 2017)
When using Visual Studio this package requires Visual Studio 2017 or later.

- Corrected an issue where System.Threading.Thread.MemoryBarrier was implemented as no-op on x86 release builds.

### 5.3.3 (April 24, 2017)
When using Visual Studio this package requires Visual Studio 2017 or later.

- Corrected an [issue](http://stackoverflow.com/questions/43530071/how-to-fix-app-submission-error-of-1300) for projects that have Visual Studio configuration values that are not "DEBUG" or "RELEASE" that causes Windows Store submission failure (error code 1300). For example, most Unity apps use a configuration named "Master". 

### 5.3.2 (April 6, 2017)
When using Visual Studio this package requires Visual Studio 2017 or later.

- Fixed an issue that caused MAKEPRI build warnings to be emitted when building app packages for UWP projects.

### 5.3.1 (March 7, 2017)
When using Visual Studio this package requires Visual Studio 2017 or later.

- Fixed an [issue](https://github.com/dotnet/corefx/issues/10374) that caused DataContractJsonSerializer to fail to serialize any [DataContract] type whose default constructor is not public.
- Fixed a regression in 5.3.0 where [4 Libraries were accidently no longer referenced by default](https://github.com/dotnet/corefx/issues/10338)
    - System.Collections.NonGeneric
    - System.Collections.Specialized
    - System.Threading.Overlapped
    - System.Xml.XmlDocument

### 5.3.0 (January 27, 2017)
When using Visual Studio this package requires Visual Studio 2017 or later. You can read more about these changes in our announcement blog [post](https://blogs.msdn.microsoft.com/dotnet/2017/01/30/announcing-net-core-net-native-and-nuget-updates-in-vs-2017-rc/).

- Added NuGet support for Visual Studio 2017 or later.
- Added hardware-accelerated support for System.Numerics.Vectors. 
- Added the ability to inspect static fields that contain the ThreadStatic attribute.
- Added x64 support for Shared Library package with profile-guided optimizations which reduces the package size and improves startup time for x64 native apps. This change brings x64 to parity with x86 and ARM32.
- Integrated .NET Native garbage collector with Windows Runtime MemoryManager API to properly calculate memory load factor in UWP applications.
- Reduced compile times for applications that contain large and/or complex methods by ~25% in certain scenarios.
- Increased performance improvements in reverse p/invoke (up to 400%) and when accessing Windows Runtime objects (up to 135% in certain scenarios).
- Improvements to the relfection stack and metadata formats which result in up to 30% performance increase in some scenarios.
- Improvements to delegate invocation that reduce code size and give up to 7% faster performance.
- General code quality improvements which improve start up times, better steady-state performance, less memory usage and smaller app size.
- Resolved an issue that sometimes resulted in a 1300 error when submitting a package to the store after upgrading / cherry-picking .NET Core assembly packages.
- resolved an issue that caused a memory leak when interacting with certain Windows Runtime objects in a different process.
- significantly reduced global lock contention when accessing Windows Runtime objects from multiple threads.
- Resolved an issue that resulted in queries not executing properly in Entity Framework when enabling .NET Native. ([GitHub #6381](https://github.com/aspnet/EntityFramework/issues/6381))
- Resolved an issue with System.Linq.Expressions that resulted in unsupressable error messages. ([GitHub #5088](https://github.com/dotnet/corefx/issues/5088))
- .NET Native will now show a warning if you have a native DLL in a different CPU architecture than the application being built. This is a common mistake that results in the application not being able to launch.

#### Known issues

- .NET native does not currently support portable PDBs. When debugging managed components with portable PDBs in application compiled with .NET native, you may have trouble setting breakpoints, stepping in, and/or inspecting variables of related types in those components. You can delete the files from the local package directory (users\userName.nuget\packages) to workaround the warning. This change was also made in the servicing update for .NET Native 1.4 in the latest update to Visual Studio 2017 RC. Earlier versions of .NET native may incorrectly throw OutOfMemoryException and crash during build when consuming portable PDBs.

### 5.2.3 (March 7, 2017)
When using Visual Studio this package requires Visual Studio 2015 Update 3 or later.

- Fixed an [issue](https://github.com/dotnet/corefx/issues/10374) that caused DataContractJsonSerializer to fail to serialize any [DataContract] type whose default constructor is not public.
- Fixed a regression in 5.2.2 where [4 Libraries were accidently no longer referenced by default](https://github.com/dotnet/corefx/issues/10338)
    - System.Collections.NonGeneric
    - System.Collections.Specialized
    - System.Threading.Overlapped
    - System.Xml.XmlDocument

### 5.2.2 (July 14, 2016)
When using Visual Studio this package requires Visual Studio 2015 Update 3 or later. You can read more about these changes in the Visual Studio 2015 Update 3 blog [post](https://www.visualstudio.com/en-us/news/releasenotes/vs2015-update3-vs).

- Fixed several customer reported bugs.
- Improved release build compilation times of large applications.
- Improved runtime performance for XAML applications and Unity games. 

## Resources

- [Microsoft.NETCore.UniversalWindowsPlatform NuGet Package Details](https://www.nuget.org/packages/Microsoft.NETCore.UniversalWindowsPlatform)
- [Windows Dev Center](https://developer.microsoft.com/en-us/windows/apps/getstarted)
- [Downloads and tools for Windows 10](https://developer.microsoft.com/en-us/windows/downloads)
