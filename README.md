# ros_style

## python

### Usage

```shell
$ yapf --recursive --in-place --parallel $DIR (Specify a target directory)
```

## cpp

Use clang-format 3.7 and `.clang-format` in this repository.
(later clang-format has [the bug](https://www.mail-archive.com/llvm-bugs@lists.llvm.org/msg05471.html) around lambda functions)

Make symlink to .clang-format file in your workspace directory.
```shell
$ ln -s /path/to/ros_style/.clang-format /path/to/your/workspace/
```

The cpp codes must be checked by [roslint cpplint](http://wiki.ros.org/roslint).

### building clang-format 3.7

```shell
$ cd ~/Downloads  # change as you like
$ wget http://releases.llvm.org/3.7.1/llvm-3.7.1.src.tar.xz
$ tar xJfv llvm-3.7.1.src.tar.xz
$ cd llvm-3.7.1.src/tools
$ wget http://releases.llvm.org/3.7.1/cfe-3.7.1.src.tar.xz
$ tar xJfv cfe-3.7.1.src.tar.xz
$ cd ..
$ mkdir build
$ cd build
$ cmake .. -DCMAKE_BUILD_TYPE=Release
$ make clang-format
$ sudo cp bin/clang-format /usr/local/bin/
```

clang-format is installed under /usr/local/bin.

### note

Line length limit (ColumnLimit) is disabled in this config.
Please check it by using [roslint cpplint](http://wiki.ros.org/roslint).
