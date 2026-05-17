Medo.X11Clipboard
=================

> ### Deprecated
> Use [PTClipboard][https://www.nuget.org/packages/Medo.PTClipboard/] instead.
> Source available at [GitHub](http://github.com/medo64/Medo.PTClipboard).

X11Clipboard library is designed for applications that need to interact with the
X11 clipboard system. This library provides essential functions for getting and
setting UTF-8 text content for both X11's primary selection and clipboard. This
makes it ideal for applications that require straightforward clipboard
interactions without the overhead of more comprehensive libraries.

Features:
* Supports both primary selection and clipboard GetText and SetText operations.
* .NET 8 AOT support

You can find packaged library at [NuGet][nuget_x11clipboard].


## Usage

To write and read X11 primary selection (aka, middle-click clipboard):
```csharp
using System;
using Medo.X11;

X11Clipboard.Primary.SetText("My text.");
Console.WriteLine(X11Clipboard.Primary.GetText());
```

To write and read normal clipboard:
```csharp
using System;
using Medo.X11;

X11Clipboard.Clipboard.SetText("My text.");
Console.WriteLine(X11Clipboard.Clipboard.GetText());
```


[nuget_x11clipboard]: https://www.nuget.org/packages/Medo.X11Clipboard/
