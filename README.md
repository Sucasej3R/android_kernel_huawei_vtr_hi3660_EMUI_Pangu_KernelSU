# 对部分华为旧机型编译的内核带KernelSU与Susfs[Pangu_Kernel]
[![Build Huawei-hi3660-KSU-Kernel](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/workflows/Build_Huawei_hi3660_KSU_Kernel.yml/badge.svg)](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/workflows/Build_Huawei_hi3660_KSU_Kernel.yml)
[![Build Huawei-hi3660-KSU-NEXT-Kernel](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/workflows/Build_Huawei_hi3660_KSU_NEXT_Kernel.yml/badge.svg)](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/workflows/Build_Huawei_hi3660_KSU_NEXT_Kernel.yml)
[![Build Huawei-hi3660-KSU-SUKI-Kernel](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/workflows/Build_Huawei_hi3660_KSU_SUKI_Kernel.yml/badge.svg)](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/workflows/Build_Huawei_hi3660_KSU_SUKI_Kernel.yml)

***
## 前情提要：
> [!WARNING]
> **技术预览版本**\
> 此内核正处于早期开发-[技术预览版本]\
> 同时作为自定义内核，与官方内核相比有许多不稳定因素！\
> 相关功能正在尝试添加，问题正在尝试修复

> [!NOTE]
> 此构建从原版的KSU迁移到了[rsuntk](https://github.com/rsuntk)的[RKSU](https://github.com/rsuntk/KernelSU/)，但是没有为其添加Susfs的支持，因此不建议使用\
> rsuntk的管理器[下载](https://github.com/rsuntk/KernelSU/releases)\
> 注明：\
> 最后的原版KSU构建在Action的此[工单](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions/runs/16693550478)\
> v0.9.5的KSU源代码和KSU管理器与华为设备不兼容。\
> 您只能使用v0.9.2管理器。\
> 你可以在这里下载：[KernelSU_v0.9.2_11682-release.apk](https://github.com/tiann/KernelSU/releases/download/v0.9.2/KernelSU_v0.9.2_11682-release.apk)

***
## 内核所支持的机型：
P10版：P10，P10Plus\
V9版：荣耀9，8Pro（V9），Nova2S，平板M5(krin960)，Mate9（Pro）
> [!WARNING]
> 此页面的内核适用于 EMUI9.0/GSI 如果需要 EMUI9.1/GSI 的版本请前往这 ~~[EMUI9.1](https://github.com/yunmo2007/android_kernel_huawei_vtr_emui9.1_KernelSU_NEXT)~~ (此版本暂停维护，仓库已经转为私有，后续会重新开放)\
> 不同版本之间的设备驱动版本不同，请不要混刷，否则会出现黑屏和功能无法使用！
> 详细的说明(强烈建议先去阅读此文件！！)：[旧版README](README_OLD.md)

***
## Github Action说明：
现在编译内核依托于Github Action进行全自动编译。编译的为KernelSU_Next，SukiSU的Susfs版本与rsuntk的KernelSU版本。  
Releases内会发布基于KernelSU_Next，SukiSU的Susfs版本和rsuntk的KernelSU版本内核(月度通道)。  
喜欢尝鲜的朋友可以在Action内下载。  
**版本说明：**
+ Build_Huawei_hi3660_KSU_NEXT_Kernel:给EMUI 9.0 和 GSI系统使用的KernelSU_Next内核。
+ Build_Huawei_hi3660_RKSU_Kernel:给EMUI 9.0 和 GSI系统使用的KernelSU内核。(旧内核支持)
+ Build_Huawei_hi3660_KSU_SUKI_Kernel:给EMUI 9.0 和 GSI系统使用的SukiSU内核。  
 > 内部包含两个系列，一个是P10系列(Pangu_P10_KSU_XXXX)，一个是V9系列(Pangu_V9_KSU_XXXX)。解压后带enforcing的版本刷入后开机SELinux为强制(严格)模式。带permissive的版本刷入后开机SELinux为宽容模式。
  
***
## 后续计划：
> [!NOTE]
> - [x] next-susfs分支手动重构
> - [x] commit重置与文件结构更改
> - [x] 添加其他SU管理器的支持
> - [x] 完成上述任务后的仓库地址变动
> - [ ] \(可能)添加其他算法
> - [ ] \(可能)将内核版本升级到4.14/4.19/5.4

***  

# 下载：  
**稳定版：[Github Release](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/releases)**
**开发版：[Github Action](https://github.com/yunmo2007/android_kernel_huawei_vtr_hi3660_EMUI_Pangu_KernelSU/actions)**  

***
# 额外文档
+ 感谢原作者提供的思路（这两篇并不是我写的但是还是表示感谢）
1. 关于刷机的一些教程:[Wiki](https://github.com/Coconutat/HuaweiP10-GSI-And-Modify-Tutorial/wiki)  
2. 适配华为EMUI9/9.1.0内核的教程:[Wiki](https://github.com/Coconutat/HuaweiP10-GSI-And-Modify-Or-Support-KernelSU-Tutorial/wiki/7.KernelSU%E9%80%82%E9%85%8DEMUI9%E6%88%969.1.0%E7%B3%BB%E7%BB%9F%E7%9A%84%E5%86%85%E6%A0%B8)  

***  
# 创建者/贡献者： 
 + [麦麦观饭](https://github.com/maimaiguanfan) / [麒麟盘古内核](https://github.com/maimaiguanfan/android_kernel_huawei_hi3660/)：提供了内核参考以及基础的内核。
 + [Coconutat](https://github.com/Coconutat) / [带有原版KSU的内核(9.0)](https://github.com/Coconutat/android_kernel_huawei_vtr_emui9_KernelSU) [带有原版KSU的内核(9.1.0)](https://github.com/Coconutat/android_kernel_huawei_hi3660_emui9.1.0_KernelSU):提供了基础的KSU编译思路与此MD文件的基本格式。
 + [kindle4jerry](https://github.com/kindle4jerry) : 感谢大佬的建议和无私帮助。  
 + [aaron74xda](https://github.com/aaron74xda) / [android_kernel_huawei_hi3660
](https://github.com/aaron74xda/android_kernel_huawei_hi3660):启发了我对于华为内核的强制SElinux宽容的具体思路。
 + [OnlyTomInSecond](https://github.com/OnlyTomInSecond) / [android_kernel_xiaomi_sdm845](https://github.com/OnlyTomInSecond/android_kernel_xiaomi_sdm845):提供了KernelSU的移植思路。  
 + [Aquarius223](https://github.com/Aquarius223) / [android_kernel_xiaomi_msm8998-ksu](https://github.com/sticpaper/android_kernel_xiaomi_msm8998-ksu)：修改SElinux的hook.c实现模块功能(可能吧)。  
 + [术哥](https://github.com/tiann) / [KernelSU](https://github.com/tiann)：开发了牛逼闪闪的各种炫酷东东的大佬。没有他就没有KernelSU。感谢他在我折腾华为内核期间给予的帮助。
 + [KernelSU_Next](https://github.com/KernelSU-Next) / [KernelSU-Next](https://github.com/KernelSU-Next/KernelSU-Next):解决了KernelSU在5系内核之前的支持，并且使项目转移到KernelSU_Next。
 + [SukiSU-Ultra](https://github.com/SukiSU-Ultra/) / [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra):解决了KernelSU在5系内核之前的支持，并且使项目转移到SukiSU-Ultra。
 + [rsuntk](https://github.com/rsuntk/) / [KernelSU-legacy](https://github.com/rsuntk/KernelSU):解决了KernelSU在5系内核之前的支持，并且使项目转移到KernelSU-legacy。
 + [simonpunk](https://gitlab.com/simonpunk) / [Susfs](https://gitlab.com/simonpunk/susfs4ksu):新隐藏方式的作者（结合Susfs花费了很久的时间）。
 + [lateautumn233](https://github.com/lateautumn233) / [android_kernel_oneplus_sm8250](https://github.com/lateautumn233/android_kernel_oneplus_sm8250)：启发我使用Github Action编译内核。(解决了我外地上班只有手机的痛点。)

***
#### 滑稽  
![alt 术哥评价适配华为内核行为](https://s1.ax1x.com/2023/03/29/ppgmvo4.png)
