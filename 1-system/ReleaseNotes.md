# 0.3.8-20190426-150000

* 更新system app

	1. RokidCameraDeploy:
		- 修复退出人脸识别，没有关闭camera的问题；
		- 更新人脸识别sdk2.2.1.2；
	2. RokidSettings：增加恢复出厂设置前的电量检查，低于25%将不允许恢复出厂设置 ；
	3. RokidAiSdk：
		- 修改眼镜语音默认 Activity 启动部分逻辑；
		- 添加asr、nlp前置拦截器；
		- 添加识别状态返回接口，可以区分SDK当前是使用在线还是离线识别状态；
		- 添加通过配置自动设置自定义激活词功能；
* 更新多路camera服务，优化功耗；

* 优化OTA流程，提高稳定性；

* 修改调节音量时的显示逻辑，不再显示震动 闹钟等文案；

* 修复若干user版本的问题。

# 0.3.7-20190417-150000

* 更新system app

	1. RokidCameraDeploy:
		- 解决卡在识别中界面的BUG；
		- 解决出现”识别中“和”请对正脸“连续切换的问题；
		- 解决偶现SDK中出现crash问题；
	2. RokidActivation：
		- 修改加密算法，解决部分机器无法绑定的问题；
		- 增加和公版APP交互功能(特征库管理)；
	3. RokidCamera：增加每次拍照后发送媒体库变化的广播；
	4. RokidTranslate：状态动画修改，线程优化；
* 调整关机充电百分比文字的位置；

# 0.3.6-20190413-150001

* 更新system app
	1. RokidSetting：增加日期设置；
	2. RokidLauncher：替换远程协助icon；
	3. RokidProvision：修复bug；
	4. RokidAiSdk：
		- 修复client socket crash 后，再次连接，无法将数据传送到turen的bug；
		- 修复turen error之后，再次使用主动拾音，只能吐出asr，不返回nlp的bug；
	5. RokidCameraDeploy:
		- 人脸识别库动态更新；
		- 单人识别中针对区域识别；
		- sdk版本2.2.0.6版本；
	6. RokidActivation：
		- 增加HTTP服务器，用来接收特征库数据库；
		- 增加接收媒体库变化的广播；
	7. RokidCamera：增加每次拍照后发送媒体库变化的广播
* 更新创达改动：
	- 修复多路cam录像花屏问题，偶现crash问题；
	- 更新了正式release的modem和xbl分区；
* 增大关机充电百分比文字的字体；
* 关闭了自动时间和时区校准；
* 增大了投屏显示的ui大小.

# 0.3.5-20190404-150003

* 更新system app
	1. RokidSetting：移除后羿相关逻辑代码；
	2. RokidLauncher：去除了单击back键启动相机的功能；
	3. RokidProvision：增加了日期设置；
	4. RokidAiSdk：
		- 向外暴露每次激活时本次激活的激活词信息；
		- 修复不激活无法使用离线asr的问题；
		- 接入lothal 最近版本，修改录音方式到多路麦克录音。
* power+vol减截屏时，打开camera拍摄一张图片叠加在ui上；

* 增大了刷机后第一次启动时的默认音量；

* 增加了多路mac的功能。
# 0.3.4-20190329-150000

*	合并创达patch：修复多路camera拍照后无法预览问题，支持API2的FULL level；
*	修复音量加键偶现无反应的问题；
*	增加sdk加密校验算法；
*	修改OTA ui效果
*	更新系统app
	1.	RokidAiSdk
		-	完成按键语音识别流程改为根据录音状态来判断是否显示浮层。
		-	添加中英文错误Toast提示
	2.	RokidCameradeploy
		-	解决RokidCameraDeploy出现闪退问题
		-	修改UI显示
	3.	RokidSettings
		-	增加恢复出厂设置选项
		-	修改UI显示


# 0.3.2-20190322-150001

* 合并创达patch
	1. 回退最大音量修改patch，重新修改
	2. 更新camera tunning库
	3. 修复待机电流bug
* 修复开机超过5分钟后进行蓝牙配对，不弹窗的问题
* 根据RokidSetting的需求，修改双击tp的键值为ENTER
* 更新系统app
	1. RokidAiSdk
		- System.Exit时 添加清空技能栈逻辑。
		- 修复无法重新启动rokid语音功能的bug。
		- 修复眼镜浮层偶现需要10秒才能关闭的bug。
		- 优化语音相关的配置文件。
	2. RokidAiSkillEngine
		- 关闭在线状态的本地指令功能，其他app语音控制改为本地技能模式。
		- 修复SkillEngine中技能栈上报链路出错的bug。
		- 修复清空技能栈的同时没有清空clear 技能cache的bug。
	3. RokidCameradeploy
		- 增加语音控制。
		- 修改使用CameraLabraity版本1.0.7.8功能。
		- 修改UI显示，优化新朋友显示逻辑。
	4. RokidLauncher : 修复电量显示bug，修改ui布局设计
	5. RokidSettings
		- 接入语音操作功能
		- 在关于界面长按直接进入投屏
		- 取消重启语音服务的toast
	6. RokidTranslate：接入语音操作功能
	7. RokidCamera：接入语音操作功能
	8. RokidGallery: 接入语音操作功能

