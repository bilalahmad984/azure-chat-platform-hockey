# Required GitHub Secrets

Environments use the suffixes `DEV`, `STG` and `PROD`. Example for production:

## Frontend repository (Vue.js)

| Secret | Purpose |
|---|---|
| `VITE_STREAM_API_KEY_HOCKEY_PROD` | Chat streaming API key baked into the build |
| `VITE_BE_BASE_URL_HOCKEY_PROD` | Backend API base URL |
| `VITE_MODE_HOCKEY_PROD` | Build mode |
| `VITE_AUTH_TOKEN_HOCKEY_PROD` | Frontend auth token |
| `VITE_ENABLED_FEATURES_HOCKEY_PROD` | Feature flags for this environment |
| `VITE_TENANT_HOCKEY_PROD` | Tenant identifier |

## Backend repository (.NET) and server access

| Secret | Purpose |
|---|---|
| `ACR_LOGIN_SERVER_PROD` | Azure Container Registry login server (e.g. `myregistry.azurecr.io`) |
| `ACR_USERNAME_PROD` | ACR username |
| `ACR_PASSWORD_PROD` | ACR password |
| `SSH_PRIVATE_KEY_HOCKEY_PROD` | Private SSH key for the deploy user |
| `SERVER_HOST_HOCKEY_PROD` / `SERVER_IP_HOCKEY_PROD` | Public IP or hostname of the Ubuntu VM |
| `SERVER_USER_HOCKEY_PROD` | SSH user on the VM (e.g. `azureuser`) |

> The SSH secrets (`SSH_PRIVATE_KEY_*`, `SERVER_HOST_*` / `SERVER_IP_*`, `SERVER_USER_*`) are needed in **both** repositories, because both pipelines deploy to the same VM.
