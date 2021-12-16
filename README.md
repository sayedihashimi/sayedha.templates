Some templates that Sayed has authored.

This repo contains a few templates that can help you create your own tempaltes for `dotnet new` as well as a template to create a new `dotnet` cli tool. 
For info on how to create your own dotnet templates go to https://aka.ms/netcore-templates.

To install this template pack, run the following command in a terminal.

```bash
dotnet new --install sayedha.templates
```

## Templates

### templatejson

To create the `template.json` file you can use the `templatejson` template. Create a new `template.json` file with the command below after installing the template pack.

```bash
dotnet new templatejson
```

This will create a `template.json` file in the current directory.

### templatepackcsproj

When creating templates, you'll need to pack them into a NuGet package to distribute them. You can learn more about this at 
[Packing a template into a NuGet package (nupkg file)](https://docs.microsoft.com/en-us/dotnet/core/tools/custom-templates#packing-a-template-into-a-nuget-package-nupkg-file).
To create the `csproj` file that can be used to pack your template pack execute the command below.

```bash
dotnet new templatepackcsproj
```

This will create a file named `template.csproj` in the current directory. You'll need to customize the content of the file to suit your needs.

### idehostjson

In most cases template authors don't need to tweak settings for the IDE, but in the cases that it's needed, you can do that with an `ide.host.json` file. To create
that file execute the command below.

```bash
dotnet new idehostjson
```

This will create an `ide.host.json` file in the current directory.

### clitool

This is a project template for a dotnet new tool that uses [System.CommandLine](https://github.com/dotnet/command-line-api). This template is setup as a tool that has a single sub-command.
You can easily add more commands as needed.

To create a project from this template, execute the command below.

```bash
dotnet new clitool
```

This template has some options, to explore what's available, invoke the command specific help with.

```bash
dotnet new clitool -h
```

