# S3C2440A_sdram_init
S3C2440A SDRAM 内存初始化程序以及验证初始化结果程序

S3C2440A_raminit.zip 内容

文件夹 S3C2440A：
该工程主要用于初始化内存工作
主要文件 
core/boot/crt0.S     // 初始化设置文件
core/boot/main.c     // blink led 测试
core/boot/S3C2440A.h // 寄存器， 内存初始化关键值等定义
linker/S3C2440A.ld   // 编译器链接文件
build     // 执行编译命令
out/exe/* // 可执行文件和反汇编文件目录
out/map/* // 编译内存映像文件
out/obj/* // 目标文件

make clean 清除临时文件
make 编译

可执行文件下载位置为  sram 0x0 处（详见 S3C2440A.ld 配置）

初始化结果 cpu 频率 532Mhz  内存频率 133Mhz， MPLL 分频比 1:4:8
Led 等 blink闪烁效果


======================================================

文件夹 S3C2440A_SDRAM_test：
测试内存是否初始成功
主要文件 
core/boot/crt0.S     // 初始化设置文件
core/boot/main.c     // blink led 测试
core/boot/S3C2440A.h // 寄存器， 内存初始化关键值等定义
linker/S3C2440A.ld   // 编译器链接文件
build     // 执行编译命令
out/exe/* // 可执行文件和反汇编文件目录
out/map/* // 编译内存映像文件
out/obj/* // 目标文件

make clean 清除临时文件
make 编译

可执行文件下载位置为  sram 0x30000000 处（详见 S3C2440A.ld 配置）
Led 流水灯效果
