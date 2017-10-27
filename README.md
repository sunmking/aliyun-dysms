# aliyun-dysms

## 安装

```bash
composer require "saviorlv/aliyun-dysms:dev-master"
```

> or添加下列代码在composer.json文件中并执行composer update 操作

```bash
{
    "require": {
       "saviorlv/aliyun-dysms":"dev-master"
    }
}
```

## 设置方法

> 代码中调用（调用短信发送接口示例）

```bash
    $accessKeyId = '2w2w2';
    $accessKeySecret = '2w2w2w2w2w';
    $obj = new Sms($accessKeyId,$accessKeySecret);
    $response = $obj->sendSms(
        "孙坤峰", // 短信签名
        "SMS_76350132", // 短信模板编号
        "13673715134", // 短信接收者
        Array(  // 短信模板中字段的值
            "code"=>"12345",
            "product"=>"dsd"
        ),
        "123"
    );
    print_r($response);
```
