# 项目1 微信-祝福语助手
# 项目2 微信-聊天机器人
如何托管代码1 亚马逊服务器
如何托管代码2 screen
来源:http://blog.sciencenet.cn/blog-255662-582024.html
Putty退出后保持背景程序运行
Putty远程登录Linux，在putty会话窗口关闭后， 远程的命令也停止了执行， 如果想要命令继续执行， 则需要用screen程序。 
方法如下： 
(1)用Putty登录服务器;用户名， 密码
(2)输入screen, 给出帮助提示， 按空格跳过
(3)此时， 程序又回到命令提示符， 但是操作都将在screen中记录。 运行程序（可能需要长时间）。 按住Ctrl + a + d， 此时， 窗口程序与Putty的会话断开， 并提示： 
There is a screen on:
27469.ttt-uuu (06/14/2012 10:10:58 AM) (Detached)
1 Socket in /var/run/screen/S-helixcn.
此时关闭putty的窗口对运算结果将没有影响。
(4) 再次用putty远程登录linux时, 运行 screen -ls 显示所有正在运行的窗口。
(5) 欲回到任何之前的对话窗口， 只需输入 screen -r 27469 即可 （这里27469在每次会话中都是变化的）， 进入窗口后， 如果要结束会话， 从相应程序退出后， 输入exit退出该窗口， 从而返回到最开始登录的状态。
