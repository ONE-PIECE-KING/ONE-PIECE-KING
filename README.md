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

## **2. 類型導向命名 (Type-based Naming)**
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

## **3. 版本管理 (Versioning)**
對於 API 或 SDK，使用 `v` + 版本號：
```bash
backend-api-v1
frontend-dashboard-v2
```
**重大變更** 應建立新 repo，而非直接修改原 repo。

---

## **4. 開源與內部專案區分**
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

## **5. 縮寫與標準詞彙**
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

## **6. 特殊專案標記**
- **PoC (概念驗證)**：`poc-`
- **測試專案**：`test-`
- **實驗性功能**：`experimental-`
- **模擬環境**：`staging-`
- **存檔專案**：`legacy-`

📌 **範例**：
```bash
poc-ai-recommendation
test-user-api
experimental-voice-cloning
staging-infra
legacy-monolith
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

## **8. 國際化專案 (i18n)**
對於國際化 (i18n) 相關專案，建議：
```bash
i18n-<project>-<language>
```
📌 **範例**：
```bash
i18n-frontend-zh
i18n-chatbot-es
```

---

## **9. GitHub Actions / CI/CD 命名規則**
- `ci-<project>` → CI/CD pipeline
- `cd-<project>` → 部署 pipeline
- `github-action-<function>` → GitHub Action

📌 **範例**：
```bash
ci-backend-auth
cd-infra-deploy
github-action-code-linter
```

---

## **10. 優秀企業 GitHub Repo 參考**
| 公司 | 命名範例 |
|------|---------|
| Facebook | `react`, `jest`, `hermes`, `flow`, `fbt` |
| Google | `tensorflow`, `protobuf`, `google-cloud-sdk` |
| Netflix | `dispatch`, `conductor`, `vectorflow` |
| Amazon | `aws-sdk`, `amazon-freertos`, `aws-cdk` |

---

## **📌 總結**
1. **使用結構化格式**：`<scope>-<project>-<component>-<details>`
2. **類型導向命名** (`frontend-*`, `backend-*`, `infra-*`)
3. **開源 vs 內部專案標記** (`oss-`, `internal-`)
4. **標準縮寫** (`api`, `svc`, `ui`, `ops`)
5. **特殊專案前綴** (`poc-`, `test-`, `legacy-`)
6. **CI/CD & i18n 命名規則** (`ci-*`, `cd-*`, `i18n-*`)
7. **整合 GitHub Teams** (`@frontend`, `@backend`, `@infra`)

