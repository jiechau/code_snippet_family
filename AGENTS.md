# 專案工作規則

## 修改後自動 commit 與 push

使用者已授權：在此專案中，只要任務新增、修改或刪除檔案，完成該次工作與適當檢查後，直接 commit 並 push，不需要再次詢問確認。使用者當次明確要求不要提交或推送時，遵循當次指示。

有檔案變更的任務，請讀取並遵循 [.agents/skills/auto-commit-push/SKILL.md](.agents/skills/auto-commit-push/SKILL.md)。只提交本次任務的相關變更，遵循目前分支及既有遠端設定；不使用 force push 或重寫歷史。若提交或推送失敗，保留現況並回報原因。

## 修改與推送前自動 git pull

每次需要新增、修改或刪除程式碼或其他版本控制檔案時，請先讀取並遵循 [.agents/skills/auto-pull/SKILL.md](.agents/skills/auto-pull/SKILL.md)，在第一次編輯前自動 git pull。每次 git push 前也必須再次 git pull；同步失敗或發生衝突時，保留現況並回報，不繼續編輯或推送。

## 遊戲檔案安排

新遊戲若能以單一 HTML 完整實作，沿用單一 HTML 的方式；若需要多個檔案，請為該遊戲建立專屬資料夾，將所需檔案集中放入其中。
