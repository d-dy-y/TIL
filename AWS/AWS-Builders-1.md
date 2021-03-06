## AWS와 함께하는 클라우드 컴퓨팅

### 1. Cloud Computing 이란?
- **초기 투자**나 **장기 계약 없이**
- **인터넷**을 통해 **IT리소스**와 **애플리케이션**을
- **원할 때 언제든지(on-demand)**
   ```
  <-> On-Premise : 기업의 서버를 클라우드 같은 원격 환경에서 운영하는 방식이 아닌, 자체적으로 보유한 전산실 서버에 직접 설치해 운영하는 방식
  ```
- **사용한 만큼만 요금을 내는** 서비스!

  #### <6가지 이점>
  #### [1] 초기 선투자 비용 없음
  - 고정비용을 가변비용으로 대체. 미리 서버를 구매할 필요 없음
  #### [2] 운영 비용 절감
  - 사용한 만큼만 지불하며 규모의 경제로 인한 지속적인 비용 절감   
  #### [3] 탄력적인 운영 및 확장
  - 필요 용량에 대한 예측 불필요. 수요에 맞춘 유연한 확장
  - 실제 트래픽을 정확하게 예측하는 것은 사실상 불가능.   
  #### [4] 속도 및 민첩성
  - 수 분 만에 인프라 구축 가능. 빠르게 변화에 대응
  - 혁신을 위한 시도를 많이 할 수 있고, 실패의 비용이 낮기 때문에 많은 혁신이 가능
    - [각 산업별 이루어지는 혁신] 클라우드 기반의 기업들이 글로벌하게 성공하는 경우↑
  #### [5] 비즈니스에만 집중 가능
  - 혁신을 위한 다양한 실험 가능. 불필요한 인프라 관리 업무 제거
  - 핵심 비즈니스에만 집중하여 경쟁력을 높일 수 있음
  #### [6] 글로벌 확장
  - 전 세계 어디라도 수 분 내 확장하여 글로벌 서비스 구현 가능


### 2. Why AWS?
#### [1] 10년 이상의 축적된 경험
#### [2] 폭 넓고 깊이 있는 서비스 포트폴리오
#### [3] 빠르고 지속적인 혁신 속도 -> 90% 이상의 서비스/기능은 고객 피드백으로부터 시작되어 출시(고객지향)
#### [4] AWS 글로벌 인프라
- 20개 리전(AWS 서비스가 운영되는 지역으로 복수개의 데이터 센터들의 집합)
- 61개 가용 영역(AZ_Availability Zone; 리전 내 위치한 복수 개의 데이터 센터들. low latency지만 각각 물리적으로 분리되어있어 고가용성/이중화 구성 가능화)
- 160+개의 CloudFront   
```💡 CloudFront```
#### [5] Amazon의 가격 철학
더 많은 AWS 이용 → 더 많은 인프라 규모 → 규모의 경제 발생 → 인프라 비용 절감 → 가격 인하 → 더 많은 고객 유치 → 더 많은 AWS 이용... 선순환의 구조
#### [6] 가장 넓고 많은 파트너 생태계 구축
- AWS partner network : 수 만 개의 SI & Consultancy 및 ISV 파트너
- AWS marketplace : 수많은 파트너 제품을 고객이 원클릭으로 설치 가능


### 3. 주요 AWS 서비스 소개

- AWS 서비스 포트폴리오 : 필요한 만큼 원하는 서비스를 사용

#### [1] 컴퓨팅 서비스 소개

- Amazon EC2(Elastic Compute Cloud) ; 가상 서버 서비스

  - **재구성**이 가능한 컴퓨팅 리소스

  - 쉽게 **확장/축소**되는 컴퓨팅 용량

  - **다양한 인스턴스 타입** 제공

    - 인스턴스 구분 : m[인스턴스 패밀리, 용도별로 선택]5[인스턴스 세대, 높을수록 최신, 최신 = 비용 대비 성능이 우수].large[인스턴스 사이즈, 커질 때마다 용량 및 가격이 2배씩 증가]

  - 사용한 만큼만 과금

    - 과금 옵션

      - On-Demand : 약정없이 쓴 만큼만 지불

        ​							갑작스런 트래픽이나 예측하기 어려운 경우, 신규 서비스

      - Reserved : 1년 혹은 3년 약정 40~70% 할인

        ​					항상 사용 중인 안정화된 서버 자원을 위한 요금제

      - Spot : 남은 자원에 대한 경매 방식. 더 높은 가격으로 입찰할 경우 바로 양도될 수 있으나 80~90% 저렴

        ​			단기적으로 수요가 많을 때 유리

