IdentityAdmin
============================

**current status: beta**

## Overview ##

IdentityAdmin is a tool for developers and/or administrators to manage the clients and scopes of their applications. This includes creating clients/scopes, editing client/scopes and deleting clients/scopes. 

## Hot to build and publish package IdentityServer3.Admin.Iflo

 1. Compile with Visual Studio
 
 Compiled files are in ./build
 
 1. Run `ILmerge` to get the `IdentityServer3.Admin.dll`
 
````
# delete folder, otherise IL merge will fail

`distribution`

# Import PSake module

Import-Module .\source\packages\psake.4.4.1\tools\psake.psm1


# run IL merge task

Invoke-psake ILMerge

`distribution\lib\net45\IdentityServer3.Admin.dll` is the built dll

# Create nuget package

 
`Invoke-psake CreateIfloNuGetPackage`

Package will be created in `distribution\IdentityServer3.Admin.Iflo.1.0.0.nupkg`

