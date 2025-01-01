## Stable Diffusion WebUI

#### 代码说明

文件：stable-diffusion-webui.zip

描述：Stable Diffusion模型部署核心文件。

#### 运行环境

Pytorch、Numpy等库

见Stable Diffusion.yml

#### 运行方法

使用Anaconda配置好名为Stable的Stable Diffusion运行环境，然后将CheckPoint模型放入根目录中的\models\Stable-diffusion目录中，将LoRA模型放入\models\Lora中，然后执行:

``` 
conda activate stable 启动环境
python run.py --api 启动WebUI的API模式
```



## 后端服务器

#### 代码说明

文件：SD_WEB.zip

描述：后端服务器源码，连接前端、数据库、SD WebUI

#### 运行环境

Flask、Json、PIL等库

详细见Backend.yml

#### 运行方法

使用Anaconda配置好名为web的Flask运行环境，然后执行:

``` 
conda activate web 启动环境
python run.py --port=8000 启动后端服务器
```



## 前端页面

#### 代码说明

文件：SD_VUE.zip

描述：项目前端代码

#### 运行环境

Vue、Node.js

#### 运行方法

``` 
npm run serve
```



##  [风格样例.pdf](风格样例.pdf)

描述：每种作图风格的样例图片以及使用的LoRA和Prompt模板。



##  [API文档.html](API文档.html) 

描述：后端服务器设计的所有API接口描述，以及使用的参数说明。（由于Apifox导出功能不完善，内容存在缺失）
