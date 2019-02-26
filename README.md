# EtAlii.xTechnology.Grpc.Tools
Nuget package that allows easy Grpc and Protobuf management from within C# projects.

Feel free to share your thoughts and/or assist by creating some wonderfull pull requests.

Current limitations / things to know:
- Currently hardwired to use the Windows protoc.exe. Therefore it only works on Windows development machines or build agents.
- The files are created in the temp folder and cleaned up afterwards. A build that is cancelled during the GRPC code creation might leave artefacts in there.
- The C# code generation is wired into the MSBuild process right before the BeforeBuild target is being executed (BeforeTargets="BeforeBuild").
- Proto includes from the Google.Protobuf.Tools NuGet package (\tools\google\protobuf\) are taken into account but are somehow incompatible with Jetbrains Resharper/Rider.