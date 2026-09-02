# Project Setup

## 1. Create the GitHub Repository

Create a GitHub repository for the project.The repository must contain:
* `README.md` — Keep this exact filename.
* `CONTRIBUTING.md` — Keep this exact filename.
* `docs/` — Create a folder for project documentation.

Inside `docs/`, add Markdown files for:
```text
TechStack.md (Optional)
Architecture.md (Optional)
Logs.md (Optional)
FolderStructure.md (Optional)
//Add other documentation files when necessary.
```
---

## 2. Initialize Git Branches

Initialize the remote repository. Rename the default `master` branch to `main`, Create a dev branch.
The repository should have:
```text
main
dev
```
---

## 3. Create the Discord Webhook

Create a Discord channel using the **project-name**. then Go to:

```text
Channel Settings → Integrations → Webhooks → New Webhook
```
Copy the webhook URL. Rename the webhook as : `Repository`. then Add an appropriate image as the webhook avatar.
Sample image: `./WebhookPicture.jpg`

---

## 4. Add the GitHub Secret

Go to then GitHub repository on github.com:
```text
Settings → Secrets and variables → Actions → New repository secret
```
Create the following secret:
```text
Name:
DISCORD_WEBHOOK_URL
Value:
<Copied Discord webhook URL>
```
---

## 5. Add the Discord Notification Workflow

Create the following folder if it does not already exist:
```text
.github/workflows/
```
Copy `./discord-notify.yml` into:
```text
.github/workflows/discord-notify.yml
```

Commit and push the workflow to the `main` branch.

The final repository structure should look similar to:

```text
project/
├── .github/
│   └── workflows/
│       └── discord-notify.yml
├── docs/
│   ├── TechStack.md
│   ├── Architecture.md
│   ├── Logs.md
│   └── FolderStructure.md
├── README.md
└── CONTRIBUTING.md
```
Create a test commit and push it to verify that the Discord webhook is working correctly. 🚀