# Translation Status — Canonical Project Tracker

**Policy (canonical, applies for the length of the project):**

1. **This file is the single source of truth** for what is translated and what is not. Before any session, the worker MUST read it; after any session, the worker MUST update it in the same commit as the translations. Never begin work on any row not marked `⬜` without first checking its status here.
2. **Output location:** each book's translations live in `<book-dir>/en/`. One `.en.md` per source file, same basename.
3. **Output format (from 2026-11-23 onward):** per section — `**ZH:**` (original Chinese, verbatim), `**PY:**` (pinyin with tone marks), `**EN:**` (English translation). The Zhuangzi chapters completed before this policy retain ZH/EN only; pinyin backfill is tracked below as its own task.
4. **Fidelity:** every `**ZH:**` block must remain character-identical to its source `ctext` cell (verified by script before commit). Embedded modern editorial notes (e.g. `○…, 依宋元本` variant-collation notes in commentaries) are kept in ZH but omitted from EN, and the omission is recorded in the file's translator's note.
5. **No double translation:** a row marked `✅` or `🟡` is locked/completed (or in progress); pick `⬜` rows only, in schedule order unless Joey directs otherwise.
6. **Rate basis:** 18,600 Han chars/hr calibrated midpoint (3.2 min/1k), from the completed Zhuangzi.

**Session log:** every completed session appends a row to the Session Log at the bottom AND a summary entry in `TRANSLATION_LOG.md`.

---

## Completed ✅

| Book | Dir | Files | Han chars | Status | Pinyin |
|---|---|---|---|---|---|
| 莊子 Zhuangzi — Inner (7) | 道可道/莊子/內篇 | 7 | 13,793 | ✅ complete | ✅ backfilled |
| 莊子 Zhuangzi — Outer (15) | 道可道/莊子/外篇 | 15 | 28,046 | ✅ complete | ✅ backfilled |
| 莊子 Zhuangzi — Miscellaneous (11) | 道可道/莊子/雜篇 | 11 | 23,341 | ✅ complete | ✅ backfilled |
| 焦氏易林注 — 序 + juan 1 | 焦氏易林注 | 1/16 | 4,746 | ✅ complete (S1) | ✅ (native format) |

---

## Schedule — remaining work (~928k Han chars, ~59 sessions)

Each session targets ≤ ~18.6k Han chars (< 1 hr). Within multi-juan books, sessions proceed by juan/file order unless stated. A session may end mid-juan; record the juan **and section/line checkpoint** in the Session Log so the next session resumes exactly there.

### Sessions 1–17 — 焦氏易林注 (298,625 Han, 16 juan)

| Session | Work item | Est. Han | Status |
|---|---|---|---|
| S1 | 焦氏易林注 — 序, juan 1 (through 未濟, 64 sections) | ~24.2k | ✅ complete |
| S2 | 焦氏易林注 — juan 2 | ~24k | ⬜ |
| S3 | 焦氏易林注 — juan 3–4 | ~20k | ⬜ |
| S4 | 焦氏易林注 — juan 5–6 | ~20k | ⬜ |
| S5 | 焦氏易林注 — juan 7–8 | ~20k | ⬜ |
| S6 | 焦氏易林注 — juan 9–10 | ~20k | ⬜ |
| S7 | 焦氏易林注 — juan 11–12 | ~20k | ⬜ |
| S8 | 焦氏易林注 — juan 13–14 | ~20k | ⬜ |
| S9 | 焦氏易林注 — juan 15–16 + book verification | ~20k | ⬜ |

(Per-juan Han ~18–24k; sessions S3–S9 pair two juans ≈ 2 hrs of content each and should be split at the natural midpoint if a session runs long — log the checkpoint either way.)

### Sessions 10–14 — Medical corpus I (~125k Han)

| Session | Work item | Est. Han | Status |
|---|---|---|---|
| S10 | 黃帝內經/素問 — files 1–20 | ~22k | ⬜ |
| S11 | 黃帝內經/素問 — files 21–45 | ~24k | ⬜ |
| S12 | 黃帝內經/素問 — files 46–81 + verify | ~42k | ⬜ |
| S13 | 黃帝內經/靈樞經 — files 1–40 | ~32k | ⬜ |
| S14 | 黃帝內經/靈樞經 — files 41–81 + verify | ~33k | ⬜ |

