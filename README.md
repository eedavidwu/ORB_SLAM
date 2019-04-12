# OpenCV_handbook
<br>Ubuntu 16.04+CUDA8.0+OPENCV3.3+Caffe环境搭建
<br>https://www.jianshu.com/p/b2470020e035
<br>opencv2.4.11: https://www.linuxidc.com/Linux/2016-07/132882.htm


<br>About Nvidia
<br>https://blog.csdn.net/xunan003/article/details/81665835


<br>卸载cmake的包:
<br>sudo make uninstall
<br>sudo rm -r build




<br>apt-get install的降版本 安装aptitude，使用aptitude来进行降级。　　
<br>sudo apt-get install aptitude


<br>使用aptitude命令进行降级
<br>aptitude install libncurses5=5.7


<br>命令解释
<br>aptitude install 包名=包的版本号  

<br>关于PCL
<br>http://www.pointclouds.org/documentation/tutorials/compiling_pcl_posix.php
#Ros
<br>特别注意：安装后不能上网的，运行以下命令：sudo ln -s /run/resolvconf/resolv.conf /etc/resolv.conf

##更新GCC支持C++11：
<br>cd gcc-5.3.0
<br>./contrib/download_prerequisites
<br> mkdir build_gcc_5.3.0
<br>cd build_gcc_5.3.0
<br>../configure --enable-checking=release --enable-languages=c --disable-multilib
<br>make
<br>make install
##更新CMAKE：
<br>cd cmake-3.10.3 
<br>./bootstrap
<br>make 
<br>sudo make install
<br>Tips:
<br>当：version `GLIBCXX_3.4.18' not found则：
<br> sudo find / -name libstdc++.so.6*
<br>sudo cp /usr/local/lib64/libstdc++.so.6.0.21 /usr/lib/x86_64-linux-gnu/
<br> sudo rm -rf  /usr/lib/x86_64-linux-gnu/libstdc++.so.6
<br>sudo ln -s /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.21 /usr/lib/x86_64-linux-gnu/libstdc++.so.6
(https://blog.csdn.net/amor_tila/article/details/77976964)

##安装Pangolin：
依赖：sudo apt-get install libglew-dev
<br>git clone https://github.com/stevenlovegrove/Pangolin.git
<br>cd Pangolin
<br>mkdir build
<br>cd build
<br>cmake ..
<br>make
