# Web可视化开发 {#concept_zkh_bpk_bhb .concept}

Web可视化开发是物联网Web开发工具。无需写代码，只需在编辑器中，拖拽组件到画布上，再配置组件显示样式、数据源和动作，即以可视化开发的方式完成Web应用开发，并可批量进行设备绑定。适用于开发设备监测/控制面板、设备数据分析报表等。

## 功能特点 {#section_bvx_wgq_bhb .section}

-   简单易用。Web可视化工作台与物联网平台的设备接入能力、物模型能力无缝衔接。无需写代码，您就可以调用设备数据，进行设备控制。

-   无需额外购买服务器和数据库，应用搭建完毕即可预览、使用，支持绑定自己的域名对最终用户进行分发。

-   页面或应用创建完毕后，可以直接应用在多个地方。同时，IoT Studio支持批量更换绑定设备。


## 使用案例 {#section_gg2_f4r_bhb .section}

下文以配置一个家居设备控制面板为例，介绍Web可视化开发过程。

1.  在物联网平台控制台左侧导航栏，单击**开发服务** \> **IoT Studio**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806240725_zh-CN.png)

2.  在物联网开发页，单击右上角**新建项目**按钮，然后新建一个项目。

3.  项目创建成功后，导入或创建使用该物联网开发项目的产品，并为该产品定义功能（即物模型TSL）。

    -   导入产品：在项目页面，单击**项目概览** \> **导入产品**，再选择要导入的产品。产品导入后，该产品下的所有设备均被导入项目中。

    -   创建产品：在项目页面，单击**产品** \> **新建产品**。新建产品后，还需为产品定义功能（即物模型）。请参见[新建产品](../../../../cn.zh-CN/用户指南/产品与设备/创建产品.md#)和[新增物模型](../../../../cn.zh-CN/用户指南/产品与设备/物模型/新增物模型.md#)。

    **说明：** 可为一个项目导入或创建多个产品。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806240758_zh-CN.png)

4.  选择**Web可视化开发**。

5.  在Web可视化开发页，鼠标光标移至**选择模板**下的区域，单击出现的**使用该模板开发**按钮，然后新建一个Web可视化应用。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806240727_zh-CN.png)

    新建Web可视化应用：

    |参数|描述|
    |:-|:-|
    |应用名称|设置应用名称。支持中文汉字、英文大小写字母、数字、部分常用符号：下划线\(\_\)，连字符\(-\)，括弧，和空格；必须以中文汉字、英文字母或数字开头；长度不超过40个字符（一个中文汉字算一个字符）。|
    |所属项目|选择该应用所属的物联网开发项目。|
    |描述|描述该应用。长度不超过100字符（一个中文汉字算一个字符）。|

6.  自定义新增页，即编辑应用。

    应用创建成功后，页面自动跳转至该应用的编辑页。在此页上，您可以新增自定义页面，并拖拽左侧的组件到画布上。然后，在页面右侧，配置组件的显示样式、数据来源和要执行的动作。

    **说明：** Web可视化编辑器暂时不支持自动保存，请随时保存设置。

    可视化编辑应用操作过程：

    1.  定义应用页面背景和页面分辨率。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806240734_zh-CN.png)

        -   设置页面背景：您可以选择背景颜色或上传本地图片作为背景。

            **说明：** 建议上传的图片分辨率是页面分辨率的2倍，以保证在手机上看到的背景图片是清晰的。

        -   设置页面分辨率：支持选择提供的分辨率和自定义分辨率。

            **说明：** 设置或调整页面分辨率后，所有新建的页面画布都遵循该分辨率。

            H5分辨率参考：

            -   iPhone8尺寸 ：375\*667
            -   iPhone 8 Plus尺寸：736\*414
            -   iPhone XS尺寸：812\*375
            -   iPhone XR 和iPhone XS Max尺寸：896\*414
            -   Android尺寸：640\*360
    2.  设置页面标题。

        从左侧可视化组件中，拖拽一个**文字**组件到画布上。然后，在右侧操作栏中，输入文字内容和设置文字样式。

    3.  设置时间组件。

        从左侧可视化组件中，拖拽一个**时钟**组件到画布上，并设置时钟组件的展示样式。

        ![](images/40746_zh-CN.gif)

        |参数|描述|
        |:-|:-|
        |展示格式|选择时钟组件展示的时间格式。可选：日期时间、时间、日期。|
        |背景颜色|时钟组件的背景颜色。时钟组件默认带背景。如果想要去掉背景，可设置背景颜色不透明度为0，即将背景颜色不透明度滑块滑至最左侧。

|
        |文字样式|设置时间文字的字号、颜色和粗细。|
        |边框|设置时间组件的边框显示效果。时钟组件默认带边框。如果想要去掉边框，将边框粗细设置为0即可。

|

    4.  添加灯泡开关。

        1.  从左侧可视化组件中，拖拽一个**开关**组件到画布上。

            ![](images/40750_zh-CN.gif)

        2.  设置开关显示样式。可选：

            -   开关icon：选择为开关icon，即显示效果为组件本身样式。您需为开关的ON状态和OFF状态设置显示颜色。

            -   图片：选择为图片，即您自定义开关的显示样式。您需为开关的ON状态和OFF状态分别上传状态显示图片。以上GIF图中，选择为图片。

        3.  设置开关组件标题。

            拖拽一个**文字**组件到开关组件上，然后设置文字内容和样式。

            ![](images/40756_zh-CN.gif)

        4.  （可选）如果您要设置多个相同样式的开关组件，可选中开关标题和开关图片，单击鼠标右键，选择**成组**，复制多个相同配置的组件。再选中复制的组件组，单击鼠标右键，选择**解散组**，再选中标题，更改标题名称。

            ![](images/40761_zh-CN.gif)

            ![](images/40762_zh-CN.gif)

        5.  配置开关的数据源。

            在右侧配置操作栏中，单击**数据****配置数据**。完成配置后，单击**确定**。

            ![](images/40763_zh-CN.gif)

            |参数|描述|
            |:-|:-|
            |选择产品|选择该开关组件对应的设备所属产品。|
            |选择设备|选择该开关组件对应的设备。            -   若选择了具体设备，需单击**在线模拟**，进入在线调试页，推送模拟属性值。
            -   若选择为空，需设置**设备模拟数据**进行模拟属性值推送。
|
            |设备属性|选择该开关组件对应的属性。|
            |设备模拟数据|当选择设备为空时出现的参数。需根据所选设备属性的取值范围，设置一个模拟值。

属性取值范围，请在产品详情页的功能定义中查看。

|

    5.  添加其他组件，如窗帘开关等。

    6.  单击编辑器上方**保存**按钮，保存设置。

    7.  单击编辑器上方**预览**按钮，测试应用。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806340764_zh-CN.png)

    8.  确认应用可用后，单击编辑器上方**发布**按钮，发布应用。

    9.  应用发布后，可选择**绑定域名**，绑定您自己的域名，自定义网址。

        若您暂时还没有购买域名，可以购买域名之后，打开该应用页面，单击**设置** \> **域名管理**，绑定域名。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806540765_zh-CN.png)

    10. （可选）在项目页，单击**设备管理** \> **设备**，可新增或删除设备。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/136659/155626806540766_zh-CN.png)


## 相关文档 {#section_czd_pzs_bhb .section}

-   有关Web可视化开发的其他组件介绍和配置细节，请参见[Web可视化搭建文档](https://linkdevelop.aliyun.com/studioweb-doc#index.html)。
-   设备端开发，请参见[Link Kit SDK 文档](https://help.aliyun.com/product/93051.html)。

