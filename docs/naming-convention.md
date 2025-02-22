# GitHub Organization Repo 命名規範

本文件定義了 GitHub Organization 內的 **Repository 命名規範**，確保專案命名一致性、可讀性和可擴展性，適用於所有成員。

---

## **1. 基本命名規則**
### 📌 **格式**：
```bash
<scope>-<project>-<component>-<details>
```
- **scope**：組織內部領域 (`ai`, `backend`, `frontend`, `devops`, `infra`)
- **project**：專案名稱 (`chatbot`, `analytics`, `mlops`)
- **component**：元件 (`api`, `dashboard`, `service`)
- **details** (可選)：細節 (`test`, `legacy`)

📌 **範例**：
```bash
ai-chatbot-api
ai-chatbot-frontend
devops-infra-terraform
backend-analytics-service
```

---

## **2. 目錄結構規範**
為了確保專案內容清晰，建議使用統一的資料夾結構：
```bash
<repository>/
  ├── docs/            # 文件與規範
  ├── src/             # 原始碼
  ├── tests/           # 測試代碼
  ├── scripts/         # 部署或工具腳本
  ├── config/          # 設定檔案 (如 .yaml, .json, .env)
  ├── data/            # 數據文件（如適用）
  ├── .github/         # GitHub Actions, PR/Issue 模板
  ├── README.md        # 專案說明文件
  ├── LICENSE          # 授權條款
  └── .gitignore       # 忽略文件列表
```

📌 **範例**：
```bash
backend-auth-service/
  ├── docs/
  ├── src/
  ├── tests/
  ├── scripts/
  ├── config/
  ├── README.md
  ├── LICENSE
  └── .gitignore
```

---

## **3. 類型導向命名 (Type-based Naming)**
針對不同類型的專案，使用標準前綴：
- **`frontend-`**：前端相關專案
- **`backend-`**：後端相關專案
- **`infra-`**：基礎設施與 DevOps
- **`data-`**：數據處理與分析
- **`mlops-`**：機器學習與部署
- **`security-`**：安全性相關
- **`docs-`**：內部文件
- **`sandbox-`**：實驗性專案

📌 **範例**：
```bash
frontend-dashboard
backend-auth-service
infra-k8s-setup
data-pipeline
mlops-model-training
security-pentest
docs-api-spec
sandbox-feature-prototype
```

---

## **4. 版本管理 (Versioning)**
對於 API 或 SDK，使用 `v` + 版本號：
```bash
backend-api-v1
frontend-dashboard-v2
```
**重大變更** 應建立新 repo，而非直接修改原 repo。

---

## **5. 開源與內部專案區分**
- **開源專案**：標記為 `public-` 或 `oss-`
- **內部專案**：標記為 `internal-` 或 `private-`

📌 **範例**：
```bash
oss-chatbot-sdk
internal-user-service
private-analytics
public-ui-library
```

---

## **6. 縮寫與標準詞彙**
- 避免模糊名稱，如 `backend-system` 應改為 `backend-user-service`
- 使用通用縮寫：
  - `api` (Application Programming Interface)
  - `ui` (User Interface)
  - `db` (Database)
  - `svc` (Service)
  - `ml` (Machine Learning)
  - `fe` / `be` (Frontend / Backend)
  - `ops` (Operations)
  - `infra` (Infrastructure)

📌 **範例**：
```bash
be-auth-svc
fe-dashboard
ops-ci-cd
ml-nlp-pipeline
db-migration-tool
```

---

## **7. 整合 GitHub Team 權限管理**
為了有效管理 repo，建議使用 `GitHub Teams` 進行權限分配：
- **@frontend**：管理 `frontend-*`
- **@backend**：管理 `backend-*`
- **@infra**：管理 `infra-*`
- **@mlops**：管理 `mlops-*`

📌 **範例**：
```bash
@frontend: frontend-dashboard, frontend-auth-ui
@backend: backend-auth-service, backend-payment
@infra: infra-k8s, infra-monitoring
```

---

## **8. 優秀企業 GitHub Repo 參考**
| 公司 | 命名範例 |
|------|---------|
| Facebook | `react`, `jest`, `hermes`, `flow`, `fbt` |
| Google | `tensorflow`, `protobuf`, `google-cloud-sdk` |
| Netflix | `dispatch`, `conductor`, `vectorflow` |
| Amazon | `aws-sdk`, `amazon-freertos`, `aws-cdk` |


