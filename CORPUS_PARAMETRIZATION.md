# Corpus Parametrization — Remaining Chinese Texts

Date: 2026-11-23 | Worker: Sarah | Basis: calibrated throughput from the completed Zhuangzi translation (PR #3)

## Methodology

- **Counting:** For every HTML capture, Han characters are counted inside `class="ctext"` cells only (the body text), excluding navigation, UI, dictionary views, and editorial footnotes. Files without ctext cells (root-level artifacts) are counted separately as duplicates/tooling.
- **Rate calibration** (observed on the completed Zhuangzi, 65,180 Han chars in ~3.5 h):
  - **Midpoint (recommended): 18,600 Han chars/hour** (~3.2 min/1k) — Outer + Miscellaneous Chapters worked fresh at full scholarly bar (crux-flagging, glossary discipline, automated fidelity checks).
  - **Optimistic: 25,000/hour** — observed on the deeply familiar Inner Chapters.
  - **Conservative: 5,000/hour** — planning floor for difficult/unfamiliar corpora (medical literature, dense commentarial prose).
- A "session" = one under-an-hour work session.

## Already complete

| Book | Sections | Han chars |
|---|---|---|
| 莊子 Zhuangzi (Inner 7 + Outer 15 + Miscellaneous 11) — **done** | 463 | 65,180 |

## Remaining books (net corpus)

| Book | Files | Han chars | Sessions @18.6k/hr | @25k | @5k |
|---|---|---|---|---|---|
| 焦氏易林注 (Jiaoshi Yilin commentary, 16 juan) | 16 | 298,625 | 17 | 12 | 60 |
| 易林補遺 (Yilin Buyi) | 5 | 97,648 | 6 | 4 | 20 |
| 黃帝內經/素問 (Suwen) | 81 | 88,232 | 5 | 4 | 18 |
| 焦氏易林 (Jiaoshi Yilin) | 64 | 75,096 | 5 | 4 | 16 |
| 黃帝內經/靈樞經 (Lingshu) | 81 | 64,905 | 4 | 3 | 13 |
| 周禮 (Rites of Zhou) | 6 | 49,391 | 3 | 2 | 10 |
| 周易注 (Wang Bi commentary) | 64 | 45,745 | 3 | 2 | 10 |
| 道可道 — Dao De Jing + Laozi commentaries | 3 | 43,147 | 3 | 2 | 9 |
| 傷寒論 (Shang Han Lun) | 22 | 31,438 | 2 | 2 | 7 |
| 道可道/列子 (Liezi) | 8 | 30,899 | 2 | 2 | 7 |
| 金匱要略 (Jinkui Yaolue) | 25 | 28,489 | 2 | 2 | 6 |
| 火珠林 (Huo Zhu Lin) | 1 | 17,029 | 1 | 1 | 4 |
| 道可道/鶡冠子 (He Guan Zi) | 19 | 15,795 | 1 | 1 | 4 |
| 周易 (Yijing, base text) | 64 | 13,381 | 1 | 1 | 3 |
| 京氏易傳 (Jingshi Yizhuan) | 64 | 13,316 | 1 | 1 | 3 |
| 難經 (Nan Jing) | 13 | 11,963 | 1 | 1 | 3 |
| 孝經 (Xiaojing) | 1 | 1,798 | 1 | 1 | 1 |
| 洪範 (Great Plan) | 1 | 1,071 | 1 | 1 | 1 |
| **TOTAL** | **618** | **927,968** | **~59** | **~45** | **~194** |

## Excluded (verified duplicates / non-corpus)

- `河上公老子注/` (top-level dir): byte-identical duplicate of the copy under `道可道/` (md5 verified) — 20,660 Han already included in the 道可道 entry; netted out of the total.
- Root-level `hexagram_*.html` (66 files, 169,898 Han): pipeline artifacts — duplicates of 周易 hexagram pages plus glossary-annotated variants. Excluded to avoid double counting; the 周易 book itself is counted once above.
- `James DeKorne*.html` (64 files): English-language source content (Gnostic Book of Changes) — 0 Han characters; not part of the Chinese corpus.
- `Unihan_*.txt`, `auxiliary/`, `extracted/`, `emoji/`, `xtra/`, `scripts/`, `logs/`, `output/`, `seasdf/`: Unicode data files and project tooling, not translation targets.

## Bottom line

- **~928,000 Han characters remain** across 19 books and 618 files.
- **~59 under-an-hour sessions** at the calibrated midpoint rate (≈49.9 worker-hours); **~45 sessions** at the optimistic rate; **~194 sessions** at the conservative floor.
- Distribution note: the corpus is front-loaded — **焦氏易林注 alone is ~30% of the total** (17 of 59 mid-rate sessions). The four medical classics (素問, 靈樞經, 傷寒論, 金匱要略, 難經 ≈ 214k Han) should be budgeted at the conservative rate because of specialized terminology; conversely the Yijing-family texts (周易, 京氏易傳, 焦氏易林, 周易注) are highly repetitive and will run at or above the midpoint rate.
- Quality bar per session remains: ZH/EN aligned pairs, consistent master glossary, `[uncertain]` flags on cruxes, automated ZH-to-source fidelity checks, per-session `TRANSLATION_LOG.md` entry.
