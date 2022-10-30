# rime-table-bin-decompiler

反编译 [RIME] 的 `xxx.table.bin` 二进制词典文件，生成 `xxx.dict.yaml`
纯文本词典文件。

[RIME]: https://github.com/rime/librime

## 简介

Fork 自 [whjiang/rime_table_bin_decompiler]，相较于原项目，有以下变动。

+ 修复在 Linux 系统上的编译错误
+ 更易读的 README

[whjiang/rime_table_bin_decompiler]: https://github.com/whjiang/rime_table_bin_decompiler

## 编译

### 工具链

+ [GNU ToolChain]
+ [CMake]
+ [Boost]

[GNU ToolChain]: https://wiki.archlinux.org/title/GNU#Toolchain
[Boost]: https://www.boost.org
[CMake]: https://www.cmake.org

### 步骤

1. `git clone --depth=1 git@github.com:kitty-panics/rime-table-bin-decompiler.git`
2. `cd rime-table-bin-decompiler && mkdir build && cd build`
3. `cmake ..`
4. `make`

## 使用

注意，由于 `xxx.table.bin` 二进制词库文件没有元数据信息，反编译生成的 `xxx.dict.yaml`
纯文本词典文件的文件头中的元数据信息，是根据常见的元数据信息填补进去的，可能是错误的，
需自行修正。

```Bash
# 反编译二进制词库并标准输出：
rime-table-bin-decompiler xxx.table.bin

# 反编译二进制词库并输出到纯文本词库文件中：
rime-table-bin-decompiler xxx.table.bin > xxx.dict.yaml
```

## 许可证

[License]

[License]: LICENSE
