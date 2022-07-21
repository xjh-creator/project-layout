1. /internal/某个应用/api/v1：HTTP API 接口的具体实现，主要用来做 HTTP 请求的解包、参数校验、业务逻辑处理、返回。注意这里的业务逻辑处理应该是轻量级的，如果业务逻辑比较复杂，代码量比较多，建议放到 /internal/apiserver/service 目录下。该源码文件主要用来串流程。
2./internal/某个应用/options：应用的 command flag。
3. /internal/某个应用/config：根据命令行参数创建应用配置。
4. /internal/某个应用/service：存放应用复杂业务处理代码。
5. /internal/某个应用/store/mysql：一个应用可能要持久化的存储一些数据，这里主要存放跟数据库交互的代码，比如 Create、Update、Delete、Get、List 等。