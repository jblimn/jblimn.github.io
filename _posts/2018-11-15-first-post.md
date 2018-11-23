# MSA
![image](https://user-images.githubusercontent.com/21349804/48928579-dfa7a580-ef23-11e8-8960-0adb9d111869.png)

Area / Level	Inception	Established	Optimizing
서비스 게이트웨이 (Service Gateway)	정적 라우팅	동적 라우팅	동적 라우팅
	                        서비스 등록/감지 수동	서비스 등록/감지 자동	서비스 등록/감지 자동
			                                                               Circuit Breaker
서비스(Service)	API Centric(Restful API)	API Centric(Restful API)	API Centric(Restful API)
		                                      서비스분할(전체범위)	서비스분할(전체범위)
		                                    서비스간 연계방식 (RESTful API/RPC/MQ)	서비스간 연계방식 (RESTful API/RPC/MQ)
                                                                    API 관리 세부계획 보유
                                                                    서비스별 권한 확인
데이터 (Data)	서비스별 데이터 공유/분리 혼재(Strangler pattern)	서비스별 데이터 분리	서비스별 데이터 분리
                             Polyglot(RDB/NoSQL)	Polyglot(RDB/NoSQL)	Polyglot(RDB/NoSQL)
	                          논리스키마 분리구성	논리스키마 분리구성	읽기/쓰기 전용 저장소(CQRS)
                                                물리스키마 일부분리	논리스키마 분리구성
			                                                               물리스키마 분리구성
통합/배포 (CI/CD)  	CI 파이프라인 자동화	CI/CD 파이프라인 자동화	CI/CD 파이프라인 자동화
	                  배포유형(Artifact) : class, jar/war	배포유형(Artifact) : jar/war(미들웨어 내장)	Automatic Continuous Deployment
	                  배포주기 : 계획기반(Scheduled)	배포주기 : 즉시(On-Demand)	배포유형(Artifact) : 도커 이미지
			                                                              배포주기 : 즉시(On-Demand)
			                                                              Feature Toggle
모니터링 (Monitoring)	서비스 개별 모니터링	서비스 통합 모니터링(대시보드)	서비스 통합 모니터링(대시보드)
                                        통합 로깅(로그수집/통합저장/시각화)	통합 로깅(로그수집/통합저장/시각화)
                                        DevOps Dashboard	              로그 분석/예측
                                                                        E2E 모니터링(서비스간 추적성)
                                                                        Self-Healing
인프라(Infra)	자원할당 소요시간 : 수일 이내	자원할당 소요시간 : 수시간 이내	자원할당 소요시간 : 즉시(On-Demand)
                HW/OS단위 자원할당	OS단위 자원할당	Container단위 자원할당
                                                자동 확장(Auto-Scaling)
