# camel-performance-test-monitoring

- execute test in https://github.com/apache/camel-performance-tests/tree/main/profiling that generates a .jfr file record
- run `docker-compse up` in order to start jfr-datasource and grafana with preconfigured datasource and dashboard
- run `curl -F "file=@/path/to/recording.jfr" "localhost:8080/load"` where `/path/to/recording.jfr` is the path to the jfr generated in step 1
- wait 20s so that grafana will poll metrics from jfr-datsource
- go to grafana dashboard camel-jfr to observe results

![image](https://user-images.githubusercontent.com/34543311/144095421-2bc8652c-bdb9-41ac-b8eb-bef3b3372d94.png)