- Auto Scaling ; 서버 자동 확장/축소

  - CPU 사용률에 따라 인스턴스 추가/삭제

- AWS Lambda; 서버리스 컴퓨팅

  - 이벤트 처리 기반 - 서버 없이 코드만으로 특정 업무를 처리 (1.업로드 2.트리거 3.실행 4.사용요금)

#### [2] 스토리지 및 컨텐츠 배포 서비스 소개

- Amazon S3(Simple Storage Service) ; 무제한 객체 스토리지

  - 객체 기반의 **무제한** 파일 저장 스토리지

  - **URL**을 통해 손쉽게 파일 공유 가능

  - 99.999999999%의 내구성

  - 사용한 만큼만 지불(GB 당 과금)

  - **정적 웹 사이트 호스팅** 가능

  - 다양한 AWS 서비스들과의 통합/연계 지원

  - 스토리지 옵션

    - AWS S3 - 무제한 스토리지

      - Hot data 를 저장하는 범용 스토리지

      ```
      💡 Hot Data : 즉시 액세스해야하는 데이터
      ```

    - AWS S3 - Infrequent Access Storage

      - 자주 접근하지 않는 데이터를 저렴하게 보관
      - 자주 조회하는 데이터에는 부적합(조회 비용 때문)

    - AWS Glacier - 데이터 백업

      - 백업/아카이빙 용도의 Cold 데이터
      - 사용한만큼 매우 낮은 비용으로 활용 가능

- Amazon EBS ; 블록 스토리지

  - EC2에 attach해서 쓸 수 있는 블록 스토리지(vm에 mount해서 쓰는 하드디스크)
    - 특정 시점에 대한 볼륨 스냅샷을 만들 수 있는 기능 제공 → S3에 저장되어 복수의 가용 영역에 걸쳐 자동으로 복제
    - 한 개의 EBS가 여러 개의 EC2에 attach 불가. 한 개의 EC2에 여러 개의 EBS를 attach 가능

- Amazon CloudFront ; 컨텐츠 전송 네트워크(CDN)

  - **컨텐츠**(이미지, HTML 등)를 **캐싱**하여 성능 가속

  - 전 세계 160개+ 엣지 로케이션 : **글로벌 서비스**

  - AWS 서비스 → CloudFront 간 **데이터 전송 무료**

  - 글로벌 고속 **백본 네트워크** 확보

    ``````
    💡 Backbone Network : 다양한 네트워크를 상호 연결하는 컴퓨터 네트워크의 일부로서, 각기 다른 LAN이나 부분망 간에 정보를 교환하기 위한 경로를 제공
    ``````

  - **Layer 3/4 DDoS 방어** 무료 제공(AWS Shield Standard)

#### [3] 데이터베이스

