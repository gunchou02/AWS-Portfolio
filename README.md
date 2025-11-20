# AWS Serverless Portfolio ☁️

![Build Status](https://github.com/gunchou02/AWS-Portfolio/actions/workflows/deploy.yml/badge.svg)

AWS S3, Lambda, DynamoDB を活用して構築したサーバーレスアーキテクチャのポートフォリオサイトです。
インフラの構築から CI/CD の自動化まで、モダンなクラウド開発フローを実践しました。

## 🛠 Tech Stack (使用技術)

| Category           | Technology              | Description                                           |
| ------------------ | ----------------------- | ----------------------------------------------------- |
| **Frontend**       | HTML5, CSS3             | シンプルな静的ウェブサイト (Simple Static Website)    |
| **Hosting**        | **AWS S3**              | 静的ウェブサイトホスティング (Static Hosting)         |
| **Backend**        | **AWS Lambda** (Python) | サーバーレスコンピューティング (Serverless Computing) |
| **Database**       | **Amazon DynamoDB**     | NoSQL データベース (Visitor Count Storage)            |
| **CI/CD**          | **GitHub Actions**      | 自動デプロイパイプライン (Automated Deployment)       |
| **IaC / Security** | IAM, Bucket Policy      | 権限管理とセキュリティ設定 (Access Control)           |

## 🏗 Architecture (アーキテクチャ)

1. **Frontend**: S3 バケットでホスティングされ、世界中からアクセス可能。
2. **CI/CD**: GitHub への Push をトリガーに、GitHub Actions が S3 へ自動デプロイ。
3. **Backend**: JavaScript (Frontend) -> API Gateway -> Lambda -> DynamoDB (現在構築中 🚧)

## 🚀 CI/CD Pipeline

GitHub Actions (`.github/workflows/deploy.yml`) を使用して以下のプロセスを自動化しています。

1. `main` ブランチへの Push を検知
2. AWS 認証情報の構成 (OIDC/Access Key)
3. S3 バケットへの同期 (Sync)

---

This project is for demonstrating cloud engineering skills.
