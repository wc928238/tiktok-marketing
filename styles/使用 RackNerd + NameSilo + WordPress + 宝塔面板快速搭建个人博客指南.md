# 使用 RackNerd + NameSilo + WordPress + 宝塔面板快速搭建个人博客指南

## 一、购买 VPS 服务器和域名

### 1.1 选择可靠的 VPS 服务商
[RackNerd](https://bit.ly/Rack_Nerd) 提供高性价比的云服务器方案，支持支付宝付款，非常适合个人博客搭建。

### 1.2 域名注册
推荐使用 NameSilo 注册域名，操作简单且价格实惠。注册完成后记得进行域名实名认证。

## 二、服务器环境配置与域名解析

### 2.1 服务器连通性测试
- 使用在线 ping 工具检测服务器 IP 是否被屏蔽
- 建议测试多个地区节点，确保全球访问正常

### 2.2 SSH 远程连接服务器
bash
ssh root@your_server_ip -p 22

首次登录后请立即：
1. 修改默认密码
2. 检查系统版本：`cat /proc/version`

👉 [【点击查看】2025年最新 Racknerd 优惠码及特价云服务器方案汇总](https://bit.ly/Rack_Nerd)

## 三、安装宝塔面板与配置环境

### 3.1 宝塔面板安装
根据服务器系统选择对应安装命令：
bash
# CentOS
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh

安装完成后会显示面板登录信息，也可通过命令 `bt 14` 重新获取。

### 3.2 推荐环境配置
在宝塔面板中选择：
- LNMP 环境（Nginx + MySQL + PHP）
- 建议选择 PHP 7.4+ 版本

## 四、域名解析与 WordPress 部署

### 4.1 域名解析设置
在 NameSilo 控制面板：
1. 添加 A 记录指向服务器 IP
2. 等待 DNS 生效（约10分钟）

### 4.2 WordPress 一键部署
通过宝塔面板：
1. 选择"网站"→"添加站点"
2. 填写域名并创建数据库
3. 完成 WordPress 初始化配置

### 4.3 启用 HTTPS 安全证书
1. 在宝塔面板申请 Let's Encrypt 免费证书
2. 开启"强制 HTTPS"功能
3. 清除浏览器缓存访问网站

## 五、博客优化建议
- 选择轻量级 WordPress 主题
- 安装必要插件（缓存、SEO等）
- 定期备份网站数据

通过以上步骤，您就可以快速搭建一个安全、稳定的个人博客平台。如果在搭建过程中遇到问题，可以参考各平台的官方文档或社区论坛获取帮助。