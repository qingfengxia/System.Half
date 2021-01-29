
### What is half precision floating point number (binary16)

see wiki: https://en.wikipedia.org/wiki/Half-precision_floating-point_format

Widely used in game, and deep learning. Some GPU has hardware support for such type.

### Author and license

This code is just the host of the gist by:  Author Ladislav Lang (2009), Joannes Vermorel (2017)

https://gist.github.com/vermorel/1d5c0212752b3e611faf84771ad4ff0d

License header on the gist is kind of public domain, in order to have some license can be searched, it is listed as MIT

> The code is free to use for any reason without any restrictions


### dotnet 5 (Nov 2020) has built in Half type

dotnet 5 (Nov 2020) has built in Half type, so this file is not needed
https://docs.microsoft.com/en-us/dotnet/api/system.bitconverter?view=net-5.0

For historical interest, I still want to use it. so I make a repo from this gist. If needed could make a nuget package to make life easier



### Notes on Conversion

For the moment, no plan to make it API identical to dotnet 5; that may involved modifying other system source code. 

C# `BitConverter`            Endianness of dotnet

`Covnert.ToUint16()`

https://stackoverflow.com/questions/59728656/c-sharp-16-bit-float-conversions


### Test with dotnet core 3.1

To target on different dotnet framework, may manually edit Half.csproj file

`dotnet build Half  --configuration Release`
`dotnet pack Half --configuration Release`

`dotnet build Half.Tests`
`dotnet test Half.Tests`

all past

### Package and CI

https://devblogs.microsoft.com/dotnet/continuous-integration-workflow-template-for-net-core-desktop-apps-with-github-actions/

todo: