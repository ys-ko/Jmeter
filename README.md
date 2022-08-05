# Jmeter

### 1. Apache Jmeter?

- Web Application 성능 분석, 측정을 하기 위한 부하 테스트 도구
- URL : [https://jmeter.apache.org/](https://jmeter.apache.org/)

### 2. Requirements

- Java 8+

### 3. 설치

1) Mac

```bash
$ brew install jmeter --with-plugins
$ open /usr/local/bin/jmeter
```

2) Windows

- [https://jmeter.apache.org/download_jmeter.cgi](https://jmeter.apache.org/download_jmeter.cgi)
- Jmeter 설치 경로 -> bin -> jmeter.bat 실행

### 4. Jmeter 설정

1) Test Plan 설정

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eafe872d-fb0c-467f-a204-7e84ce0df9ea/Untitled.png)

2) Thread Group 생성

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7ebc8aee-f04a-4049-a593-e01de543c46b/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d090ed7d-0baf-49fe-b28b-c762a6798ec5/Untitled.png)

- **Number of Threads(users)**가상의 생성자를 몇 명으로 설정할건지에 대한 값이다. (= 몇 개의 쓰레드를 생성할 것인지의 값이다)이 값이 커질수록 당연히 서버는 많은 부하를 받을 것이다.
- **Ramp-up Period(in seconds)**한번의 실행을 몇초 동안 완료 시킬것인지에 대한 설정값
- **Loop Count**반복하고자 하는 횟수, Infinite를 누르면 무제한 실행.
    - **Same user on each iterator** 첫 번째 응답에서 얻은 쿠키를 다음 요청에도 사용
    - **Delay Thread creation until needed** Number of Threads에 설정된 수 만큼 Thread가 생성되면 테스트를 시작
    - **Specify Thread lifetime**
        - **Duration** 테스트 시간을 초 단위 설정
        - **Startup Delay** 설정 시간 이후 테스트 시작

3) Sampler 생성 (http request)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9becc4d-8a92-4466-8625-58e6ce7e895c/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/166b670b-f3f4-49a0-b08a-4060edb4a385/Untitled.png)

4) Listener 생성

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2380420f-12d5-4182-b116-cfa73e330d15/Untitled.png)

4-1) Listener 예시 (Summay Report)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c39a355-f833-4748-a9ae-1085a921ea52/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b3c04c31-fd11-49b0-905f-2e03e8e2683a/Untitled.png)

4-2) Listener 예시 (Transactions per Second)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/67c7f163-7d9e-4843-8c7b-19df5718c904/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6f56d8c5-6927-4887-ab3d-5e6ae1756087/Untitled.png)
