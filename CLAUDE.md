# firstaid-course

**`kansasray/gym-course`(自有框架 fork)的 clone,放一門課:`courses/firstaid/`「防災急救」。** 框架負責建置稽核驗證部署;課程內容全在 `courses/firstaid/`;`courses/gym/` 是上游對照範例不要動。

課程:繁中防災急救,3 部 9 章(基礎生命支持/創傷處置/災害與野外)、29 單元 71 支影片、8 小時 46 分。PART I-II 中文主軸(衛福部/消防署官方 + EMT 頻道「安妮怎麼了」骨幹),PART III 野外章英文權威(NOLS/MedWild)補位。**不建 citations 檔、不宣告 grades**(立場頁 evidence_grade 直接放中文標籤,同 atak-course 解法)。

## 指令
```bash
COURSE=courses/firstaid make build audit verify   # 一律帶 COURSE=
COURSE=courses/firstaid COOKIES_BROWSER= uv run python src/build/fetch_meta.py
```

## 這門課的特殊紀律(改動前必讀)

1. **AHA/ILCOR 2025-10 指引大改版是全課的時效軸**。每支影片的 why 都標了上傳日期與指引版本判斷;成人哽塞流程已改為「拍背 5 下+腹部擠壓 5 下交替」,CH2 的 58 萬觀看經典舊片(2013)與新指引衝突,導讀有明確對照。未來更新影片時,先查當時最新指引年份。
2. **真實傷患/災民新聞畫面一律不收**(倫理紅線),教學示範與演習紀錄才收。策展時排除了大量新聞片。
3. **台灣求援號碼:山域是 119/112,118 是海巡署海上專線** —— CH8 策展時查證確認(消防署官網),派工簡報曾寫錯,勿再犯。
4. 業配/自售內容有收但 why 標明身分(安妮商店、黑熊商城、PrepMedic 折扣)。
5. 兩支 <300 觀看影片為刻意收錄(audit 唯一警告):267 觀看那支是全網唯一示範 2025 新版哽塞流程的中文影片;168 觀看的燒傷分級有 note。
6. **兩支影片待人工過目**(agent 依 metadata 判斷,未逐格看畫面):`3Km4wk6RH98`(02:37-05:31 八仙塵爆訪談段,已標可略過)、`l4eyqRBOSI8`(2018 花蓮地震兩天後的技巧講解新聞)。

## 框架陷阱
同 atak-course/pilot-course 的清單(8899 撞港、facetLabel/tabs.stance 必填、立場區塊無條件渲染、unitTypes 避開 field/demo、fetch_meta 用 COOKIES_BROWSER=、deploy 前先 create Pages 專案)。本 repo 無新增陷阱。

## 狀態(2026-08-10 完成)
- **verify 71/71、audit 0 錯誤 1 警告、89 tests 全過**;71 支零跨章重複;最大頻道佔比 14.1%(安妮怎麼了)
- (部署後補:上線網址與 GitHub repo)
