# GitHub Pages 上線 SOP

這份 SOP 是把 X23 電商營運中台「靜態預覽版」上傳到 GitHub Pages 給妹妹看的流程。

## 目前狀態

- 本機已經初始化 Git repository。
- 已完成兩個 commit：
  - `4a1c130 Add X23 ops GitHub Pages preview`
  - `5bab47d Add preview login and owner approval sidebar`
- 目前尚未設定 GitHub remote。
- 這台電腦目前沒有 `gh` GitHub CLI、GitHub token 或 SSH key，所以不能由 Codex 自動建立新 repo。

## 你需要先做一次

1. 打開 GitHub。
2. 建立一個新的空 repository，例如 `x23-ops-preview`。
3. 不要勾選 README、`.gitignore`、license。
4. 建好後，把 repo URL 貼給 Codex。

建議使用 HTTPS URL，例如：

```bash
https://github.com/YOUR_ACCOUNT/x23-ops-preview.git
```

## Codex 收到 repo URL 後會做

```bash
cd /Users/linyuchen/Desktop/_工作/x23_ops_app
git remote add origin https://github.com/YOUR_ACCOUNT/x23-ops-preview.git
git push -u origin main
```

如果 GitHub 要求登入，請由你本人完成授權，不要把密碼或 token 貼到聊天裡。

## GitHub Pages 設定

推上去後，到 GitHub repo：

1. 進入 `Settings`
2. 點 `Pages`
3. Source 選 `Deploy from a branch`
4. Branch 選 `main`
5. Folder 選 `/root`
6. 儲存

GitHub Pages 會產生一個網址，通常長得像：

```text
https://YOUR_ACCOUNT.github.io/x23-ops-preview/
```

## 上線前安全確認

上傳前確認 Git 只包含這些公開預覽檔：

```bash
git ls-files
```

應該只看到：

```text
.gitignore
.nojekyll
README.md
docs/GITHUB_DEPLOY.md
docs/README_PREVIEW.md
docs/SECURITY_PREVIEW.md
docs/SISTER_HANDOFF.md
index.html
```

不應該包含：

- `app.py`
- `x23_ops.sqlite3`
- `__pycache__`
- 真實 CSV / Excel 報表
- 平台帳密、token、API key

