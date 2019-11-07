一个yago程序的配置文件

```bash
[app]

app_name = "app"
env = "dev"
debug = true
# 如果不设置则不会创建 pidfile
# pidfile = "/var/run/app.pid"

# 是否开启http服务
http_enable = true
# http服务地址
http_addr = ":8080"
# http服务关闭最大等待时长, 秒
http_stop_time_wait = 10

# http ssl config
# http_ssl_on = true
# http_cert_file = "./yourdomain.crt"
# http_key_file = "./yourdomain.key"

# cors 跨域
# http_cors_allow_all_origins = true
# http_cors_allow_origins = []
# http_cors_allow_methods = ["GET", "POST", "PUT", "PATCH", "DELETE", "HEAD"]
# http_cors_allow_headers = ["Origin", "Content-Length", "Content-Type"]
# http_cors_expose_headers = []
# http_cors_allow_credentials = true
# http_cors_max_age = "12h"

# gzip 模式 1:Default, 2:Best Speed, 3:Best Compression
# http_gzip_on = true
# http_gzip_level = 1

# pprof route: /debug/pprof
# http_pprof_on = false

# http html 模版配置
# http_view_render = true
# http_view_path = "views/*"
# http_static_path = "static/js"

# 是否开启rpc服务
rpc_enable = true
# rpc服务地址
rpc_addr = ":50051"
# rpc服务关闭最大等待时长, 秒
rpc_stop_time_wait = 10
# rpc reflection
# rpc_reflect_on = true

# rpc ssl config
# rpc_ssl_on = true
# rpc_cert_file = "./conf/server.pem"
# rpc_key_file = "./conf/server.key"

# 是否开启task任务
task_enable = true
# http服务关闭最大等待时长, 秒
task_stop_time_wait = 10

##########################################
#  以下自定义配置区
##########################################

##########################################
# 以下是组件区
##########################################

[logger]
# json | text, default text
formatter = "json"
# 日志最低等级 Panic = 0, Fatal = 1, Error = 2, Warn = 3, Info = 4, Debug = 5, Trace = 6
level = 5
# 文件路径
file_path = "./logs/app.log"
# 最大保留的备份数
max_backups = 20
# 日志最大保留天数
max_age = 30
# 文件最大大小(mb)
max_size = 500
# 是否开启压缩
compress = true
# write log to stdout
# stdout_enable = true

[db]
host = "127.0.0.1"
user = "user"
password = "password"
port = "3306"
database = "db"
prefix =""
timezone = "Asia/Shanghai"
charset = "utf8"
max_life_time = 8
max_idle_conn = 20
max_open_conn = 500
show_log = true

[redis]
addr = "127.0.0.1:6379"
auth = ""
db = 0
max_idle = 5
idle_timeout = 30

[mongodb]
# https://docs.mongodb.com/manual/reference/connection-string/
mongodb_uri = "mongodb://user:password@127.0.0.1:27017/?connectTimeoutMS=5000&socketTimeoutMS=5000&maxPoolSize=100"
database = "test"

[kafka]
cluster = "127.0.0.1:9092"
topic = "demo"
topic_cloud = "cloud"

##########################################
# 以下是 api 区
##########################################

[home_api]
domain = "http://127.0.0.1:8080"
hostname = "localhost"
rpc_address = "127.0.0.1:50051"
timeout = 10
max_recv_msgsize_mb =  10
max_send_msgsize_mb =  10
# ssl_on = true
# cert_file = "./conf/server.pem"

```