# Observability Lab

## Project Overview

Observability(관측성) 학습을 위한 실습 프로젝트. 한국어로 설명하되 기술 용어는 영문 그대로 사용. Docker Compose 또는 Kubernetes 기반으로 스택을 구성하며, 실전 운영 관점의 설정과 튜닝을 중시한다.

## Tech Stack

- **Metrics**: Prometheus, VictoriaMetrics, Grafana
- **Logs**: Loki, Elasticsearch, Kibana
- **Traces**: Tempo, OpenTelemetry
- **Collector**: OpenTelemetry Collector
- **Application**: Next.js
- **Infrastructure**: Kubernetes, Docker

---

## Curriculum

# Part 1. 관측성(Observability) 기초

## 1장 관측성이란 무엇인가

- 모니터링과 관측성의 차이
- 장애 탐지와 장애 분석
- 현대 시스템의 복잡성
- Telemetry 데이터
- Observability 성숙도 모델

## 2장 SRE와 관측성

- SLI
- SLO
- SLA
- Error Budget
- Golden Signals
- RED Method
- USE Method

## 3장 시계열 데이터 이해

- 시계열 데이터베이스
- Cardinality
- Sampling
- Aggregation
- Retention
- Downsampling
- Compression

---

# Part 2. 메트릭 엔지니어링

## 4장 메트릭 설계

- 좋은 메트릭이란
- 메트릭 네이밍
- Label 설계
- Cardinality 관리
- 안티 패턴

## 5장 메트릭 타입

- Counter
- Gauge
- Histogram
- Native Histogram
- Summary
- Exemplar

## 6장 애플리케이션 계측

- 계측 전략
- 비즈니스 메트릭
- 시스템 메트릭
- 커스텀 메트릭
- 프론트엔드 메트릭

---

# Part 3. Prometheus

## 7장 Prometheus 아키텍처

- Prometheus Server
- Scrape Manager
- Rule Engine
- Sharding
- Remote Write
- Remote Read
- HA 구성

---

# Part 4. PromQL

## 12장 PromQL 기초

- Selector
- Instant Vector
- Range Vector
- Scalar
- String

## 13장 집계 연산

- sum
- avg
- min
- max
- count
- topk

## 14장 벡터 매칭

- one-to-one
- many-to-one
- group_left
- group_right

## 15장 함수

- rate
- irate
- increase
- delta
- predict_linear
- histogram_quantile

## 16장 실전 PromQL

- Error Rate
- Availability
- Throughput
- Latency
- Capacity Planning
- 이상 탐지

## 17장 Recording Rule

- Recording Rule 설계
- Naming Convention
- 성능 최적화

---

# Part 5. Grafana

## 18장 Grafana 구조

- Data Source
- Query Engine
- Dashboard
- Panel

## 19장 Dashboard 설계

- 운영 Dashboard
- 서비스 Dashboard
- 개발 Dashboard
- 경영 Dashboard

## 20장 Variables

- Query Variable
- Custom Variable
- Chained Variable

## 21장 Transformation

- Merge
- Join
- Pivot
- 계산 필드

## 22장 Alerting

- Unified Alerting
- Contact Point
- Notification Policy
- Escalation

---

# Part 6. OpenTelemetry

## 24장 OpenTelemetry 개요

- OpenTracing
- OpenCensus
- OpenTelemetry
- CNCF

## 25장 OTel 데이터 모델

- Resource
- Attribute
- Event
- Link
- Span
- Trace

## 26장 Context Propagation

- W3C Trace Context
- Baggage
- Correlation

## 27장 Semantic Convention

- HTTP
- Database
- Messaging
- Frontend

## 28장 OTLP

- Protocol
- gRPC
- HTTP
- Export Pipeline

---

# Part 7. 프론트엔드 Observability

## 29장 Browser Instrumentation

- Auto Instrumentation
- Manual Instrumentation
- Web SDK

## 30장 사용자 행동 추적

- Click Tracking
- Route Tracking
- API Tracking
- User Journey

## 31장 Web Vitals

- LCP
- CLS
- INP
- FCP
- TTFB

## 32장 Next.js Observability

- SSR
- Server Components
- Route Handlers
- Edge Runtime

---

# Part 8. OpenTelemetry Collector

## 33장 Collector 아키텍처

- Receiver
- Processor
- Exporter
- Connector
- Pipeline

## 34장 Processor

- Batch
- Memory Limiter
- Resource
- Attribute
- Transform

## 35장 배포 패턴

- Agent Pattern
- Gateway Pattern
- Hybrid Pattern

---

# Part 9. VictoriaMetrics

## 37장 VictoriaMetrics 개요

- VictoriaMetrics란?
- Prometheus와의 관계
- 왜 VictoriaMetrics가 등장했는가?
- 사용 사례
- CNCF Observability 생태계에서의 위치

## 38장 Prometheus의 한계

- High Cardinality 문제
- 메모리 사용량 증가
- 장기 보관 문제
- Federation의 한계
- 운영 비용 증가