### Sessions 15–20 — 易林補遺 + 焦氏易林 (~173k Han)

| Session | Work item | Est. Han | Status |
|---|---|---|---|
| S15 | 易林補遺 — file 1–2 | ~40k | ⬜ |
| S16 | 易林補遺 — file 3–5 + verify | ~58k | ⬜ |
| S17 | 焦氏易林 — files 乾–暌 (1–20) | ~24k | ⬜ |
| S18 | 焦氏易林 — files 蹇–夬 (21–42) | ~25k | ⬜ |
| S19 | 焦氏易林 — files 姤–未濟 (43–64) + verify | ~26k | ⬜ |

### Sessions 21–28 — Commentaries & ritual (~138k Han)

| Session | Work item | Est. Han | Status |
|---|---|---|---|
| S20 | 周禮 — 天官冢宰 | ~12k | ⬜ |
| S21 | 周禮 — 地官司徒 | ~12k | ⬜ |
| S22 | 周禮 — 春官宗伯 + 夏官司馬 | ~14k | ⬜ |
| S23 | 周禮 — 秋官司寇 + 冬官考工記 + verify | ~11k | ⬜ |
| S24 | 周易注 — 上經 (files 1–30) | ~22k | ⬜ |
| S25 | 周易注 — 下經 (files 31–64) + verify | ~24k | ⬜ |
| S26 | 道可道 — Dao De Jing base text | ~5k | ⬜ |
| S27 | 道可道 — 道德真經註 | ~17k | ⬜ |
| S28 | 道可道 — 河上公老子注 (canonical copy; root dir is verified duplicate — skip) | ~21k | ⬜ |

### Sessions 29–34 — Medical corpus II + 列子 (~72k Han)

| Session | Work item | Est. Han | Status |
|---|---|---|---|
| S29 | 傷寒論 — 22 files | ~31k | ⬜ |
| S30 | 金匱要略 — files 1–13 | ~15k | ⬜ |
| S31 | 金匱要略 — files 14–25 + 難經 + verify | ~29k | ⬜ |
| S32 | 道可道/列子 — 天瑞, 黃帝, 周穆王, 仲尼 | ~16k | ⬜ |
| S33 | 道可道/列子 — 湯問, 力命, 楊朱, 說符 + verify | ~15k | ⬜ |

### Sessions 34–39 — Divination & short texts (~62k Han)

| Session | Work item | Est. Han | Status |
|---|---|---|---|
| S34 | 火珠林 | ~17k | ⬜ |
| S35 | 道可道/鶡冠子 — 19 files | ~16k | ⬜ |
| S36 | 周易 (base text, 64 hexagrams) | ~13k | ⬜ |
| S37 | 京氏易傳 (64 files) | ~13k | ⬜ |
| S38 | 孝經 + 洪範 | ~3k | ⬜ |

### Backfill task (any spare session)

| Task | Status |
|---|---|
| Pinyin backfill for 莊子 (33 chapters, ZH→PY lines per section) | ⬜ |

---

## Session Log

| # | Date (UTC) | Worker | Work completed | Checkpoint for resume | Han | Uncertain |
|---|---|---|---|---|---|---|
| 0a | 2026-11-22 | Sarah | 莊子 Inner 7 (complete) | — | 13,793 | 20 |
| 0b | 2026-11-22 | Sarah | 莊子 Outer 15 (complete) | — | 28,046 | 8 |
| 0c | 2026-11-23 | Sarah | 莊子 Misc. 11 (complete) — book done | — | 23,341 | 11 |
| 1 (half) | 2026-11-23 | Sarah | 焦氏易林注: 序 + juan 1 sections 1–12 (乾–姤) | **resume juan 1 §13 同人** | ~1.9k | 1 |
| 1 (backfill) | 2026-11-23 | Sarah | Pinyin backfill: all 33 莊子 chapters (463 sections ZH→PY) — uniform ZH/PY/EN everywhere | — | 65,180 (already counted) | 0 |
| 1 (second half) | 2026-11-23 | Sarah | 焦氏易林注: juan 1 sections 13–64 (同人–未濟) — **juan 1 complete** | next: S2, juan 2 | ~2.9k | 2 |
