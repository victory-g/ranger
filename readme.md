### 用户手册
https://github.com/ranger/ranger/wiki/Official-user-guide
### ranger安装
```shell
$ sudo apt-get install ranger
```
### 配置文件
```shell
$ ranger --copy-config=all

$ cd ~/.config/ranger
```

#### 配置文件说明

|    配置文件    |               说明               |
| ------------- | ------------------------------- |
| `rc.conf`     | 选项设置和快捷键                  |
| `commands.py` | 能通过 : 执行的命令               |
| `rifle.conf`  | 指定不同类型的文件的默认打开程序。 |
| `scope.sh`    | 用于指定预览程序的文件            |

#### 取消ranger默认配置
```shell
# 环境变量设置
RANGER_LOAD_DEFAULT_RC FALSE
```

### 自动挂载U盘等外部存储位置,需要安装usbmount
```shell
$ sudo apt-get install usbmount
$ sudo vim /etc/usbmount/usbmount.conf

# 在MOUNTOPTIONS那行添加user即可使普通用户也对挂载的U盘拥有写权限, 如下:MOUNTOPTIOS="rw,user,noatime,nodiratime"
```

### 浏览

| ranger命令 |     功能      |
| ---------- | ------------- |
| `{`        | 在上级目录上移 |
| `}`        | 在上级目录下移 |
| `Ctrl-f`   | 向下翻页       |
| `Ctrl-b `  | 向上翻页       |


### 编辑

|     ranger命令      |       功能       |
| ------------------ | ---------------- |
| `?`                | 帮助             |
| `yy`               | 复制             |
| `pp`               | 粘贴             |
| `dd`               | 删除             |
| `:mkcd/,m`         | 创建文件夹并进入  |
| `cw`               | 重命名           |
| `I`                | 前重命名          |
| `A`                | 后重命名          |
| `:bulkrename`      | 批量重命名        |
| `:shell <command>` | 执行shell命令     |
| `空格`              | 单选             |
| `v`                | 全选/反选         |
| `V`                | 进入/退出多选模式 |
| `:extracthere/,c`  | 解压缩           |
| `:compress/,x`     | 压缩             |

### 书签

| ranger命令 |   功能   |
| ---------- | -------- |
| `m`        | 新建书签 |
| \`         | 打开书签 |
| `um`       | 删除书签 |

### 标签

|      ranger命令       |   功能   |
| -------------------- | -------- |
| `gn/<c-n>`           | 添加标签 |
| `TAB/<s-TAB>`        | 切换标签 |
| `<a-right>/<a-left>` | 切换标签 |
| `gc/<c-w>`           | 关闭标签 |


### 其他

|        ranger命令        |                           功能                           |
| ----------------------- | -------------------------------------------------------- |
| `zh`                    | 显示隐藏文件                                              |
| `zp`                    | 打开/关闭文件预览功能                                     |
| `zP`                    | 打开目录预览功能                                          |
| `zf`                    | 过滤器(如过滤pdf文件, zf+pdf,回车)                        |
| `S`                     | 在当前目录打开终端                                        |
| `z(*)`                  | 改变设置, *表示在弹出选项中的选择                          |
| `o(*)`                  | 改变排序方式                                              |
| `!/s `                  | 使用shell命令(！shell -w ls -hl %s,%s代表当前被选中的文件) |
| `:`                     | 使用ranger命令(? 查看可用命令)                            |
| `:set colorscheme snow` | 设置颜色模式                                              |
| `/`                     | 搜索                                                     |
| `:fzf_select/,f`        | 搜索                                                     |

### 快速预览

|       所需程序        | 可预览文件格式 |
| -------------------- | ------------- |
| `elinks/w3m`         | html          |
| `highlight`          | text/code     |
| `img2txt/caca-utils` | 图片          |
| `atool`              | 压缩包         |
| `pdf2text/poppler`   | pdf           |
| `mediainfo`          | 多媒体文件预览 |
| `catdoc`             | doc预览       |
| `docx2txt`           | docx预览      |
| `xlsx2csv`           | xlsx预览      |