- Amazon RDS(Relational Database Service) ; 관리형 관계형 DB 서비스

  - 다양한 DB 엔진 제공
  - DB 이중화 (Multi-AZ) : master-slave 간에 자동적으로 싱크가 이루어짐. master에서 문제 발생시 slave로 자동적으로 failover가 진행됨. failover가 진행될 때 수분 내로 옮겨지며 endpoint 변경 필요 없이 자동적으로 처리가 되기 때문에 이중화 구성에 용이함.

  ```
  💡 Multi-AZ
  ```

  ```
  💡 DB Instance : 클라우드에서 실행하는 격리된 데이터베이스 환경
  ```

  ```
  💡 Failover(장애 극복 기능) : 컴퓨터 서버, 시스템, 네트워크 등에서 이상이 생겼을때 예비 시스템으로 자동전환되는 기능. 시스템 대체 작동 또는 장애 조치라고도 한다. <-> Switchover : 사람이 수동으로 전환을 실시하는 것
  ```

  - Read Replica : RDS DB 인스턴스의 성능과 내구성을 높여줌. 단일 DB 인스턴스의 용량 한도 이상으로 탄력적으로 확장하여 읽기 중심의 데이터베이스 워크로드를 처리할 수 있음. 

  - 인스턴스 확장이 자유로움
  - **Amazon Aurora** : MySQL 및 PostgreSQL과 호환되는 완전 관리형 관계형 데이터베이스 엔진. 성능 및 비용효율성을 모두 확보한 DB엔진

  ```
  💡 Database Engine : DBMS이 데이터베이스에 대해 데이터를 CRUD 하는 데 사용하는 기본 소프트웨어 컴포넌트
  ```

  ```
  💡 데이터베이스 운영
  - 비관리형(Non-Managed)
  	- 사용자가 직접 관리
  	- 사용자가 데이터센터를 운영하는 경우
  	- 장비 운영, OS 설치 및 운영, 데이터베이스 솔루션 설치 및 운영까지 모두 담당
  - 관리형(Managed)
  	- 사용자와 AWS가 함께 관리
  	- AWS EC2 서버에 데이터베이스 솔루션을 설치하고 운영하는 경우
  	- 장비 운영, OS 설치 및 운영은 AWS가 담당하고, 데이터베이스 솔루션의 설치 및 운영은 사용자가 담당
  - 완전관리형(Fully-Managed)
  	- AWS가 모두 관리
  	- AWS에서 제공하는 RDS 솔루션을 이용하는 경우
  	- 장비 운영, OS 설치 및 운영, 데이터베이스 솔루션 설치 및 운영까지 AWS에서 모두 담당
  ```

- Amazon DynamoDB ; 관리형 NoSQL DB 서비스

  ```
  💡 SQL vs NoSQL
  - 관계형 데이터베이스
  	- 고정된 행(row)와 열(column)로 구성된 테이블에 데이터를 저장
  	- 각 열을 하나의 속성에 대한 정보를 저장하고, 행에는 각 열의 데이터 형식에 맞는 데이터가 저장됨
  	✅ 테이블 기반으로 데이터 저장. SQL(구조화 쿼리 언어)을 사용해서 데이터를 다룰 수 있음.
  		테이블의 관계가 구조화된 데이터의 모음이기 때문에 구조화된 쿼리 언어를 사용할 수 있는 것!
  - 비관계형 데이터베이스
  	- 관계형 데이터베이스를 뺀 나머지 유형을 총칭
  	- 데이터 모델에 따라 유형이 다양함(문서, 키-값, 와이드 컬럼, 그래프..)
  	- 유연한 스키마 제공 및 대량의 데이터와 높은 사용자 부하에서도 손쉽게 확장 가능
  	- Schema on Read(Hadoop): 데이터를 읽어올 때 스키마에 따라 데이터를 읽어옴 즉, 데이터의 스키마 확인을 데이터를 읽는 시점에 한다는 뜻.
  		<-> Schema on Write(RDBMS) : 데이터를 처음 저장할 때 스키마를 정의하고 데이터를 저장하는 것
  ```

  ```
  💡 Database Schema : 데이터베이스에서 자료의 구조, 자료의 표현 방법, 자료 간의 관계를 형식 언어로 정의한 구조. DBMS이 주어진 설정에 따라 데이터베이스 스키마를 생성하며, 데이터베이스 사용자가 자료를 저장, 조회, 삭제, 변경할 때 DBMS는 자신이 생성한 데이터베이스 스키마를 참조하여 명령을 수행한다.
  ```

  

- Amazon ElastiCache ; 인메모리 캐싱 서비스

#### [4] 기타 AWS 서비스들

​	데이터 분석, 보안, DevOps 등

#### [5] AWS AI

- Amazon Lex
  - 대화형 챗봇 서비스(Alexa와 같은 기술)
  - 음성 및 텍스트 입력 지원
  - 음성 인식 및 자연어 처리 기술 지원

- Amazon Polly
  - Text-to-speech 음성 합성 서비스
  - 일상 언어와 비슷한 음성으로 변환
  - 24개 언어 지원

- Amazon Rekognition
  - 이미지 인식/분석 서비스
  - 객체 및 장면 탐지
  - 안면 분석/비교
  - 유명인 인식 등


### 4. AWS와 보안

**책임 공유 모델**

​	- **클라우드 인프라 위**의 보안은 **고객**이 담당

​	- **클라우드 인프라 자체**의 보안은 **AWS**가 담당
