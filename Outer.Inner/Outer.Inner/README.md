This project is to verify a bug in Rider https://youtrack.jetbrains.com/issue/RIDER-2240 .


Steps:

1. Create a dotnet core project
1. Set the `RootNamespace` in `Outer.Inner.xproj` to `Outer` (By manually editing the `xproj` file).
1. Create a directory `SubDir` in the project.
1. Add a class `Sample.cs` in directory `SubDir`.

Expected:

Rider should give NO warning for the namespace `Outer.SubDir` in `Sample.cs`.

Actual:
Rider warns `Namespace does not correspond to file location, should be 'Outer.Inner.Inner'`
