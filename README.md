### 1、本示例的 Python 版本为2.7
### 2、本demo主要是为了提供签名方法，调用示例可以参考 ClientDemo.py 文件
### 3、使用注意事项：
- 含有中文和空格的query, body在请求时需要对值进行urlencode处理，编码为utf-8.
- 参数参与签名时，必须使用原文签名，不能用urlencode后字符串的进行签名.所以请在签名之后再对query、body的值做urlencode.
- [签名文档](http://https://help.aliyun.com/document_detail/29475.html)
### 4、说明：没设置忽略检查ssl证书，会返回三个none。尝试通过路径导入ca证书,出现证书验证不成功。因此增加了设置忽略检查 SSL 证书有效性，由于忽略后会有请求被劫持的安全风险，最好只在测试时使用。