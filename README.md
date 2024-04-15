#安装 vofa+ 

  sudo dpkg -i vofa+_1.3.10_amd64.deb   			     //安装 vofa+
 
#检查vofa+运行状况

  cd /opt/vofa+/					     //进入到此目录
 
  ./vofa+						     //执行该命令

#报错：./vofa+: error while loading shared libraries: libcrypto.so.1.1: cannot open shared object file: No such file or directory 

  拷贝  libcrypto.so.1.1  文件到    /opt/vofa+/lib   目录下                  

#再次检查vofa+运行状况

  报错：./vofa+: error while loading shared libraries: libGl.so.1: cannot open shared object file: No such file or directory

#安装依赖库

  sudo apt-get install qt5-image-formats-plugins


#之后可正常打开软件，不过不能显示中文 ，缺少中文依赖包 

  sudo apt-get install language-pack-zh-hans      //安装中文支持包

  sudo apt-get install fonts-wqy-zenhei	         //安装常用的中文字体
