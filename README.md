# LabelImg Fix for Python 3.13+ (Crash & TypeError Solved)

[中文说明请往下拉 / Scroll down for Chinese version]

---

## 🇺🇸 English Guide

### 📌 What is this?
This is a patch for **labelImg** to fix compatibility issues with **Python 3.13**.
Original labelImg crashes or fails to save due to strict `float` to `int` type checking in newer Python versions.

**Fixed Issues:**
* `TypeError: expected str, bytes or os.PathLike object, not NoneType` (When saving)
* `TypeError: arguments did not match any overloaded call` (When drawing boxes)
* Zooming and scrolling crashes.

### 🚀 How to Install (Step-by-Step)

You need to replace **2 specific files** in your Python installation directory with the files from this repository.

#### Step 1: Find your Python `site-packages` folder
Locate where `labelImg` is installed. It is usually inside your Python folder:
* **Windows:** `C:\Users\YourName\AppData\Local\Programs\Python\Python313\Lib\site-packages\`
* **Mac/Linux:** `/usr/local/lib/python3.13/site-packages/`

#### Step 2: Replace the files
Download the files from this repo and overwrite the original ones in the following locations:

| File in this Repo | **Where to put it (Destination Path)** |
| :--- | :--- |
| **`labelImg.py`** | `.../site-packages/labelImg/labelImg.py` |
| **`canvas.py`** | `.../site-packages/libs/canvas.py` |

> **Note:** Please verify the folder name. `canvas.py` must go into the **`libs`** subfolder, NOT the `labelImg` folder!

#### Step 3: Run
Open your terminal and type `labelImg`. It should work perfectly now!

---

## 🇨🇳 中文说明

### 📌 这是什么？
这是 **labelImg** 标注工具在 **Python 3.13** 环境下的修复补丁。
原版软件在 Python 3.13 下会因为浮点数（float）和整数（int）的类型检查变得严格，导致**无法保存、画框闪退、缩放报错**。本补丁修复了所有这些问题。

### 🚀 使用方法 (如何替换文件)

你需要下载本仓库的两个文件，并替换你电脑里对应的原文件。

#### 第一步：找到你的安装目录
找到你 Python 的 `site-packages` 文件夹（即 labelImg 安装的地方）。
* **Windows 通常路径:** `C:\Users\你的用户名\AppData\Local\Programs\Python\Python313\Lib\site-packages\`

#### 第二步：精准替换 (请看清路径)
请将本仓库的文件覆盖到以下位置：

| 本仓库文件 | **你需要放入的目标文件夹** |
| :--- | :--- |
| **`labelImg.py`** | `.../site-packages/labelImg/labelImg.py` |
| **`canvas.py`** | `.../site-packages/libs/canvas.py` |

> **⚠️ 特别注意：**
> * `labelImg.py` 放在 `labelImg` 文件夹里。
> * `canvas.py` 必须放在 **`libs`** 这个子文件夹里！（这是最容易放错的地方）

#### 第三步：启动
重新打开终端输入 `labelImg`，即可正常使用。

---

*Fixed by [Your Name]*
