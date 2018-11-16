# AutoLogin_Mail for UPC Authentication System
此脚本针对UPC校园网认证系统！   
功能：自动登陆+自动向指定邮箱发送IP变更消息(方便无人值守远程连接) 
## 1、使用方法   
accountList文件：填写能够登陆的网络账号 账号名 密码 运营商 使用空格分隔 多用户使用换行符分隔；     
        运营商代码（中国联通：unicom，中国电信：ctcc，中国移动：cmcc，校园网：default，校园内网：local）  
        
userList文件：填写需要通知的用户名称以及该用户邮箱，使用空格分隔，多用户使用换行符分隔；    

log文件：运行记录默认不保存，只在终端输出，如有需要可以将输出重定向到log文件中

## 2、不同认证系统的自定义方法
（1）不同认证系统POST需要提交的Header和Data不同，该脚本主要适用UPC锐捷web认证，不同认证系统需要修改全局变量中postHeader和postData的格式。  
（2）不同认证系统登陆成功后的重定向网址不同，根据需要可修改CheckLoginStatus函数中的判别方法。  

2018-11-17
