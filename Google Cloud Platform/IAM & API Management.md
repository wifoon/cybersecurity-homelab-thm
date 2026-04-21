
Quick reference note on navigating the Google Cloud Console, managing Identity and Access Management (IAM), and handling Cloud APIs. Based on the Google Cloud Computing Foundations series.

---

### Project Identification
In Google Cloud, every resource must belong to a **Project**. Projects are isolated from each other and identified by:

* **Project Name**: A user-friendly name (can be changed).
* **Project ID**: A globally unique identifier (cannot be changed).
* **Project Number**: An automatically assigned unique number.

In a lab environment, we often see a **Qwiklabs Resources** project, which is a shared, read-only repository for datasets and machine images.

---

### Cloud IAM (Identity & Access Management)
IAM defines **Who** (Principal) has **What** (Role) on **Which** resource. Roles are collections of permissions.

**Basic Roles (Primitive):**

| Role Name | Permission Level | Description |
| :--- | :--- | :--- |
| `roles/viewer` | Read-only | View resources without modifying state. |
| `roles/editor` | Read + Write | All viewer permissions plus the ability to modify/delete resources. |
| `roles/owner` | Full Access | All editor permissions plus managing roles, permissions, and billing. |

To grant access via Console:
`Navigation Menu` -> `IAM & Admin` -> `IAM` -> `Grant Access`.

---

### APIs & Services
Most Google Cloud features are exposed via **APIs**. By default, many APIs are disabled to minimize security risks and costs.

**Example: Enabling Dialogflow API**
The Dialogflow API allows building conversational interfaces (chatbots) using machine learning.

1.  Go to `APIs & Services` -> `Library`.
2.  Search for **"Dialogflow API"**.
3.  Click **Enable**.

To verify or enable via **Cloud Shell (gcloud CLI)**:
```bash
# List enabled services
gcloud services list --enabled

# Enable a specific service
gcloud services enable dialogflow.googleapis.com