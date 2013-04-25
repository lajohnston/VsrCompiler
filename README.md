Lemmings Paintball .VSR resource file compiler

This is used by the Lemmings Paintball level editor to handle the technicalities of the Lemball .VSR resource file, allowing you to pass it your own level files and have it replace the standard Lemmings Paintball levels with your own. The VSR compiler handles all the technical stuff such as file addresses and inner-directories, and fills empty level slots with blank levels to stop Lemmings Paintball from crashing. It is able to handle a variety of VSR versions that have been released over the years.

The standard Lemmings Paintball levels are all stored at the end of the VSR file, so we can simply truncate them from the end of the file and rebuild our own level directories without risking corrupting the other resources stored in the file.

I've set this up as a separate repo to LemballEdit as it will eventually be used by a separate Level Pack loader, which will allow you to load over people's levelpack files and compile them into your VSR file to play. This project will therefore act as its own entity that both the levelpack loader and the level editor can use as a dependency.

It's implemented in C#, using Visual Studio 2010 Express, .NET 2.0.