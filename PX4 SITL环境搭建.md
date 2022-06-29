# PX4环境搭建

## 1）安装内容：

**PX4（飞控固件）**

**jMAVsim(模拟器)**

**QGroundControl(地面控制站）**



## 2）飞控固件：PX4



```plain
首先选择安装目录，然后执行下面两条命令：

git clone https://github.com/PX4/PX4-Autopilot.git --recursive

bash ./PX4-Autopilot/Tools/setup/ubuntu.sh
```



## 2.仿真器：jMAVSim

已经跟随PX4安装，不需要安装

**启动PX4并打开模拟器：**

```plain
make px4_sitl jmavsim
```

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1649898191104-6aed34c5-0e82-443a-a9b2-55fb6530c991.png)

报错：INFO  [simulator] Waiting for simulator to accept connection on TCP port 4560）

解决方法：https://blog.csdn.net/Iamsonice/article/details/120372120

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1649897592556-4ea44b45-3952-4e77-bef1-f05cb5e580fb.png)





### 也可以分别启动 jMAVSim 和 PX4

```plain
单独启动jmavsim
./Tools/jmavsim_run.sh -l
单独启动px4
make px4_sitl non
```

另外：PX4中

也集成了gazebo

```plain
make px4_sitl gazebo
```

![img](https://cdn.nlark.com/yuque/0/2022/png/2652737/1649898625132-64d2eb53-57c4-48be-84b8-fee9cb118f40.png)

## 3）QGroundControl：地面控制站

https://docs.qgroundcontrol.com/master/en/getting_started/download_and_install.html

**打开控制站：**

```plain
./QGroundControl.AppImage
```