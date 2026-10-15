[Notion Portfolio](https://www.google.com/search?q=https%3A%2F%2Fdiscovered-echinodon-22b.notion.site%2F7f606eb186c183f0bf3c01738996c796)
[GitHub](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fqorgh529)


## 👋 About Me

> **"클라우드를 안정적으로 운영하고, 반복되는 장애와 위협을 자동화로 해결하는 엔지니어 김성현입니다."**

* **멀티클라우드 운영 및 무장애 이관**: 실무에서 **MS Azure · AWS · NCP** 환경을 동시에 운영하며, 5개 라이브 게임 서비스(VM 약 150대 규모)의 **AWS·NCP → Azure 무장애 마이그레이션**을 완수했습니다.

* **클라우드 보안 및 대응 자동화**: 방화벽·NSG·VPN 등 네트워크 접근 제어를 직접 관리하고, L7(Application Gateway) 앞단의 비정상 대량 접속을 **1분 주기 스크립트로 탐지·자동 차단**하여 야간·주말 보안 공백을 해소했습니다.

* **컨테이너 & 멀티클라우드 아키텍처 확장**: **베스핀글로벌 멀티클라우드(AWS·Azure·GCP·NCP) 부트캠프**와 개인 **홈랩 Kubernetes(GitOps)** 구축을 통해 클라우드 네이티브 인프라와 재해 복구(DR) 설계까지 역량을 넓히고 있습니다.

## 🏆 Key Achievements

| 핵심 영역 | 주요 성과 및 지표 | 적용 환경 / 기술 | 
| ----- | ----- | ----- | 
| **무장애 클라우드 이관** | 라이브 게임 서비스 5개(VM 약 150대) **AWS·NCP → Azure 무장애 전환** (담당 2개 서비스·VM 약 60대 직접 수행) | MS Azure, AWS, NCP | 
| **인프라 비용 최적화** | 라이선스 및 워크로드 분석 기반 **Azure Dedicated Host(ADH) 도입으로 월 25% 비용 절감** | Azure Dedicated Host, VM | 
| **보안 위협 자동 차단** | IP당 1분 500회 이상 비정상 요청 탐지 시 **NSG Deny 정책 자동 등록 및 메일 알림** 자동화 | Application Gateway, Azure CLI, NSG | 
| **고가용성 & 관측성 구축** | 멀티존 MIG 오토스케일링(2→4대 확장 검증) 및 **감사 로그 기반 DB `DELETE` 실시간 Slack 알림** 구현 | GCP Compute Engine, Cloud Monitoring | 
| **온프레미스 & GitOps** | 사내 가상화 서버 **23대 운영** 및 홈랩 **K8s + Gitea + ArgoCD 자동 배포 파이프라인** 구축 | VMware, Proxmox, Kubernetes, ArgoCD | 

## 🛠️ Tech Stack

### Cloud & Virtualization

### Container & GitOps

### Network, Security & Monitoring

### OS, Middleware & Automation

<details>
<summary><b>📊 기술별 실무 숙련도 및 활용 근거 펼쳐보기 (Click)</b></summary>
<br>

| 기술 분야 | 숙련도 | 경험 기간 | 핵심 실무 및 프로젝트 적용 내역 | 
| ----- | ----- | ----- | ----- | 
| **MS Azure** | **상** | 33개월 | VM·NSG·Application Gateway·Monitor 운영, AWS·NCP→Azure 이관, ADH 도입 비용 25% 절감, Azure 보안 점검 | 
| **네트워크 접근 보안** | **상** | 33개월 | NSG·방화벽 정책·접근 제어 관리, 오픈소스 VPN 경유 구성, L7 비정상 접속 자동 차단, 패킷·침해사고 분석 | 
| **AWS · NCP** | **중** | 33개월 | 라이브 게임 서버 인프라 운영 및 Azure 환경으로의 단계적 무장애 마이그레이션 수행 | 
| **VMware · Proxmox** | **중** | 29개월 | 사내 가상화 서버 23대 운영 관리, Proxmox 기반 사내 개발·테스트 환경 구축 | 
| **GCP · Kubernetes** | **중** | 집중 과정 | GCP 3-Tier 고가용성 인프라 구축, 멀티클라우드 DR 설계, 홈랩 K8s + ArgoCD GitOps 파이프라인 운영 | 

</details>

## 🚀 Featured Projects

### 1. 멀티클라우드 사이버 복구(DR) 프로젝트 (`nova-final`)

* **Repository**: [github.com/qorgh529/nova-final](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fqorgh529%2Fnova-final) · [bespin-nova-final-team3/was](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fbespin-nova-final-team3%2Fwas)

* **개요**: CI/CD 공급망 공격으로 주 클라우드(GCP) 조직 권한이 탈취된 재난 상황을 가정하여, 신원 체계가 완전히 분리된 **AWS 불변 백업 및 클린 빌드 환경으로 핵심 서비스를 복구**하는 멀티클라우드 DR 프로젝트

* **담당 역할**: GCP 3-Tier 인프라 WAS 구성(Tomcat MIG, 골든 이미지, Auto Scaling·헬스 체크) 및 아키텍처 설계·핸드오프 문서화

<details>
<summary><b>🔍 아키텍처 및 핵심 구현 상세 보기 (Click)</b></summary>

* **AWS 3계정 격리 아키텍처**: `백업 계정(상시)` · `DNS 계정(상시)` · `DR 계정(평시 비용 0원)`으로 권한 및 네트워크 격리

* **불변 백업 및 데이터 무결성**: AWS Lambda가 WIF(Workload Identity Federation) 단방향 읽기 권한으로 GCP 데이터를 Pull하고, SHA-256 해시 검증 후 S3 Object Lock(Compliance 모드)으로 위변조 원천 차단

* **클린 빌드 & 수동 DNS 전환**: 오염 시점을 특정할 수 없는 컨테이너 이미지 대신 AWS CodeBuild에서 클린 소스로 재빌드하고, 공격 표면 노출 방지를 위해 Route 53(TTL 60초) 수동 Failover 및 자체 JWT 인증 적용

</details>

### 2. GCP 3-Tier 구축 프로젝트 NOVA (PROFIT 동물병원 Lift & Shift)

* **Repository**: [github.com/bespin-nova/WAS](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fbespin-nova%2FWAS) · [github.com/bespin-nova/WEB](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fbespin-nova%2FWEB)

* **기간 및 규모**: `2026.09 ~ 2026.10` · 4인 팀 프로젝트 (**본인 역할: WAS 및 모니터링 담당**)

* **아키텍처 흐름**: `사용자 → Cloud Armor · External HTTPS LB · Cloud CDN → WEB MIG(Apache) → Internal NLB(8080) → WAS MIG(Tomcat) → PSC → Cloud SQL HA` (SSH는 IAP 전용, 방화벽 태그+CIDR 최소 권한 허용)

<details>
<summary><b>🔍 핵심 구현 및 트러블슈팅 상세 보기 (Click)</b></summary>

* **고가용성 WAS 구성**: Tomcat 골든 이미지 제작 및 멀티존(Zone A·C) MIG 구성, 오토스케일링(2\~6대) 및 오토힐링 적용 → **부하 테스트 시 2대에서 4대로 자동 확장 검증**

* **관측성 및 Slack 실시간 알림 4종**: WAS 5xx 에러 급증, WAS 애플리케이션 오류, Cloud SQL Failover, **감사 로그 기반 DB `DELETE` 쿼리 실행 감지 시 실행 계정·쿼리·복구 절차를 Slack으로 즉시 전송**

* **트러블슈팅**: 배포 후 모바일 환경에서 메뉴가 동작하지 않는 원인이 Bootstrap 3와 jQuery 3.5.1 간 버전 비호환임을 규명하고, jQuery 1.9.1로 변경하여 정상화

</details>

### 3. 홈랩 Kubernetes & ArgoCD GitOps 파이프라인 (`homelab-k8s`)

* **Repository**: [github.com/qorgh529/homelab-k8s](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fqorgh529%2Fhomelab-k8s)

* **기간 및 규모**: `2026.04 ~ 진행 중` · 1인 개인 구축 프로젝트

* **아키텍처 흐름**: `사용자 → 라우터(80/443 포트포워딩) → Nginx Ingress Controller (cert-manager Let's Encrypt TLS) → hub / web-portal(FastAPI · PostgreSQL PVC · Redis) / gitea / argocd`

<details>
<summary><b>🔍 핵심 구현 및 주요 트러블슈팅(14건 중 대표 사례) 보기 (Click)</b></summary>

* **End-to-End GitOps**: 자체 호스팅 Gitea 저장소 및 레지스트리와 ArgoCD를 연동하여 `git push` 시 자동 동기화·배포 파이프라인 완성

* **보안 및 이상 감지 알림**: 로그인 API 분당 5회 Rate Limit 적용으로 브루트포스 방어, APScheduler 기반 Pod 상태(1분 주기)·인증서 만료(24시간 주기) 감시 및 Discord/Gmail 알림 연동

* **주요 트러블슈팅**:

  1. **헤어핀 NAT 환경에서 cert-manager 인증서 발급 실패**: 내부 클러스터에서 외부 도메인 접근 시 루프백 실패 원인을 분석하여 **CoreDNS에 내부 도메인을 등록**해 HTTP-01 챌린지 해결

  2. **Gitea 컨테이너 레지스트리 Push 시 HTTP 413 오류**: Nginx Ingress 기본 요청 크기 제한을 확인하고 `proxy-body-size: "0"` 어노테이션을 적용해 대용량 이미지 Push 해결

  3. **PostgreSQL Pod 재시작 시 데이터 유실**: 컨테이너 임시 볼륨 문제를 `PersistentVolumeClaim(PVC)` 마운트로 전환하여 영속성 확보

</details>

### 4. Kubernetes Pod 생성 내부 동작 시각화 (`kube`)

* **Repository**: [github.com/qorgh529/kube](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fqorgh529%2Fkube)

* **개요**: `kubectl`로 Pod 6개를 배포할 때 클러스터 내부 컴포넌트(`kube-apiserver`, `etcd`, `Deployment/ReplicaSet Controller`, `kube-scheduler`, `kubelet`, `CRI/CNI/CSI`, `cloud-controller-manager`)가 상호작용하는 **11단계 메커니즘을 Draw.io 다이어그램과 인터랙티브 HTML로 시각화**한 학습 레포지토리

## 💼 Work Experience & Education

### Work Experience

| 기간 | 회사명 | 직무 / 역할 | 주요 수행 업무 및 성과 | 
| ----- | ----- | ----- | ----- | 
| `2025.12 ~ 2026.03` | **(주)유성씨앤아이** | 네트워크 엔지니어 (경력) | 공공 클라우드(정부24 통합창구) 네트워크 아키텍처 수립·프로비저닝·모니터링, MSP 및 대외기관 협업 장애 대응 | 
| `2025.02 ~ 2025.05` | **오엠티아이코리아(주)** | 인프라·보안 (인턴) | 사내 인프라 및 Azure 클라우드 보안 점검, MSSQL 로그인 실패 로그 모니터링을 통한 비정상 접근 탐지 | 
| `2022.02 ~ 2024.06` | **(주)무브인터렉티브** | 시스템·클라우드 엔지니어 (경력) | 5개 라이브 게임 서버 AWS·NCP → Azure 무장애 이관, ADH 도입 월 25% 비용 절감, L7 비정상 접속 자동 차단, 사내 가상화 서버(23대) 및 헬프데스크 운영 | 

### Education & Training

| 기간 | 교육기관 / 학교 | 과정명 / 전공 | 주요 내용 | 
| ----- | ----- | ----- | ----- | 
| `2026.06 ~ 2026.12` | **베스핀글로벌** | AI MSP 멀티클라우드(AWS·Azure·GCP·NCP) 엔지니어 부트캠프 5회차 (1,000시간) | 멀티클라우드 구축·운영, GCP 3-Tier 팀 프로젝트 및 멀티클라우드 사이버 복구(DR) 프로젝트 수행 | 
| `2020.03 ~ 2020.09` | **코리아AI아카데미** | 정보시스템 보안 운영 및 보안사고분석 과정C (868시간) | Linux/Windows 서버 운영, 네트워크(VLAN·라우팅·Wireshark 패킷 분석), 모의해킹·취약점 및 침해사고 분석, Firewall·VPN 운영 | 
| `2016.03 ~ 2020.02` | **인하공업전문대학** | 금속재료과 (전문학사 졸업) | 공학 기초 및 데이터 분석 기반 문제 해결 역량 함양 | 

## 💡 How I Work (Learn · Do · Share)

* **반복되는 수작업은 스크립트로 자동화합니다**: 야간·주말마다 수동으로 IP를 차단하던 비효율을 없애기 위해, 임계치(1분 500회) 기준 정의부터 Azure CLI 스크립트 기반 NSG 자동 차단·알림까지 파이프라인으로 만들었습니다.

* **장애와 해결 과정을 누구나 재현할 수 있게 기록합니다**: 홈랩 Kubernetes 구축 과정에서 겪은 14건의 트러블슈팅과 사내 인프라 가이드를 `증상 → 원인 → 해결` 순서로 문서화하여 팀과 커뮤니티가 같은 문제를 빠르게 해결할 수 있도록 공유합니다.

* **알림에는 반드시 '확인 순서와 복구 절차'를 담습니다**: 단순 경고에 그치지 않고, DB `DELETE` 감지 알림처럼 실행 계정·쿼리·복구 절차를 함께 전달해 담당자가 즉시 조치할 수 있는 관측성을 지향합니다.

* **기술 일정만큼 서비스와 현업의 일정을 존중합니다**: 150대 규모의 라이브 게임 서버를 이관할 때 각 게임 PD 및 유관 부서와 점검 일정을 조율하며 1년 1개월간 무장애 병행 운영 및 전환을 이끌었습니다.

## 📊 GitHub Stats

## 📫 Contact

* **Email**: [qorgh529@gmail.com](mailto:qorgh529@gmail.com) / [qorgh529@kakao.com](mailto:qorgh529@kakao.com)

* **Portfolio**: [Notion 포트폴리오 바로가기](https://www.google.com/search?q=https%3A%2F%2Fdiscovered-echinodon-22b.notion.site%2F7f606eb186c183f0bf3c01738996c796)

* **GitHub**: [github.com/qorgh529](https://www.google.com/search?q=https%3A%2F%2Fgithub.com%2Fqorgh529)
