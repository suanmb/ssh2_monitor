# ssh2_monitor监控 v0.2版
    本项目是用java编写的监控程序，可以监控多台主机。依赖的环境为 java+oracle+linux。
    核心功能是利用ssh2 服务，实现在不同的主机上执行脚本或命令。
    因此，每台主机只要开启ssh2服务即可，无需在每台主机都安装代理程序。
为了调高灵活性。设计了如下执行动作。<br>
-  条件检查 <br>
-  阈值判断<br>
-  执行预定修复命令或其他脚本<br>
-  关联后续动作继续执行形成执行流<br>
-  支持sql操作，甚至自己可以修改自己的配置。<br>

### 特点
1.无需在各台主机上分别部署，只需部在一台主机即可，要监控的所有主机打开ssh2服务即可。<br>
2.多线程执行各监控项，而且是并发执行的。<br>
3.只需一张配置表，其所属用户可配。<br>
4.可直接执行Linux命令，或监控接口表是否积压。<br>
5.监控值大于阈值时，可触发执行linux命令，或sql语句。且支持执行流。<br>

