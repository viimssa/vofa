#安装 vofa+ 

    ```bash
    sudo dpkg -i vofa+_1.3.10_amd64.deb   			     
    ```
    
#检查vofa+运行状况

    ```bash
    cd /opt/vofa+ 	
    
    ./vofa+						          
     ```
     
#报错：./vofa+: error while loading shared libraries: libcrypto.so.1.1: cannot open shared object file: No such file or directory 
![01](https://github.com/viimssa/vofa/assets/164175884/d0004361-f77c-477b-a587-9e9b9267482b)

拷贝  libcrypto.so.1.1  文件到    /opt/vofa+/lib   目录下                  

#再次检查vofa+运行状况

报错：./vofa+: error while loading shared libraries: libGl.so.1: cannot open shared object file: No such file or directory
  ![02](https://github.com/viimssa/vofa/assets/164175884/8572ac0e-eb5e-4e23-94eb-b23e33bb717b)

#安装依赖库
    ```bash
    sudo apt-get install qt5-image-formats-plugins
     ```

#之后可正常打开软件，不过不能显示中文 ，缺少中文依赖包 -----安装中文支持包 -----安装常用的中文字体
    ```bash
    sudo apt-get install language-pack-zh-hans      
    sudo apt-get install fonts-wqy-zenhei	         
     ```
