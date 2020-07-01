## Qualcomm MultDecoderApp Developer documentation

#brief introduction
#This document mainly introduces the deployment and use of MultDecoderApp environment。

#Environment configuration
#Compile environment, run the installation script aikit_ 845_ Env-1.0.sh, mainly including opencv, GStreamer, QT, 
 etc. please modify according to the error prompt if you encounter any problems during the installation process. Refer to MultDecoderApp_Development Manual.doc for details MultDecoderApp.
cd MultDecoderApp
./aikit_845_env-1.0.sh

#Check whether the environment configuration is correct

cd MultDecoderApp
export | grep PATH

#Compile the project and generate the executable file to the MultDecoderApp/ out / directory，The project includes two applications: mult_decoder_app. 
#MultDecoderApp is compiled by default. If firedetectapp is compiled, multpreviewapp needs to be modified/ AiKitConfig.pro ,Remove defines + = make_ FIRE_ Detedt comment "#"
（编译工程，生成可执行文件到MuPreviewApp/out/目录，工程包含MultDecoderApp和FireDetectApp两个应用，默认编译MultDecoderApp，如果编译FireDetectApp，需要修改MultPreviewApp/AiKitConfig.pro,
去掉DEFINES += MAKE_FIRE_DETEDT的注释“#”）

cd AikitDemo
source /etc/profile
qmake；make；make install


#Run program
./mult_decoder_app
