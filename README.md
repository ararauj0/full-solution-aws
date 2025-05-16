# 🔹 Requisitos

- 🌐 Aplicação Web
- 🛡️ Login e controle de acesso
- 📁 Upload de arquivos (fotos e PDFs)
- 📢 Notificações
- 🧠 Backend público e para terceiros
- 🧑‍🤝‍🧑 1000 usuários simultâneos (alta concorrência)
- 🧾 Banco de dados relacional (PostgreSQL)
- 🏗️ Arquitetura 100% AWS (Descrição Detalhada)

## 🔹 Frontend
- Amazon S3: Hospedagem do frontend (HTML/CSS/JS, React/Vue/etc.)
- Amazon CloudFront: CDN com cache e HTTPS
- Amazon Route 53: Gerenciamento de domínio e DNS
  
## 🔹 Autenticação e Autorização
- Amazon Cognito (User Pools): Login de usuários e controle de sessão
- Amazon Cognito (Identity Pools): Para gerar credenciais temporárias e acessar AWS (ex: S3)
- IAM Roles com políticas: Regras de acesso refinadas
  
## 🔹 Backend (API REST para app + terceiros)
- Amazon API Gateway: Gateway seguro e escalável com throttling
- AWS Lambda: Funções serverless para lógica de negócio
- Alternativa: AWS ECS Fargate (se preferir containers)
- Amazon RDS (Aurora PostgreSQL): Banco de dados relacional e escalável
  
## 🔹 Upload de Arquivos
- Amazon S3: Armazenamento de fotos e PDFs
- Upload com presigned URLs para segurança
- Integração com Lambda para redimensionamento, antivírus ou outras validações
  
## 🔹 Notificações
- Amazon SNS: Envio de notificações push, e-mails ou integração com sistemas externos
  
## 🔹 Monitoramento e Observabilidade
- Amazon CloudWatch: Logs, métricas e alarmes
- AWS X-Ray: Rastreamento entre Lambda/API Gateway/RDS
- AWS CloudTrail: Auditoria de ações em toda a conta
  
## 🔹 Segurança
- WAF + API Gateway: Proteção contra bots e ataques
- AWS Shield (Standard): Proteção contra DDoS
- AWS KMS: Criptografia de dados em repouso (RDS/S3)
- Secrets Manager: Armazenamento seguro de senhas e tokens
