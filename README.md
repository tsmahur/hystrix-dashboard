# hystrix-dashboard
  This ms is monitor Api-Gateway hystrix stream . This is a part of [ms-eureka-gateway-hysrtix-cloud-config](https://github.com/tsmahur/ms-eureka-gateway-hysrtix-cloud-config) Project.
  It will load yml properties from [configurations-server](https://github.com/tsmahur/configurations-server)
##
### Dependency
    eureka client, spring-cloud-starter-netflix-hystrix-dashboard
    spring-cloud-starter-config

### application.yml
    port, name, hystrix-dashboard, eureka client(same in all MS)
    config:import: optional:configserver:http://localhost:8094

### main application class
    @EnableEurekaClient, @EnableHystrixDashboard	

### EndPoints
    http://localhost:8092/actuator/hystrix.stream  -> API gateway hystrix stream

    http://localhost:8093/hystrix -> give above stream to monitor using hystrix dashboard

   *Hit api's endpoint and check in dashboard , also test fallback by making down any of MS*
