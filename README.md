# Wechat_database_decrypt
## 提取EnMicroMsg.db
这个是我们微信记录数据的数据库,提取这个文件有两种方法:
- 本机root,直接提取,地址为`/data/data/com.tencent.mm/MicroMsg/xxx(一大串hash值)/EnMicroMsg.db`
- 用模拟器登陆微信,推荐**网易MuMu模拟器**,速度流畅另外自带root权限,还可以文件共享
## 解密EnMicroMsg.db
密码是md5(IEMI+uin)取前7位,注意不是数值相加,是拼接
- IMEI也有两种方法:
    - 拨号输入`*#06#`
    - 模拟器直接设置
- uin如何获取
    - uin一般都是存放在本地的`/data/data/com.tencent.mm/shared_prefs/`下的`com.tencent.mm_preferences.xml`文件中
- md5计算
    - 利用hashTab工具计算取前7位

## 导出数据
- 利用仓库的可视化工具打开,导出message表