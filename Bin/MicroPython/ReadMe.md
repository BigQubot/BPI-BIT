# 如何烧写？

##Linux 使用 shell 命令行直接调用

- 在这之前需安装python2.7和依赖pip install esptool。
- `esptool.py --chip esp32 --port COM3 --baud 1152000 write_flash -z --flash_mode dio --flash_freq 40m 0x1000 firmware.bin`

##Windows 双击运行此处提供的EXE程序

- 程序将运行烧写同一目录下的`fimware.bin`文件
- 经由`Pyinstller X86`打包而成

##Python源码直接调用烧写请自行查看此处的Py文件。

- 不做解释。
- 不，还是稍微解释一下。
    1. AutoErase是指擦除当前硬件的固件，当遇到问题的时候解决不了请直接擦除，包治百病。
    2. AutoFlash分别为Fast和Safe，即为快速烧写和安全烧写，除了烧写速度以外没有区别，可以自行在Py代码中查阅得知。
    
##烧写之后？

- 请到目录 Code 下获取 Python 开发说明介绍。

- https://github.com/yelvlab/BPI-BIT/tree/master/Code/MicroPython