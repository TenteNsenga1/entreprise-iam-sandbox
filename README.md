markdown# 🔒 Enterprise Identity \& Access Management (IAM) Sandbox



\*\*Project Overview:\*\* A local, containerized Identity Provider (IdP) sandbox simulating enterprise identity governance, user lifecycle management, and security compliance. Engineered as an open-source equivalent to practice \*\*Microsoft Entra ID (Azure AD)\*\* and \*\*M365 administration\*\* workflows.



\---



\### 🛠️ Core Infrastructure Stack

\* \*\*Identity \& Access Management:\*\* Keycloak (v26.0)

\* \*\*Containerization \& Runtime:\*\* Docker Engine (WSL 2 on Windows 11)

\* \*\*Automation \& Scripting:\*\* PowerShell



\---



\### 💼 Technical Skill Mapping (M365 / Entra ID Equivalent)



| Implemented Keycloak Feature | Microsoft 365 / Entra ID Equivalent | Business \& Security Value |

| :--- | :--- | :--- |

| \*\*Custom Corporate Realm\*\* | Dedicated Entra ID Tenant | Complete data and directory isolation. |

| \*\*Role Hierarchy (`Helpdesk-Tech`)\*\* | Entra ID Security Groups \& RBAC | Enforces the Principle of Least Privilege. |

| \*\*`realm-management` Client Mapping\*\* | Granular Administrative Delegation | Prevents dangerous global root/superuser access. |

| \*\*Mandatory User Login Action\*\* | Self-Service Password Reset (SSPR) | Forces onboarding password lifecycle updates. |



\---



\### 📂 Key Lab Accomplishments



\* \*\*User Lifecycle Control:\*\* Provisioned and managed secure employee profiles (`james.smith`) matching enterprise helpdesk provisioning cycles.



!\[User Registry Panel](user-registry.png)



\* \*\*Access Control Realization:\*\* Designed granular client roles (`manage-users`, `view-users`) to guarantee strict data segregation, aligning directly with \*\*Health Canada \& FDA compliance criteria\*\* for clinical systems.

&#x20; 

!\[Role Hierarchy Dashboard](role-hierarchy.png)

!\[Administrative Role Mapping UI](role-mapping.png)



\* \*\*Defensive Identity Policies:\*\* Configured temporary credential enforcement to block credential sniffing and ensure account ownership handover security.



\---



\## 🚀 How to Run the Environment

To instantly pull and deploy this isolated development sandbox, execute the following command in PowerShell:



```powershell

docker run -d --name keycloak-sandbox -p 8080:8080 -e KEYCLOAK\_ADMIN=admin -e KEYCLOAK\_ADMIN\_PASSWORD=admin quay.io/keycloak/keycloak:26.0 start-dev

```