## 39장 VictoriaMetrics 아키텍처

### Single Node

- 구성 요소
- 데이터 흐름
- 저장 구조

### Cluster Mode

- vminsert
- vmstorage
- vmselect

### 요청 흐름 분석

- Prometheus → vminsert → vmstorage → vmselect → Grafana

## 40장 저장소 내부 구조

- TSDB 구조
- Part
- Block
- Merge
- Delta Encoding
- Compression Strategy
- Label Index
- Search Path
- Cardinality 최적화

## 41장 Prometheus 연동

- Remote Write
- Remote Read
- Queue
- Retry
- Query Path

## 42장 VictoriaMetrics Query Language

- MetricsQL
- PromQL 호환성
- MetricsQL 확장 기능
- rollup
- increase
- rate
- histogram_quantile
- Subquery
- Aggregation

## 44장 성능 튜닝

- Cache
- Query Optimization
- Storage Optimization

## 45장 고가용성(HA)

- Active-Active
- Replication
- Multi AZ
- Failover
- 장애 복구

## 46장 멀티 클러스터 운영

- Global Monitoring
- Regional Monitoring
- Multi Cluster Monitoring
- Cross Cluster Query

## 47장 비용 최적화

- Storage Cost
- Memory Cost
- Query Cost
- Compression Ratio
- Capacity Planning

## 48장 Prometheus vs VictoriaMetrics

- 성능 비교
- 메모리 비교
- Cardinality 비교
- 운영 복잡도 비교
- 비용 비교
- 실무 적용 사례

## 49장 VictoriaMetrics Operator

- Kubernetes 배포
- CRD
- VMCluster
- VMAgent
- VMAlert
- VMAuth

## 50장 실전 운영 사례

- 스타트업 규모
- 중견기업 규모
- 대규모 SaaS
- Kubernetes 환경
- 장애 사례 분석

---

# Part 10. Loki

## 51장 Loki 아키텍처

- Distributor
- Ingester
- Querier
- Query Frontend
- Compactor

## 52장 로그 설계

- Structured Logging
- JSON Logging
- Correlation ID
- Trace ID

## 53장 저장 구조

- Chunk
- Index
- Object Storage

## 55장 LogQL

- Log Query
- Metric Query
- Pipeline

## 56장 로그 파이프라인

- Metrics From Logs
- Pipeline

## 57장 로그 분석

- 에러 분석
- 성능 분석
- 사용자 분석

---

# Part 12. Elasticsearch

## 58장 Elasticsearch 소개

- 검색 엔진 이해
- Index
- Document
- Shard
- Replica

## 59장 데이터 모델링

- Mapping
- Analyzer
- Tokenizer
- Inverted Index

## 60장 검색과 집계

- Query DSL
- Full Text Search
- Aggregation
- Filtering

## 61장 운영 전략

- Cluster 구성
- Scaling
- Storage 관리
- 성능 최적화

## 62장 Loki vs Elasticsearch

- 저장 방식 비교
- 검색 성능 비교
- 운영 비용 비교

---

# Part 13. Kibana

## 63장 Kibana 소개

- Elastic Stack 이해
- Kibana 역할

## 64장 데이터 탐색

- Discover
- Search
- Filter

## 65장 시각화

- Dashboard
- Lens
- Visualization

## 66장 운영 활용

- 로그 분석
- 알림 구성
- 운영 Dashboard

## 67장 Grafana vs Kibana

- 사용 목적 비교
- 강점과 약점
- 실무 적용 사례

---

# Part 14. Tempo

## 68장 분산 추적

- Distributed Tracing

---

# Part 15. Correlation

## 72장 Correlation 설계

- Metrics ↔ Logs
- Logs ↔ Traces
- Metrics ↔ Traces

## 73장 Exemplar

- Histogram Exemplar
- Trace 연결

## 74장 Root Cause Analysis

- 장애 분석 절차
- Incident Investigation
- 실전 사례

---

# Part 16. Kubernetes Observability

## 75장 Kubernetes 모니터링

- Node Monitoring
- Pod Monitoring
- Container Monitoring

## 76장 kube-state-metrics

- Cluster 상태 수집
- Workload 상태 수집

## 77장 Prometheus Operator

- ServiceMonitor
- PodMonitor
- AlertManager

---

# Part 17. 운영과 아키텍처

## 78장 알림 엔지니어링

- Alert Fatigue
- Alert Routing
- Runbook

## 79장 장애 대응

- Detection
- Response
- Recovery
- Postmortem

## 80장 운영 아키텍처

- 스타트업 규모
- 중견기업 규모
- 대기업 규모
- Multi Region
- High Availability
- Meta Monitoring
- Blackbox Monitoring
- Dead Man's Switch

---

# Part 18. 최종 프로젝트

## 81장 Next.js 서비스 구축

## 82장 OpenTelemetry 계측

## 83장 Collector 배포 및 모니터링
