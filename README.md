# GIGABYTE B560M-AORUS-ELITE I5-11400F 5500XT RTL8111 RTL8125 macOS 13.2.1
使用了geminiwen大大的EFI做了小修改。原地址https://github.com/geminiwen/Gigabyte_B560m_AORUS_PRO_AX_i5_11600K
- 主板：GIGABYTE-B560M-AORUS-ELITE
- 处理器：I5-11400F
- 内存：Kingston FURY 16GB DDR4 2666 * 4
- 硬盘：Kingston 240GB A400
- 显卡：蓝宝石Sapphire 5500XT
- 网卡：RTL8111 RTL8125 
- 系统：macOS 13.2.1
- 移除了 Intel 网卡，使用了博通的RTL8111、RTL8125网卡替换
- 移除了 核芯显卡区动添加AMD-5500XT驱动 
- 因为使用了 Intel 11th Gen CPU，所以使用的 SMBIOS 为 Mac Pro 7,1，禁用了 iGPU，不然硬件加速无法启用。


## 已知问题
- 路由器输出接口 为非2.5G口 安装完后 RTL8125网卡默认自动不能上网 需手动改 相应速度
- 修改方法打开系统便好设置 — 》网络 –〉以太网，点击高级按钮，弹出的选项再点击硬件选项卡
  - 配置：选择手动。
  - 速度：根据你的路由器输出接口设置，我这里是千兆所以选择1000baseT。
  - 双工：我这里选择全双工、流控制、节能以太网，这个根据个人情况设置，如果设置了不能上网，你就换个选择。
  - MTU：默认

- sidecar 不能使用
