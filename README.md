# MicroServiceTest
测试天气预报系统
collection   8083 定时采集数据到redis
report 8084  最终消费者，呈现给用户的
server 8761 eureka监控端
zuul  8089  网关
city 8081 负责加载城市列表
data 8082 通过id查找城市天气

最先启动redis
启动时先启动sever，然后启动city和data和zuul，collection和report最后启动，可能拿不到数据需要重新启动collection
访问方法是通过report微服务进行访问
例：http://localhost:8084/report/cityId/101280206
