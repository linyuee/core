###核心代码模块
http模块使用方法：
```
$response = \Linyuee\Http\HttpHelper::curl('10.8.8.99/v4_1/upload_complete','POST',$params,$header);
$body = $response->getBody();
```
生成签名字符串使用方法
```
$sign_str = \Linyuee\Auth\Signature::SignMd5($params,$access_key_secret)
```
异常模块使用方法
```
throw new \Linyuee\Exception\ApiException('message','UNKNOWN_ERROR',400);