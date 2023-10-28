# 实验2：GBN协议的设计与实现
## 报告与本文件说明
- 为了减少报告文件大小，未在报告中粘贴源代码
- 源代码已经打包在文件中，且带有详细的注释
## 运行环境
- pyCharm 2023.2
- python 3.11 解释器
## 文件目录
### lab_code:代码文件夹
- gbn.py
    - 作用：GBN协议的主要模块
    - 调用：被调用，无执行模块
- sr.py
    - 作用：SR协议的主要模块
    - 调用：被调用，无执行模块
- main.py
    - 作用：执行模块，用户选择执行SR或者GBN
    - 调用：通过多线程执行sr.py和gbn.py中的方法
### file:文本文件
- config_file.txt
    - 作用：配置主机地址
    - 修改：可按照源既定格式修改
- read_file.txt
    - 作用：读取的数据的源文件
    - 修改：读文件操作，可以修改该文件内容以实现传输不同的数据包
	- 包括：上传文件read_upload_file, 下载文件read_download_file
- save_file.txt
    - 作用：生成文件，为接收方保存的文件
    - 修改：无需修改，每次启动程序都会首先将该文件内容擦除
	- 包括：服务器接收的上传文件save_upload_file, 客户端下载文件save_download_file
- save_file_ack.txt
	- 作用：ACK生成文件，为接收方保存ACK信息的文件
	- 修改：无需修改，每次启动程序都会首先将该文件内容擦除
	- 包括：GBN协议的上传文件ACK文件save_upload_file_GBN_ack, 下载文件ACK文件save_download_file_GBN_ack;
			SR协议的上传文件ACK文件save_upload_file_SR_ack, 下载文件ACK文件save_download_file_SR_ack;