# aws-saa-Dev-Ops-
나만의 동앗줄

DevOps 포트폴리오 실행 체크리스트
🟢 1단계: AWS 기본 세팅

 AWS 계정 생성 + 무료 티어/크레딧 확보

 IAM 사용자 생성 (Admin 권한 X, 최소 권한 기반 + MFA 켜기)

 AWS CLI 설치 & aws configure (Access Key 세팅)

 Cloud9이나 로컬 환경에서 CLI 테스트 (aws s3 ls)

🟢 2단계: Terraform으로 EKS 클러스터 구축

 Terraform 설치

 VPC 모듈 작성 (Public/Private Subnet, RouteTable 포함)

 EKS 모듈 작성 (Cluster + NodeGroup)

 terraform apply → 클러스터 생성

 aws eks update-kubeconfig → kubeconfig 세팅

 kubectl get nodes로 노드 확인 (첫 번째 스샷 확보)

🟢 3단계: 애플리케이션 배포

 Helm 설치

 Helm 차트 작성 (frontend, backend, db 분리)

 Values 파일로 dev/prod 환경 분리

 Ingress Controller 설치 (AWS ALB Ingress Controller)

 브라우저에서 서비스 접속 → 스크린샷 확보

🟢 4단계: CI/CD 파이프라인

 GitHub Actions 작성 (Docker 빌드 → ECR 푸시)

 ArgoCD 설치 & Git 리포 연동

 코드 커밋 → 자동 배포되는 시연 성공

 배포 로그/ArgoCD 대시보드 스샷 확보

🟢 5단계: 모니터링 & 운영

 Prometheus + Grafana 설치 (Helm 차트 이용)

 Pod 리소스 대시보드 구성

 Loki(혹은 ELK) 설치 → 로그 수집

 CloudWatch 알람 → Slack Webhook 연동

 HPA 실험: kubectl scale or 부하 테스트(k6/locust) → Pod 확장 스샷 확보

🟢 6단계: 보안 & 운영 시나리오

 RBAC 세팅 (dev/ops 역할 분리)

 Sealed Secrets 적용 → 민감정보 암호화 관리

 NetworkPolicy 적용 → Pod 간 통신 제한 테스트

 “Pod 죽여보기” 실험 (재시작/복구 과정 캡처)

🟢 7단계: 문서화 & 포트폴리오 완성

 GitHub 레포: Terraform 코드 + Helm 차트 + Actions Workflow 업로드

 README 작성 (아키텍처 다이어그램, 배포 플로우, 모니터링 결과)

 블로그/노션 정리: “SAA 자격증 공부 → EKS 실습 → DevOps 포트폴리오” 스토리라인 완성

 PDF 포트폴리오 버전까지 만들어서 면접 때 제출 가능하게 준비
