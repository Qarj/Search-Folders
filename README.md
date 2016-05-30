# Search-Folders 0.04
Search windows network folders for files containing a string

## About:

Designed for searching a very large number of files and folders over a network connection.

Only for Windows.

## Usage:

```
Search-Folders.pl [target folder without trailing \] [extension to check] [search string]
```

The search string is a Perl regular expression, so escape special characters with a backslash.

## Examples:

Over a UNC:
```
Search-Folders.pl \\IRON\C$\webinject txt devenv
```

Escaping special characters:
```
Search-Folders.pl \\IRON\C$\webinject txt \.example\.com
```

With spaces in path or search text including sample output:
```
Search-Folders.pl "C:\Program Files" xml "critical state"

Search base path  : C:\Program Files
Search extension  : xml
Search target for : critical state

Built file list in 0.15 seconds

[1] C:\Program Files\Microsoft SQL Server\110\SDK\Assemblies\en\Microsoft.SqlServer.Management.Utility.xml:
      <summary>The operation is in a critical state.</summary>


[2] C:\Program Files\Microsoft SQL Server\110\SDK\Assemblies\en\Microsoft.SqlServer.SqlEnum.xml:
      <summary>The policy is in a critical state.</summary>


[3] C:\Program Files\Microsoft SQL Server\120\SDK\Assemblies\en\Microsoft.SqlServer.Management.Utility.xml:
      <summary>The operation is in a critical state.</summary>


[4] C:\Program Files\Microsoft SQL Server\120\SDK\Assemblies\en\Microsoft.SqlServer.SqlEnum.xml:
      <summary>The policy is in a critical state.</summary>


Searched files in 0.285 seconds

4 matches total in 4 files out of 1592 files searched

```

