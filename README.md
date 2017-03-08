# httpsqs
毛雨平-转载

HTTPSQS（HTTP Simple Queue Service）是一款基于 HTTP GET/POST 协议的轻量级开源简单消息队列服务，使用 Tokyo Cabinet 的 B+Tree Key/Value 数据库来做数据的持久化存储。

项目网址：http://code.google.com/p/httpsqs/
使用文档：http://blog.zyan.cc/httpsqs/
使用环境：Linux（同时支持32位、64位操作系统，推荐使用64位操作系统）
软件作者：张宴

队列（Queue）又称先进先出表（First In First Out），即先进入队列的元素，先从队列中取出。加入元素的一头叫“队头”，取出元素的一头叫“队尾”。利用消息队列可以很好地异步处理数据传送和存储，当你频繁地向数据库中插入数据、频繁地向搜索引擎提交数据，就可采取消息队列来异步插入。另外，还可以将较慢的处理逻辑、有并发数量限制的处理逻辑，通过消息队列放在后台处理，例如FLV视频转换、发送手机短信、发送电子邮件等。

HTTPSQS 具有以下特征：

● 非常简单，基于 HTTP GET/POST 协议。PHP、Java、Perl、Shell、Python、Ruby等支持HTTP协议的编程语言均可调用。

● 非常快速，入队列、出队列速度超过10000次/秒。

● 高并发，支持上万的并发连接，C10K不成问题。

● 支持多队列。

● 单个队列支持的最大队列数量高达10亿条。

● 低内存消耗，海量数据存储，存储几十GB的数据只需不到100MB的物理内存缓冲区。

● 可以在不停止服务的情况下便捷地修改单个队列的最大队列数量。

● 可以实时查看队列状态（入队列位置、出队列位置、未读队列数量、最大队列数量）。

● 可以查看指定队列ID（队列点）的内容，包括未出、已出的队列内容。

● 查看队列内容时，支持多字符集编码。

● 源代码不超过800行，适合二次开发。
