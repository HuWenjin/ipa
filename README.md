个人开发ipa无需发布到appstore即可下载使用。



1.选择https服务器（需要有服务商颁布的https证书）

  1.1通常使用startssl申请（免费）

StartSSL是StartCom公司旗下的SSL证书，貌似是现在唯一一家提供免费SSL证书服务并且被主流浏览器支持的免费SSL，包括Chrome、Firefox、IE等浏览器都可以正常识别StartSSL，任何个人都可以从StartSSL中申请到免费一年的SSL证书。
StartSSL申请虽然要审核，但是一般十几分钟就会回复邮件了。而且经过部落的几次申请测试发现，StartSSL申请审核并不严格，如果遇到问题，你只要回复一封邮件过去回答邮件当中所提的问题，通过率几乎是100%。
步骤如下
http://www.freehao123.com/startssl-ssl/
1.2 或者直接使用第三方服务器 如github支持https服务器（dropbox国内已和谐，你懂得）

   1.2.1使用github上传文件xxx.plist

  

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>items</key>
	<array>
		<dict>
			<key>assets</key>
			<array>
				<dict>
					<key>kind</key>
					<string>software-package</string>
					<key>url</key>
					<string>http://xxx/xxx.ipa</string>
				</dict>
			</array>
			<key>metadata</key>
			<dict>
				<key>bundle-identifier</key>
				<string>com.fnst.smartwork</string>
				<key>bundle-version</key>
				<string>1.0</string>
				<key>kind</key>
				<string>software</string>
				<key>title</key>
				<string>xxx.ipa</string>
			</dict>
		</dict>
	</array>
</dict>
</plist>
如上http://xxx/xxx.ipa为可以正确下载该ipa的地址。

其余XXX均类似为用户自定义内容 



如上传至 https://github.com/qixiaobo/WeiChat 目录下获取该plist链接https://raw.githubusercontent.com/qixiaobo/WeiChat/master/XXX.plist

2.在ios的浏览器里访问如下网址itms-services://?action=download-manifest&url=https://raw.githubusercontent.com/qixiaobo/WeiChat/master/XXX.plist即可实现安装ipa！！！