# INI文件配置解读

|              项              |                             说明                             |  属性  |   备注   |       例        |
| :--------------------------: | :----------------------------------------------------------: | :----: | :------: | :-------------: |
|            debug             |                           输出日志                           |  bool  |          |      False      |
|save_debug_img|输出调试文件|bool|给开发者后，可以帮助减少BUG|True|
|  trace_exception_for_debug   | 开启后，所有的try向上传递错误信息，并且只用第一个device跑第一个任务（单进程） |  bool  |          |      False      |
|      use_template_cache      |                 在开发工具使用时可以将其关闭                 |  bool  |          |      True       |
|        baidu_ocr_img         |      是否输出名为 baidu_ocr.bmp的图片，该图片为原生截图      |  bool  |          |      False      |
|        disable_timeout_raise         |      如果lock_img报错，是否禁用错误      |  bool  |          |      False      |
|u2_record_size|U2指令记录列表大小|int|20      ||
|u2_record_filter|U2指令过滤列表|list|列表中的指令不会被记录|[]      |
|debug_record_size|Automator指令记录列表大小|int|50      ||
|debug_record_filter|Automator指令过滤列表|list|列表中的指令不会被记录|['_lock_img','_move_check']      |
|trace_tree|追踪的分支版本|str||master |
|force_as_ocr_as_possible|开启后，如果某个任务有OCR版本，则自动使用之|bool||True|
| qqbot_select | qqbot的选择api服务商 | str | CoolPush/Qmsgnike | CoolPush |
| qqbot_private_send_switch | qqbot私聊开关 | int | 0关 1开 | 0 |
| qqbot_group_send_switch | qqbot群聊开关 | int | 0关 1开 | 0 |
| qqbot_key | qqbot的apikey | str | | SCU6390~94d830b |
| qq | 指定接收消息的QQ号或者QQ群号，可以添加多个，以英文逗号分割。如：1244453393,2952937634（指定的QQ号或QQ群号必须在您的QQ号列表中） | str | 这个Qmsgnike才会用到 | 1244453393,2952937634 |
| tg_token | 电报的token | str | 具体看说明文件 | SCU6390~94d830b |
| tg_mute | 电报推送是否静音 | bool |  | Flase |
| proxy_http|推送使用的代理|str|||
| proxy_https|推送使用的代理|str|||
|           s_sckey            |                     s_sckey为Server酱API                     | string |          | SCU6390~94d830b |
|         sentstate          |                 全体BOT播定时报脚本任务状态                 |  int   | 单位分钟 |        5        |
| sent_state_img | 播报任务状态时是否推送运行截图 | bool |  | Flase |
|           log_lev            | log_levBOT的日志等级，微信日志等级 仅有0/1/2/3，越小越详细，注意每天接口调用有上限！ |  int   |          |        1        |
|          log_cache           |                       日志缓冲消息条数                       |  int   |          |        3        |
|         baidu_apiKey         |                  baidu_apiKey为百度ocr api                   | string |          | SCU6390~94d830b |
|       baidu_secretKey        |                 baidu_secretKey为百度ocr api                 | string |          | SCU6390~94d830b |
| baidu_QPS | baidu_QPS为百度并发限制连接数 | int | | 2 |
| ocr_mode | OCR模式目前有智能/本地/网络/混合 4种不同的工作方式 | string | | 混合 |
| anticlockwise_rotation_times |      根据baidu_ocr.bmp需要逆时针旋转90°多少次截图才正向      |  int   |          |        1        |
|    async_screenshot_freq     |                     异步截图一次休眠时间                     |  int   |          |        5        |
|     bad_connecting_time      |                      异步判断异常的时间                      |  int   |          |       30        |
|        fast_screencut        |                       mincap 快速截图                        |  bool  |          |      True       |
|     fast_screencut_delay     | 由于截图太快造成脚本崩溃，可以使用这个加上全局的截图delay，模拟卡顿。 | float  |          |       0.5       |
|    fast_screencut_timeout    |                      等待服传输数据超时                      | float  |          |       10        |
|         end_shutdown         |                   非常“危险”的Windows功能:自动关机           |  bool  |          |      True       |
|       lockimg_timeout        |               90秒如果还在lockimg，则跳出重启                |  int   |          |       90        |
|         enable_pause         |              开启后，可以按下Shift+P暂停脚本。                |  bool  |          |     True       |
|       running_input          |           开启后，可以在运行时向控制台输入指令                   |  bool |          |      True  |
|selected_emulator|使用的模拟器的名称|string||雷电|
|enable_auto_find_emulator|启动自动模拟器搜索，理论支持各种模拟器共同使用|bool|建议关闭|False|
|emulators_port_interval|自动搜索模拟器端口区间|list||[5565,5566]|
|emulators_port_list|自动搜索模拟器连接的端口list|list||[5565,5566]|
|emulator_ports|（除雷电外的的）模拟器端口|list|雷电可以不写|[]|
|adb_dir|adb目录|str|可以使用脚本自带adb|adb|
|emulator_console|模拟器控制台目录|str|目前仅支持雷电|F:\XuanZhi\LDPlayer\ldconsole.exe|
|emulator_id|模拟器设备编号|list|目前只支持雷电|[0,1]|
|quit_emulator_when_free|空闲时退出模拟器|bool||True|
|max_free_tine|空闲多久触发推出模拟器|int|单位：秒|120|
|captcha_level|接码平台的识别等级|str|特速双倍扣分哦|小速/特速|
|captcha_userstr|接码密码串|str||10001\|QASWC~G3A9|
|captcha_software_key|接码的软件KEY|str||1001\|4A96~F0EA|
|captcha_senderror|                         自动申诉题目                         |bool|成功返回分值，失败扣除双倍|True|
|captcha_senderror_times| 验证失败多少次后触发自动申诉题目 |int||2|
|captcha_skip|出现验证码是否直接跳过该账号|bool||True|
|captcha_wait_time|出现验证码后等待用户输入的时间|int||60|
|clear_traces_and_cache|是否启用PCR干净模式|bool||True|
|use_my_id|是否使用自己提供的身份证|bool|                             |True|
|auto_start_app|执行first/continue后是否自动打开app.py|bool||True|
|inline_app|是否采用内部方式打开app（无窗口，无输出）|bool||True|
|captcha_popup|出现验证码后是否弹出置顶提示框|bool||True|
|wait_for_launch_time|自启动模拟器最大忍耐超时时间|int||600|
|ignore_serials|不连接的模拟器|str||["emulator-5554"]|





------

小脚印

- 2020/8/5 By:CyiceK
- 2020/8/30 By:TheAutumnOfRice