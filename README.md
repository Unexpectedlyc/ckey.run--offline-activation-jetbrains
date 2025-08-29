# Windows|Linux|MacOS采用ckey.run离线激活jetbrains全家桶教程

> [!IMPORTANT]
>
> 验证在IntelliJ IDEA 2025.1.4.1版本上生效，mac跟linux下操作步骤相似

## 一、离线安装教程

### 1.将ckey.run保存为本地脚本

在联网环境的powershell管理员权限下执行下面的命令

#### Windows:

```powershell
cd C:\
irm ckey.run | Out-File -FilePath "ckey.run.ps1" -Encoding UTF8
```

执行完后会在你的c盘下生成一个ckey.run.ps1文件

#### Linux

```shell
wget -q ckey.run -O ckey.run
```

执行完后会在你的当前目录下出现一个文件ckey.run

#### MacOS

```shell
curl -Ls ckey.run -o ckey.run
```

执行完后会在你的当前目录下出现一个文件ckey.run

### 2.打开脚本，注释下面几行

#### Windows:

打开ckey.run.ps1

```powershell
 #Create_Work_Dir
 #File_Download
```

Linux/MacOS:

打开ckey.run

```bash
#do_create_work_dir
#do_download_resources
```



### 3.在联网环境中执行下面的命令

#### Windows:

```powershell
irm ckey.run|iex
```

这个命令执行完后，可以在C:\Users\Public这个目录下看到一个.jb_run的文件夹

#### Linux/MacOS:

```bash
bash ckey.run
```

这个命令执行完如果是linux用户会在/root目录下看到.jb_run的文件夹，macOS用户是在/Users/${YOUR_USER_NAME}目录下看到.jb_run的文件夹。

### 4.将文件拷贝到离线环境中

1. 将第2，3步得到的文件拷贝到离线机器中，Windows将.jb_run文件夹拷贝到离线机器中C:\Users\Public目录下。linux拷贝到root下，mac拷贝到/Users/${YOUR_USER_NAME}目录下
2. windows以管理员身份运行ckey.run.ps1文件,linux/macOS运行bash ckey.run
3. 去[ckey.run官网](https://ckey.run/)复制对应产品的激活如果需要的话

> [!NOTE]
>
> 完成以上步骤即可离线激活成功

#有用的话给个star✨,谢谢

