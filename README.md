# Installing TensorFlow on Windows10 with gpu
用Anaconda 安裝tensorflow-gpu
## CUDA Toolkit 9.0 Downloads windows10_x64 :<br/> ##
https://developer.nvidia.com/cuda-90-download-archive?target_os=Windows&target_arch=x86_64&target_version=10<br/>
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-10_144237.png) <br/>
一直安裝到底就可以了

## Downloads cuDNN v7.0 dll :<br/> ##
https://developer.nvidia.com/cudnn
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-10_150151.png)
***確定環境變數名稱 `PATHEXT`裡包含 `.DLL` <br/>***
對本機右鍵->內容->變更設定->系統內容(進階)->環境變數->`PATHEXT`
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-11_182727.png)
***解壓縮 cuDNN 後將以下檔案直接覆蓋到 (預設路徑) C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0 <br/>***
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-10_165850.png)<br/>
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-11_171331.png)<br/>
## 下載 Anaconda windows10_64 python 3.6 version :<br/> ##
https://repo.anaconda.com/archive/Anaconda3-5.1.0-Windows-x86_64.exe 第一次安裝一直用下一步設定就好 <br/>

**Anaconda裡也支援vscode囉! 可以自行決定要不要安裝 <br/>**
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-10_152212.png)<br/>

## 在Anaconda 裡面安裝python 與設定 tensorflow 環境 :<br/> ##
執行 `Anaconda Prompt bash`  
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/%E6%93%B7%E5%8F%96.PNG)  
**1. 用以下指令創建一個 conda 的工作環境叫做 "tensorflow" <br/>**
```conda create -n tensorflow pip python=3.6 ```  <br/>
**2. 用以下指令啟用 conda tensorflow 環境 <br/>**
```activate tensorflow```  <br/>
**3. 用以下指令安裝 gpu版本的 tensorflow <br/>**
```pip install --ignore-installed --upgrade tensorflow-gpu``` <br/>
**4. 執行程式碼表示驗證成功 <br/>**
```
import tensorflow as tf  
hello = tf.constant('Hello, TensorFlow!') 
sess = tf.Session()  
print(sess.run(hello))  
```  
**5. 最後執行 Anaconda Navigator 改變環境執行你要的IDE <br/>**
![](https://github.com/Tai-liang-Zhou/Natural-Language-Processing/blob/master/2018-05-11_183522.png)<br/>
