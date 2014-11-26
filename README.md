## Motivation

One day, I decided to develop using the wxWidget library and Code::Blocks as IDE. My choice was made because of the wxSmith plugin that allows you to draw your wxWidget UI using a simple and well-designed GUI interface.

I was playing around with the different widget when I thought it would be nice to make some graphics (I needed for my project). I found the wxWdiget library and was quite happy to see the wxSmithPlot plugin. Unfortunately, the plugin was not maintained anymore (even if it's always in the Code::Blocks source tree). By the way, the wxMathPlot library is not really updated often as well.

During my free time, I managed to make the plugin working again. The result is this new repo that contains a working wxSmithPlot under Linux/Windows. I also started a wxMathPlot repo for adding a few stuff in it like the mpMarker class.

Feel free to fork/pull/report problems :-)

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

For more information like compiling the plugin for a working Code::Blocks installation on Debian, see the [wxSmithPlot README](./src/plugins/contrib/wxSmithPlot/README).

## Licenses

[Code::Blocks License](./LICENSE_CodeBlocks)
[wxMathPlot License](./LICENSE_wxMathPlot)



