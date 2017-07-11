# imooc-requests
python requests course for pythonists

本项目是参考的[Python-走进Requests库](http://www.imooc.com/learn/736)课程，了解更多课程信息点击链接即可访问。

# learn_requests
  通过简单的requests类库的学习，理解HTTP基本原理，并能够纯熟地使用requests和Github API进行数据交互。除此之外，你还能够获得诸如HTTP认证，Oauth授权等进阶知识和技能.

## 文档
- Requests的官方下载：kennethreitz/[requests](https://github.com/kennethreitz/requests)
- Requests的官方文档：[Requests](http://docs.python-requests.org/en/master/)
- Github的API开发文档：[users](https://developer.github.com/v3/users/)
- [HTTP协议](https://zh.wikipedia.org/wiki/%E8%B6%85%E6%96%87%E6%9C%AC%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE)

## 1、需要的运行环境：
- 认识Requests库
- Ubuntu14.04、Python2.7、Requests、pip、virtualenv、gunicorn、httpbin等

## 2、[HTTP协议](https://zh.wikipedia.org/wiki/%E8%B6%85%E6%96%87%E6%9C%AC%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE)：
- 特点：无状态、分布式、协作式、超文本信息系统
```
  The Hypertext Transfer Protocol (HTTP) is an application protocol for distributed, collaborative, hypermedia information systems.
```
- 流程：Requests、Response
- urllib、urllib2、urllib3
```
  Requests支持urllib3的“Keep-alive”连接方式。
```

## 3、请求方法：
```
  OPTIONS：这个方法可使服务器传回该资源所支持的所有HTTP请求方法。
  HEAD：与GET方法一样，都是向服务器发出指定资源的请求。只不过服务器将不传回资源的本文部分。
  GET：向指定的资源发出“显示”请求。
  POST：向指定资源提交数据，请求服务器进行处理（例如提交表单或者上传文件）。
  PUT：向指定资源位置上传其最新内容。
  DELETE：请求服务器删除Request-URI所标识的资源。
  TRACE：回显服务器收到的请求，主要用于测试或诊断。
  CONNECT：HTTP/1.1协议中预留给能够将连接改为管道方式的代理服务器。通常用于SSL加密服务器的链接（经由非加密的HTTP代理服务器）。
  方法名称是区分大小写的。
  HTTP服务器至少应该实现GET和HEAD方法，其他方法都是可选的。当然，所有的方法支持的实现都应当匹配下述的方法各自的语义定义。此外，除了上述方法，特定的HTTP服务器还能够扩展自定义的方法。例如：
  PATCH（由 RFC 5789 指定的方法）:用于将局部修改应用到资源。
```
- 带参数的请求：
- 请求异常处理：
- 自定义Request：

## 4、处理响应：
- 状态代码的第一个数字代表当前响应的类型：
```
    1xx消息——请求已被服务器接收，继续处理
    2xx成功——请求已成功被服务器接收、理解、并接受
    3xx重定向——需要后续操作才能完成这一请求
    4xx请求错误——请求含有词法错误或者无法被执行
    5xx服务器错误——服务器在处理某个正确请求时发生错误
```
- Response库：status_code、reason、headers、url、history（重定向）、elapsed（耗时）、request
- 响应体：encoding、raw（原始对象）、content（流）、text（解析后的）、json
- 事件钩子（Event Hooks）：需要用到回调函数

## 5、进阶话题：
- HTTP认证
- Proxy代理
- Session和Cookie
