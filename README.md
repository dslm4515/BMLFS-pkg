# BMLFS-pkg
Beyond Musl Linux From Scratch - Build Recipes for  MLFS [Musl Linux From Source] using pkgtools

This is based on the works of Beyound Linux Fom Scratch (https://www.linuxfromscratch.org/blfs), Void Linux (https://voidlinux.org), Alpine Linux (https://alpinelinux.org), and Slackware

These build recipes allow to build "slack" packages (*.txz) for a MLFS, a Musl [based] Linux from Scratch system. Such system uses Musl as libc, LibreSSL for SSL support, S6+S6-rc for init system, and command-line tools from Slackware (pkgtools: makepkg, installpkg, removepkg).

WARNING: This is currently under development.

## Layout

<ul>
  <li> build-scripts -- Scripts to automatically build and install packages with pkgtools. </li>
  <li> files -- Files that may be optional or required for a package build </li>
  <li> patches -- Patches that fix known issues or to allow package to build/run with Musl as libc </li>
  <li> sources -- Packages sources that may be difficult to find or pre-patched </li>

</ul>

How to Use the Build Scripts

Build scripts assume pkgtools is installed as package manager and assumes the following directory tree:
```
 + -- [sources]
       |
       + -- [files]
       + -- [patches]
       + -- [scripts]
       + -- (source packages)
```
<ol>
	<li>Unpack package in `source` and `cd` into the unpacked source:
	`tar xf foo-4.3.tar.xz && cd foo-4.3` </li>
	<li>Run build script: `sh ../scripts/foo-4.3.build` </li>
</ol>
