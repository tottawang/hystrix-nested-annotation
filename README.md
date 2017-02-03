# hystrix-nested-annotation

### Run and build
Step-1: 
./gradlew clean build

Step-2:
* export HYSTRIX_TEST_URL=ANY_TEST_GET_ENDPOINT
* java -jar build/libs/sample-0.0.1-SNAPSHOT.jar

Step-3:
* curl http://localhost:{server_ip}/api/hystrix-get
* curl http://localhost:{server_ip}/api/hystrix-self-invocation
* curl http://localhost:{server_ip}/api/hystrix-self-invocation-annotation


###  Output: You will see that selfInvocation call is not wrapped by hystrix
hystrix-HttpWebClientPool-1: getContent call<br/>
hystrix-HttpWebClientPool-2: selfInvocationWithAnnotation call<br />
hystrix-HttpWebClientPool-2: getContent call<br/>
http-nio-8082-exec-2: selfInvocation call<br/>
http-nio-8082-exec-2: getContent call<br/>