# 0.3.1-20190318-150000

*	更新system app
	1.	RokidSetting：系统信息页面长按tp可以直接拉起投射。
	2.	RokidCameraDeploy：重新设计ui，增加单脸识别和多脸识别功能，支持若琪眼镜app导入人脸数据。 
*	修复WFD时视频播放显示异常的问题
*	关闭联网后自动时间校准

# 0.3.0-20190315-150000

*	更新system app
	1.	RokidAiSdk：
		*	添加后羿离线语音功能，语音SDK会通过包名是否存在探测当前设备是普通模式还是后羿模式。。
		*	解决语音SDK初次启动偶现跨进程监听之后，无法自启动数据链接工具类的bug。
		*	修复按键模式语音浮层首次弹出，无法自动关闭的bug。
	2.	RokidSetting：
		*	重新设计WIFI 扫描二维码模块，支持camera2 API
		*	修改按键keycodedpadcenter
		*	修改蓝牙可见性
	3.	RokidGallery：修改按键keycodedpadcenter。
	4.	RokidProvision：修改按键keycodedpadcenter。
	5.	RokidCamera：修改录像尺寸为16：9，修改按键keycodedpadcenter。
	6.	RokidActivation：增加特征库管理接收数据功能。
	7.	RokidTranslate：修改按键keycodedpadcenter。

*	合并TS的多路camera patch，可以支持多app同时打开camera。
*	App crash或ANR时不再弹出dialog，改为toast提醒。
*	增大系统property字节数到128。
*	增加系统alignment和当前硬件版本的property属性。
*	删除系统vr feature的xml配置文件。
*	根据aligment参数调整WFD显示区域。
*	修复截屏图像异常bug。
*	修改系统TP点击按键键值，从ENTER改为DPAD_CENTER。
*	修改蓝牙可见时间，当应用打开蓝牙未设置可见时间时，蓝牙始终可见。

# 0.2.2-20190308-150056

*	更新system app
	1.	RokidAiSdk：
		*	添加后羿模式，通过包名判断。
		*	去除“没事了”激活词配置。
		*	优化录音架构并修改代码，使用系统改动来规避麦克风权限占用问题。
	2.	RokidAiSkillEngine：
		*	统一校准离线asr字段。
	3.	RokidGallery：更新头控sdk方向。
	4.	RokidSetting：重新排列菜单项，更新头控sdk方向。
	5.	RokidLauncher：更新电量显示，更新头控sdk方向。
	6.	RokidRadashoot：更新IMU方向。
*	修改了系统IMU方向，与普通手机竖放的方向一致，可兼容google vr app的方向。
*	修复设置语言后，rokidkeyboard无法拉起的问题。
*	放开系统Audio source HOTWORD的权限，可供语音助手使用。
*	修改OTA服务启动时间，开机后直接启动，不再等待90s。

# 0.2.1-20190301-150055

*	更新system app
	1.	RokidCamera: 修改左右滑动可以自由切换录像和拍照模式
	2.	RokidAiSdk：
		*	接入turen新架构版本lothal，完善全部jni。
		*	添加中文离线asr识别功能。
		*	通用版本中添加网络变动时自动切换成离线/在线功能。
	3.	RokidAiSkillEngine：
		*	添加本地指令处理离线asr命令功能。
		*	本地指令中添加全局固定指令配置。
		*	修改一些技能的默认本地指令配置。
	4.	RokidActivation：添加登录后上报设备信息，可以在若琪APP设置中查看。
	5.	RokidGallery：修改删除图片英文提示。
	6.	RokidSetting：增加操作指南和时间设置入口，增加系统更新入口，拉起原生setting的功能改为直接拉起“显示”设置页面。
	7.	RokidLauncher：修改游戏名称图标支持。
	8.	RokidProvision：新增开机系统引导App，在刷完机第一次开机时或者恢复出厂设置后启动。
	9.	RokidTranslate：修改新的交互方式。
	10.	RokidRadashoot：替换为新游戏：突袭。
	11.	CameraDeploy: 修改人脸最大识别数10，修复camera抢占问题。
*	修改系统SystemUi默认通知展示的样式：修改长宽及背景色。
*	重构OTA流程，移除了自动更新，需要用户在setting中主动发起。

# 0.1.9-20190222-150053

*	更新system app
	1.	RokidCamera: 拍照分辨率改成16：9
	2.	RokidAiSdk：
		*	按键模式下，增添不佩戴无法使用限制。
		*	更新代码并适配最新的RokidAiSkillEngine。
		*	将本地指令迁移到RokidAiSkillEngine中。
	3.	RokidAiSkillEngine：
		*	架构完全重构，提出center、executor概念模块。
		*  修改消息传递方式，预留出适应局域网传递接口。
		*	增加本地技能搜索、nlp传递、拦截控制等相关功能。
	4.	RokidAiCloudApp：
		*	更新代码并适配最新的RokidAiSkillEngine。
	5.	RokidCameraDeploy：支持中英文菜单
