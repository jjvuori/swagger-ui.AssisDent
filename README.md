# General

This repository is fork of https://github.com/swagger-api/swagger-ui. 

AssisDent uses old version of the swagger-ui, and the purpose of this fork is to provide that old UI as NuGet package.

The old version of the UI is v 2.1.3 (tag v.2.1.3 and commit 8bc259558ba7774f814d7426c7794f27c144d2be). This commit has been chosen as the base for the main branch, and all changes should go to main branch. There is also master branch that contains the newest version of the swagger-ui (which is not used by AssisDent).

# Package

## Info
To use the package, add following code to *.csproj* file.

```xml
<ItemGroup>
  <PackageReference Include="Entteri.Swagger.UI" Version="1.0.2" />
</ItemGroup>
```

## Publish
See general instructions for publishing Entteri NuGet packages: https://github.com/jjvuori/ac-dependency-binaries#publishing-nuget-packages

Publish nuget (from Windows command line):
```
cd nuget
dotnet pack Entteri.Swagger.UI.csproj
cd Bin\Release
dotnet nuget push --source "Entteri" --api-key none Entteri.Swagger.UI.1.0.2.nupkg
cd ..\..\..
```
