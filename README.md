针对Obfuscator对LLVM10.0的移植，详情参考：
[LLVM（二）obfuscator混淆工具移植llvm-10.0](http://www.gandalf.site/2020/08/llvmobfuscator-llvmllvm-100.html)

由于在解压后的llvm项目文件夹内部编译会失败，所以需要在llvm项目外部新建一个文件夹再进行编译：
```sh
$ mkdir build
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Release -DLLVM_CREATE_XCODE_TOOLCHAIN=ON ../llvm
$ make -j7
```

other:

Please have a look at the [wiki](https://github.com/obfuscator-llvm/obfuscator/wiki)!

Current version: [LLVM-4.0](https://github.com/obfuscator-llvm/obfuscator/tree/llvm-4.0)

You can cite Obfuscator-LLVM using the following Bibtex entry:

```
@INPROCEEDINGS{ieeespro2015-JunodRWM,
  author={Pascal Junod and Julien Rinaldini and Johan Wehrli and Julie Michielin},
  booktitle={Proceedings of the {IEEE/ACM} 1st International Workshop on Software Protection, {SPRO'15}, Firenze, Italy, May 19th, 2015},
  editor = {Brecht Wyseur},
  publisher = {IEEE},
  title={Obfuscator-{LLVM} -- Software Protection for the Masses},
  year={2015},
  pages={3--9},
  doi={10.1109/SPRO.2015.10},
}
```
