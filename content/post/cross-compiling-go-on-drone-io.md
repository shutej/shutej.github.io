+++
date = "2014-12-07"
author = "Jeremy Shute"
title = "Cross-compiling Go on drone.io"
+++

The folks over at [drone.io](https://drone.io) offer free builds for open
source projects.  However, currently they only support Go 1.2.  This method
allows you to to cross-compile artifacts with a more recent version of Go.

Copy **commands.sh** and **environment-variables.sh** into the **Settings / Build &
Test** tab and copy **artifacts.sh** into the **Settings / Artifacts** tab.  Then,
adjust the **GOX_OSARCH** environment variable to your liking.

{{% gist "shutej/ff2610b1b692c7726f7c" %}}

Incidentally, I specified that my project is **C / C++** for the simple reason
that gox recompiles the build toolchain.
