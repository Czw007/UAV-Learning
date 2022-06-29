# 安装Ardupilot

参考：https://ardupilot.org/dev/docs/building-setup-linux.html#building-setup-linux

```plain
首先下载项目源码
git clone https://github.com/ArduPilot/ardupilot
cd ardupilot
git submodule update --init --recursive
最后一步需要的时间较长，耐心等待即可
然后是安装需要的依赖
 
Tools/environment_install/install-prereqs-ubuntu.sh -y 
. ~/.profile
```

最后一步执行脚本可能会出错，这是写需要换ubuntu的安装源

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1646724013865-a17c624f-3fe7-476a-a0cf-5ebc2518e332.png)

各种下载安装失败的原因可能都是网络原因，可以切换节点或者在网络好的时候再安装

因为各种源码，依赖都从github下载，需要开启vpn

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1650422072546-5bad161d-6e1e-495e-9e0a-578561a802d9.png)

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1650542502568-e2209ee6-424b-4195-ae83-1d65672d0b77.png)



## 启动SITL（飞控固件+模拟器）+MAVproxy（地面站）

https://ardupilot.org/dev/docs/setting-up-sitl-on-linux.html

```python
cd ardupilot/ArduCopter
sim_vehicle.py -w（第一次运行之前需要，加载成功后需要强行退出，然后输入下面的指令）
sim_vehicle.py --console --map
```

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1650434810646-0ac2b8b4-683b-4c0d-83f1-b1c160f0fcf8.png)

然后就启动了模拟器+地面控制站MAVProxy