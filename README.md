﻿个人开发ipa无需发布到appstore即可下载使用。
使用github上传文件xxx.plist

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

实测效果:ios4中开发的软件,使用该方法安装于ios9是,程序进行到显示桌面安装图标后无响应,提示无法下载.
目标ipa文件,使用http和https同时测试
