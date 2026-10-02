# nexmon-p9-native
Native Nexmon kernel patches for Huawei P9 (EMUI 8) — lib-free monitor mode and Wi-Fi injection.

# nexmon-p9-native

## 这是什么？

**Nexmon** 是一个开源的 Wi-Fi 芯片固件研究项目，允许在**博通和赛普拉斯（Broadcom / Cypress）**的 FullMAC 芯片上实现监听模式和帧注入。

- 原项目地址：https://github.com/seemoo-lab/nexmon
- Nexus 5 原生注入参考：https://github.com/seemoo-lab/bcm-public

本仓库是**为华为 P9（EMUI 8）提供的 Nexmon 原生注入内核补丁**，可以让华为 P9 像 Nexus 5 一样，**不依赖任何用户态库（no libnexmon.so）** 进行原生 Wi-Fi 注入。

---

## 重要声明

**在 10 年之后，N5 之后，世界上第二台无限接近原生监听支持的华为 P9 正式诞生了。**

**全球第二台**公开的不依赖 libnexmon.so 的内核原生注入设备（第一台是 Nexus 5）。  
**麒麟平台首例**，**BCM43455 芯片首例**。

这个补丁**无需手动把网卡切换到监听模式**——因为驱动本身就保留了监听接口。  
直接使用工具扫描即可：

```bash
airodump-ng wlan0
