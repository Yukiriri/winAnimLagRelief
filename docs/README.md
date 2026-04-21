从NVIDIA RTX30+开始，在低负载时存在系统动画掉帧  
掉帧的原因是GPU核心和显存都休眠太深，重新唤醒又过慢  
使用NV自带的工具锁定GPU核心和显存频率下限，可以大幅缓解掉帧  

## 使用方法
下载和管理员运行[`lock-nvgpu-min-mhz.bat`](../bin/lock-nvgpu-min-mhz.bat)  

> [!NOTE]  
> 这个修改仅够维持本次开机，严格来说只能维持本次驱动会话，驱动状态更改后就被重置  
> 如果要永久生效，需要加入开机自启  

## 加入开机自启
下载和双击导入[`lock-nvgpu-min-mhz.reg`](../bin/lock-nvgpu-min-mhz.reg)  

> [!IMPORTANT]  
> 需要启用系统开发者设置的sudo（24H2新功能）  

## 如果没有任何办法做到管理员开机自启怎么办
那就每次开机后手动管理员运行bat吧（）
