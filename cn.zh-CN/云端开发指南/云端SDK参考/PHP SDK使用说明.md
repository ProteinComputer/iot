# PHP SDK使用说明 {#reference_y3b_zwb_zdb .reference}

物联网平台提供PHP语言的云端SDK供开发人员使用。本文介绍云端PHP SDK的安装和配置，及使用PHP SDK调用云端API的示例。

## 安装IoT PHP SDK {#section_vxf_kb2_zdb .section}

1.  安装PHP开发环境。

    访问[PHP官网](http://www.php.net/)下载PHP安装包，并完成安装。

2.  下载并解压IoT PHP SDK软件包。

    访问[IoT PHP SDK下载地址](https://github.com/aliyun/aliyun-openapi-php-sdk/tree/master/aliyun-php-sdk-iot)下载PHP SDK 包，然后解压下载的软件包到指定的目录。PHP SDK 是一个软件开发包，不需要进行安装操作。


## 初始化SDK {#section_mp5_jd2_zdb .section}

初始化SDK示例

```
<?php
include_once 'aliyun-php-sdk-core/Config.php';
use \Iot\Request\V20180120 as Iot;
//设置你的AccessKeyId/AccessSecret/ProductKey
$accessKeyId = "";
$accessSecret = "";
$iClientProfile = DefaultProfile::getProfile("cn-shanghai", $accessKeyId, $accessSecret);
$client = new DefaultAcsClient($iClientProfile);
```

accessKeyId即您的账号的AccessKeyId，accessSecret即AccessKeyId对应的AccessKeySecret。您可在[阿里云官网控制台AccessKey管理](https://ak-console.aliyun.com)中创建或查看您的AccessKey。

## 发起调用 {#section_fcq_qd2_zdb .section}

物联网平台云端API，请参见[API列表](intl.zh-CN/云端开发指南/云端API参考/API列表.md#)。

以调用Pub接口发布数据到设备为例。

```
$request = new Iot\PubRequest();
$request->setProductKey("productKey");
$request->setMessageContent("aGVsbG93b3JsZA="); //hello world Base64 String.
$request->setTopicFullName("/productKey/deviceName/get"); //消息发送到的Topic全名.
$response = $client->getAcsResponse($request);
print_r($response);
```

