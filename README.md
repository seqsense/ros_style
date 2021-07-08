# ros_style

## python

### Usage

```shell
$ yapf --recursive --in-place --parallel $DIR (Specify a target directory)
```

## cpp

Use clang-format 11 and `.clang-format` in this repository.
You can install clang-format 11 with apt if you are using Ubuntu 20.04.
```
$ sudo apt install clang-format-11
```


Make symlink to .clang-format file in your workspace directory.
```shell
$ ln -s /path/to/ros_style/.clang-format /path/to/your/workspace/
```

The cpp codes must be checked by [roslint cpplint](http://wiki.ros.org/roslint).

### Notes

- Formatting of initializer list

When you want to put only one element per line, please add comma after the last element to format them correctly.


With last comma:
```
  std::vector<int> a =
      {
          1,
          2,
          3,
      };
```

Without last comma:
```
  std::vector<int> a =
      {
          1,
          2,
          3};
```

- Line length limit

`ColumnLimit` parameter is disabled in this config.
Please check it by using [roslint cpplint](http://wiki.ros.org/roslint).
