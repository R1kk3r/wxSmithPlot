## Synopsis

At the top of the file there should be a short introduction and/ or overview that explains **what** the project is. This description should match descriptions added for package managers (Gemspec, package.json, etc.)

## Motivation

A short description of the motivation behind the creation and maintenance of the project. This should explain **why** the project exists.

## Installation

This will teach you how to install the wxSmithPlot plugin into the default Code::Blocks source tree.

#### Howto enable wxSmithPlot plugin

Clone the repo. The repo structure follow the Code::Blocks source tree structure. So you just have to apply the patch regarding the corresponding depth and name where there are.

* __./__

 Apply both patch "__acinclude.m4.diff__" and "__configure.ac.diff__".
This will add wxSmithPlot to the build chain of contrib plugins.

* __./src/plugins/contrib__

 Apply the patch "__Makefile.am.diff__".
This will add wxSmithPlot to the build chain of contrib plugins.

* __./src/plugins/contrib/wxSmithPlot__

 Replace the whole Code::Blocks's directory (wxSmithPlot) with the new one given in this repo.



#### Compile Code::Blocks with the new plugins

Btw, to compile Code::Blocks with the contrib plugins:

```
./bootstrap
```

```
./configure --with-contrib-plugins=all
```

```
make && make install
```

## License

A short snippet describing the license (MIT, Apache, etc.)


