zlibpatched
===========

Nick Nussbaum  10/24/2014

a copy of zlib 1.28.0 from zlib.net patched to run in Visual Studio 2013
This repository exists because the patch doesn't seem to work on some systems.

The patch is include in the file zlibpatch.zip
The following steps were done to make this version in a build directory
	
	(a)Get the zlib 1.28.0 file from   http://zlib.net/zlib128.zip
	(b) unzip zlib-1.2.8.zip into the build directory

	use contrib/vstudio/vc11 since there is no contrib/vstudio/vc12 as yet
	
	(c)Get the GnuWin32 Patch Utility http://gnuwin32.sourceforge.net/packages/patch.htm patch.exe
	and simply put it in the build directory
	(d)Unzip the zlibpatch.zip file and place the contained zlibpatch.txt file in the build directory 



	(e) From a dos command shell run as administrator and move to the build directory
	
	  patch --dry-run -p0 --directory=zlib-1.2.8 --input=../zlibpatch.txt -F3
		check output messages looks good then
	  patch  -p0 --directory=zlib-1.2.8 --input=../zlibpatch.txt -F3
	  
	  
	  This software is available under the zlib license which is included in the zlib directory.

