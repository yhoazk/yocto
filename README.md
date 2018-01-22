# Yocto


## Kernel Lab


## [Yocto Mega-Manual](http://www.yoctoproject.org/docs/2.4.1/mega-manual/mega-manual.html)

The link in the title is for the version 2.4.1, for newer versions see: [Link](http://www.yoctoproject.org/docs/2.4.1/mega-manual/mega-manual.html)




## [Useful BitBake Commands](https://docs.atsgarage.com/tips/useful-bitbake-commands.html)





- Clean the build environment:
	- `bitbake -c cleanall [package]`
- View the actual build environment bitbake will execute:
	- `bitbake -e [package] > env.log`
- Launch the bitbake devshell for a package:
	- `bitbake -c devshell|shell [package]`
- Launch the dependency explorer for a package:
	- `bitbake [package] -g -u depexp`
- Show the layers currenlty in the build
	- `bitbake-layers show-layers`
- Show all available recipes
	- `bitbake-layers show-recipes`
- List all packages that will be build in an image/package
	- `bitbake -g [package] && cat pn-depends.dot | grep -v -e '-native' | \
	  grep -v digraph | grep -v -e '-image' | awk '{print $1}' | sort | uniq`
- Save verbose build log
	- `bitbake -v [package] 2>&1 | tee build.log`