*	back双击改回默认launcher，可以通过修改system/etc/SystemConfig.prop的配置自定义
*	增加property属性，可以设置默认launcher
*	增加后羿device目录，编译后羿专用镜像
集成进RokidKeyboard，并设置成默认输入法，支持tp操作：前后滑动tp控制光标左右，音量键+-控制光标上下，点击tp确认输入。

# 0.1.8-20190201-150052

*	更新system app
	1.	RokidCamera: 相机增加语音控制拍照和退出功能
	2.	RokidCameraDeploy: 重构识别流程，优化识别速度
	3.	RokidShow：移除
*	移除自动时区功能
*	增加realtek r8150/8152 USB网卡驱动支持
*	ota更新增加dsp.img分区
*	修复默认setting中投射无法点击的问题
*	同步创达更新
	1.	配合产线需求和PC工具，增加Psensor校准功能
	2.	配合产线需求和PC工具，修改音频测试配置
	3.	合入高通解决modem死机patch
	4.	删除动态库中的冗余打印

# 0.1.7-20190125-150044

*	更新system app
	1.	RokidActivation：修复文件管理的一些BUG
	2.	RokidCamera: 修改切换到视频模式就停止语音，避免录像和语音服务冲突导致的crash
	3.	RokidSettings: 增加在本机信息中启动原生设置的隐藏入口
	4.	RokidGallery：修复了连续删除照片crash问题
*	修改打开投射时，默认开启wfd功能
*	修改setting，打开投射时获取按键焦点，方便tp控制wfd
*	整理按键逻辑，修复双击返回键遗留bug
*  修复zoom app 没有声音的bug

# 0.1.4-20190118-150041

*  更新system app 
	1.	RokidAiCloudApp 伟明 -迁出engine、TtsService，并优化剩余代码
	2.	RokidAiSdk/ 伟明 -接入ProximitySensor监听，完成眼镜语音助手“若琪”激活模式用户佩戴、不戴、息屏、亮屏等交互逻辑优化; 修复语音浮层弹出，屏幕亮起功能
	3.	RokidCamera/ 恒锋 -
	4.	RokidCameraDepoly/。 闻斌 无更新
	5.	RokidGallery/。 杨剑 -1. 替换删除按钮​​.2. app那边删除图片同步
	6.	RokidLauncher/。 杨剑 -修复时间显示的crash
	7.	RokidSettings/ 恒锋 -
	8.	RokidTranslate/。 恒锋 无更新
	9.	RokidActivation 恒锋 -。
* WFD功能增加camera 预览为背景
* 双击返回不再回到launcher，改为发送intent广播 
* ota升级成功后发送intent广播
* 同步创达更新
	1. remove gps hal
	2. remove unused module in kernel
	3. TRY_SINK to swap to UFP while plugging in a typec dev
	4. modify audio ftm config file
	5. update TP firmware
	6. remove iop
	7. resolve AutioTimeZone issue

# 0.1.3-20190111-150040

* 更新system app 
	1.	RokidAiCloudApp 伟明 -修改tts通知名称，用新正则过滤所有技能tts
	2.	RokidAiSdk/ 伟明 -语音唤醒词修改 rada为游戏、showroom为播放器，优化其他本地指令
	3.	RokidCamera/ 恒锋 -录制过程中无法唤醒若琪; 录制视频的时间放在中间显眼的位置
	4.	RokidCameraDepoly/。 闻斌 -识别不到的时候显示绿色框和“新朋友”文案
	5.	RokidGallery/。 杨剑 -长按删除照片及视频交互方式改变。
	6.	RokidLauncher/。 杨剑 -桌面支持头部运动浏览图标
	7.	RokidSettings/ 恒锋 -设置新增头部运动开关，控制相册、桌面、设置列表的头部运动浏览。
	8.	RokidTranslate/。 恒锋 无更新
	9.	RokidActivation 恒锋 -集成mqtt，实现glass扫二维码后与账户绑定，glass语音触发可在app上看到相应信息；在APP端管理相册中的照片及视频。
* 增加从persist分区读取seed并设置property的功能
* 修复md5校验错误导致无法下载新的ota升级包的问题 
* 修复ota弹窗显示不全的问题

# 0.1.2-20180104-150033

*	 更新system app（RokidAiCloudApp, RokidAiSdk, RokidCameraDeploy, RokidGallery, RokidLauncher，RokidTranslate），增加RokidActivation
*	 增加rokid glass type id
*	 修复keyevent 事件的上报逻辑
*	 去除Psensor自动校正
*	 更新IMU sensor校正
*	 修改百度时区sdk的key
*	 删除vendor下的Generic.kl，解决增量编译按键错误的问题



