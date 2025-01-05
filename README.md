**Fmake** is a bash script that automatically makes and runs project build.
Intended to use with *CMake*, `CMakeLists.txt` is getting cached for comparison and to avoid regenerating Makefile

`Command line options:`
### Add # before flag to enable opposite effect of parameter
> Example: `fmake -#c` -  Do not clean *.o files after finish
```
  -c, --clean            Clean *.o files after finish
  -h, --help             Print this text
  -p, --pass-run         Skip running build for once
  -r, --reset            Restore config initial state
  -s, --silent           No verbose
  -t, --time             Print current time before compiling and after closing executable.

```
## Config file is stored in `/home/user/.config/fmake.conf`:
```
run_build=true
build_folder_name="build"
move_build_to_parent=true
print_time=true
clean=true
```
Command line options *do* override configuration values temporarily.
