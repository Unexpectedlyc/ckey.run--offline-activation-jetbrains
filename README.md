<p align="center">
<br>
        <a href="README_CN.md">中文</a> &nbsp ｜ &nbsp English &nbsp
</p>

# Offline Activation Tutorial for JetBrains Suite Using ckey.run on Windows | Linux | macOS

> [!IMPORTANT]
>
> Verified to work with IntelliJ IDEA 2025.1.4.1

## Part 1: Offline Installation Guide

### 1. Save ckey.run as a Local Script

Run the following command in an administrator PowerShell (on Windows) or terminal (on Linux/macOS) with internet access.

#### Windows:

```powershell
cd C:\
irm ckey.run | Out-File -FilePath "ckey.run.ps1" -Encoding UTF8
```

After execution, a file named `ckey.run.ps1` will be created on your C: drive.

#### Linux:

```shell
wget -q ckey.run -O ckey.run
```

After execution, a file named `ckey.run` will appear in your current directory.

#### macOS:

```shell
curl -Ls ckey.run -o ckey.run
```

After execution, a file named `ckey.run` will appear in your current directory.

---

### 2. Open the Script and Comment Out the Following Lines

#### Windows:

Open `ckey.run.ps1` and comment out:

```powershell
 #Create_Work_Dir
 #File_Download
```

#### Linux / macOS:

Open `ckey.run` and comment out:

```bash
#do_create_work_dir
#do_download_resources
```

---

### 3. Execute the Following Command in an Online Environment

#### Windows:

```powershell
irm ckey.run | iex
```

After running this command, you will find a `.jb_run` folder in `C:\Users\Public`.

#### Linux / macOS:

```bash
bash ckey.run
```

After execution:
- Linux users: the `.jb_run` folder will be created in the `/root` directory.
- macOS users: the `.jb_run` folder will be created in `/Users/${YOUR_USER_NAME}`.

---

### 4. Copy Files to the Offline Environment

1. Copy the files obtained in Steps 2 and 3 to the offline machine:
   - **Windows**: Copy the `.jb_run` folder to `C:\Users\Public`.
   - **Linux**: Copy to the `/root` directory.
   - **macOS**: Copy to `/Users/${YOUR_USER_NAME}`.

2. On the offline machine:
   - **Windows**: Run `ckey.run.ps1` as Administrator.
   - **Linux/macOS**: Run `bash ckey.run`.

3. Visit the [ckey.run official website](https://ckey.run/) and copy the activation code for your desired product, if required.

> [!NOTE]
>
> After completing the above steps, offline activation should be successful.

# If you find this helpful, please give a star ✨, thank you!
## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Unexpectedlyc/ckey.run--offline-activation-jetbrains&type=Date)](https://www.star-history.com/#Unexpectedlyc/ckey.run--offline-activation-jetbrains&Date)
