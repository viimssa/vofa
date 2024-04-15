
# 在Windows子系统Ubuntu安装vofa+

## 准备工作

1. 首先装好 Ubuntu 子系统

2. 下载 vofa+_1.3.10_amd64.deb、libcrypto.so.1.1 两个文件
   
3. 将 vofa+_1.3.10_amd64.deb、libcrypto.so.1.1拷贝到tmp目录下

4. 进入到tmp目录安装vofa+

   ```bash
   cd /tmp
   sudo dpkg -i vofa+_1.3.10_amd64.deb
   ```

5. 进入到opt目录检查vofa+运行状况

   ```bash
   cd /opt/vofa+
   ./vofa+
   ```

6. 这里会错误提示，缺少openssl库的加密解密文件
![01](https://github.com/viimssa/vofa/assets/164175884/f65781a9-271a-4ee6-a0e6-c99e530db7c5)

7. 拷贝  libcrypto.so.1.1  文件到    /opt/vofa+/lib   目录下

    ```bash
    sudo mv /tmp/libcrypto.so.1.1 /opt/vofa+/lib/
    ```

8. 再次检查vofa+运行状况,还有错误提示，缺少UI界面依赖
![02](https://github.com/viimssa/vofa/assets/164175884/6bd4ab69-9676-44da-b4e6-919b32c8f119)

9. 安装qt5-image-formats-plugins库

    ```bash
    sudo apt-get install qt5-image-formats-plugins
    ```

10. 之后即可正常打开vofa+,不过界面可能会乱码，不能正常显示中文

11. 这里需要安装中文支持包和常用的中文字体

    ```bash
    sudo apt-get install language-pack-zh-hans
    sudo apt-get install fonts-wqy-zenhei
    ```

重启vofa+，就可以正常使用vofa+



