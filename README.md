# 研究生时期资料
## 项目历程
### （一）中核北方核燃料元件有限公司 - IOT物联网平台元件检测系统的研发 - (2023.02-2023.10)
- **项目概述**：使用计算机视觉对燃料棒TIG焊接元件、CANDU型端塞焊接元件、导向管（六角管）元件进行区域分割和物体检测，并进行参数测量。对处理结果进行数据传输和导出，设计GUI界面和人机交互逻辑。
- **项目技术栈**：图像处理算法，YOLOv8，U-Net，PyQt，线程管理，程序打包。
- **责任描述**：
  
  **焊接元件参数获取部分**
  1. 利用像素差异对元件数据进行分类，识别数据图像上的比例标尺。
	2. 训练U-Net网络获取元件的边界数据，设计拟合方法获取燃料棒、导向管元件管边方程。
	3. 训练YOLOv8网络获取燃料棒、导向管元件焊接头坐标，端塞焊元件焊接线长度。
	4. 设置阈值，对端塞焊元件边界数据进行循环判断，得出管边线数据，获取数据均值（即为截距），对数据去均值化拟合，得到斜率。
	5. 继续在管边线数据上进行二次拟合，判断二次项变号情况，找到畸变点。
	6. 整合上述数据，进行数值计算和图像绘制，与元件国际标准对比，判断是否合格。

  **人机交互设计部分**
	1. 检测过程中数据实时传输至UI界面，工程人员能够实时查看。
	2. 设计有修订功能，可使用鼠标滑动、点击进行元件数据的重测量和修订。
	3. 设计放缩、查看、选择图像数据、数据导出、修订等按钮，并配置专属快捷键。
	4. 多线程操作，并发处理，元件检测与前端人员操作互不影响。
	5. 数据按格式一键式导出为EXCEL本地存储，历史数据查看。
	6. 报错弹框防止崩溃，Debug报错信息本地存储等。
	7. 整套程序打包为.exe可执行文件，能够在GPU或单CPU设备(Windows系统)进行安装调试。

### （二）新疆金风科技股份有限公司 - 基于计算机视觉的风机叶片缺陷检测系统开发 - (2022.8 - 2022.12)
- **项目概述**：使用深度学习算法对无人机采集的风机视频中叶片存在缺陷进行识别分类，对处理结果进行数据传输，设计GUI界面和人机交互逻辑，并对存在的缺陷进行数据导出。
- **项目技术栈**：ResNet，tkinter，程序打包。

- **责任描述**：
  
  **视频数据检测处理** 
	1. 读取视频数据，设计循环对视频数据进行分帧操作，对视频帧进行A、B、C分叶片命名。
	2. 训练ResNet网络对叶片上的：裂纹、划痕、针眼、正常等类别进行分类。

  **人机交互设计部分**
	1. UI界面设计有数据选取、数据导出、历史数据查看等按钮。
	2. 检测过程中，待检叶片、风机号等数据会展示在UI界面上，允许工程人员实时查看。
	3. 数据按格式一键式导出为EXCEL本地存储，历史数据查看。
	4. 报错弹框防止崩溃，Debug报错信息本地存储。
	5. 整套程序打包为.exe可执行文件，能够在GPU或单CPU设备(Windows系统)进行安装调试。

###  （三）天汇风电有限公司 - 风电场关键装备“图-声-热”大数据智能采集与分析平台的研发与应用 - (2023.10 - 2026.10) （未结项）
<font color=#00ffff size=72> color=#00ffff </font>



## 自我描述
