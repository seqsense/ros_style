# ros_style

## cpp

Use clang-format 3.7 and `.clang-format` in this repository.
(later clang-format has a bug around lambda functions)

### building clang-format 3.7

```
$ cd ~/Download
$ wget http://releases.llvm.org/3.7.1/cfe-3.7.1.src.tar.xz.
$ tar xJfv cfe-3.7.1.src.tar.xz
$ cd cfe-3.7.1.src
$ mkdir build
$ cd build
$ cmake .. -DCMAKE_BUILD_TYPE=Release
$ make
$ sudo make install
```

clang-format is installed under /usr/local/bin.
