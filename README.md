# xdg-base-directory
.NET class for [freedesktop XDG base directories specification](http://standards.freedesktop.org/basedir-spec/basedir-spec-0.8.html)

Install with [nuget](https://www.nuget.org/packages/Freedesktop.Xdg.BaseDirectory.Sources):

    Install-Package Freedesktop.Xdg.BaseDirectory.Sources

Use it to find files:

    using System.IO;
    using MyNamespace.Freedesktop.Xdg;
    
    var myFileName = BaseDirectory.FindDataFile (Path.Combine ("my-package", "data.file"));
    if (myFileName == null) {
      throw new FileNotFoundException ("Could not find data.file in XDG data directories");
    }
