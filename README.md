# .Net-MAUI-Prototype

## Installing with .NET MAUI Check Tool

Install: `dotnet tool install -g redth.net.maui.check` 
and then
Run: `maui-check`

## iOS and Android workloads needed for dotnet to build platform projects

Android:

* Windows: [Microsoft.NET.Workload.Android.11.0.200-preview.3.196.msi](https://dl.internalx.com/vsts-devdiv/Xamarin.Android/public/net6/4624420/6.0.1xx-preview3/7d6cd1cde4182d7db2cfc5d0b55364c972b6d34f/Microsoft.NET.Workload.Android.11.0.200.196.msi)
* macOS: [Microsoft.NET.Workload.Android-11.0.200-preview.3.196.pkg](https://dl.internalx.com/vsts-devdiv/Xamarin.Android/public/net6/4624420/6.0.1xx-preview3/7d6cd1cde4182d7db2cfc5d0b55364c972b6d34f/Microsoft.NET.Workload.Android-11.0.200-preview.3.196.pkg)

iOS:

* Windows: [Microsoft.NET.Workload.iOS.14.4.100-preview.3.1326.msi](https://bosstoragemirror.azureedge.net/wrench/6.0.1xx-preview3/f68d4d9c2a342daf9eaad364ccbe252e009d3901/4623693/package/Microsoft.NET.Workload.iOS.14.4.100-preview.3.1326.msi)
* macOS: [Microsoft.iOS.Bundle.14.4.100-preview.3.1326.pkg](https://bosstoragemirror.azureedge.net/wrench/6.0.1xx-preview3/f68d4d9c2a342daf9eaad364ccbe252e009d3901/4623693/package/notarized/Microsoft.iOS.Bundle.14.4.100-preview.3.1326.pkg)

Prerequisites:

* You will need the Android SDK installed as well as `Android SDK Platform 30`.

For example, to build the Android project:

    dotnet build HelloAndroid

You can launch the Android project to an attached emulator or device via:

    dotnet build HelloAndroid -t:Run

## iOS

Prerequisites:

* Xcode 12.4 or higher than this

To build the iOS project:

    dotnet build HelloiOS

To launch the iOS project on a simulator:

    dotnet build HelloiOS -t:Run

## .NET MAUI

To launch the .NET MAUI project, you will need to specify a `$(TargetFramework)` via the `-f` switch:

    dotnet build HelloMaui -t:Run -f net6.0-android
    dotnet build HelloMaui -t:Run -f net6.0-ios
    dotnet build HelloMaui -t:Run -f net6.0-maccatalyst
