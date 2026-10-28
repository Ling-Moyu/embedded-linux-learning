# 第 1 周 · Day 2 笔记

## 今天做了什么
- 看完韦东山 2_3/2_4/2_5：shell 解析、目录文件操作、权限属性
- 完成权限三任务：5 层目录树 + 逐层 chmod + 600 秘密文件
- 用 nano 给 ~/.bashrc 加了永久 PATH，学会 source 生效

## 学到的命令
- ls -l：看权限，drw-r--r-- 这串的读法（类型/主人/组/其他人）
- chmod 755/700/644：数字法 r=4 w=2 x=1
- mkdir -p：一次建多层目录；tree：树状看目录结构
- sudo -u nobody cat：以别人身份执行命令，验证权限真的生效
- nano：命令行文本编辑器（Ctrl+O 保存，Ctrl+X 退出）
- source：让修改过的配置当场生效（不用重开窗口）
- echo $PATH：查看命令搜索路径；export 临时加，写进 .bashrc 才永久
- 命令总结(cd,pwd,mkdir,rm-rf,ls,cp,rm,mv,cat,touch,chown,chmod)

## 今天最大的收获：644 的目录进不去
- chmod 644 给目录后，cd 报 Permission denied
- 原因：目录的 x = 能否进入；r = 能否看名字列表；w = 能否增删文件
- 目录权限和文件权限含义不一样，x 对目录是"门"

## 卡住的问题
- gedit 打不开 → WSL 没有图形界面，改用 nano，已解决
- 遗留疑问：PATH 里故意不放当前目录，是防恶意程序伪装（待第2周细究）
