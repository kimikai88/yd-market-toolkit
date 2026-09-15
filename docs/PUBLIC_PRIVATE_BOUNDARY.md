# 公開與私有內容邊界

## 可以公開

- 通用 EMA／BOLL／RSI／量能計算
- 多週期趨勢面板與非未來函數寫法
- UI、Alert、文件、範例與測試案例
- 不含真實身分資料的示意圖

## 保持私有

- 商業版杯柄辨識、評分、失效緩衝與參數細節
- 邀請制腳本與付費會員授權流程
- 客戶公司資料、統編、聯絡人、設備序號、IP、帳密
- Supabase 金鑰、Google／LINE／Meta 憑證與 webhook secret
- 未公開交易紀錄、資金與持倉資料

## 發布前檢查

```bash
git grep -n -i -E "password|passwd|secret|api[_-]?key|token|private[_-]?key"
```

命中結果必須逐項確認。即使 GitHub 顯示刪除，曾 commit 的秘密仍可能留在歷史中；若誤傳，應立即撤銷並更換憑證。

