# Chinese Divination Skills

Traditional Chinese divination tools with complete databases — pure Python, zero dependencies.

> **Any AI platform** can use this. Just tell it: "clone this repo, run `python divination.py` to do divination."

## Features

- **Liuyao (六爻)** — Six-Line coin casting divination with 64 hexagrams
- **Meihua (梅花易数)** — Plum Blossom numerology via numbers or character strokes
- **Zhuge (诸葛神算)** — Zhuge Liang's 384-poem divination system

All data included: 64 hexagrams with judgments, images, readings + 384 Zhuge poems with interpretations.

## Quick Start

```bash
git clone https://github.com/PAOHUISYB/chinese-divination-skills.git
cd chinese-divination-skills

python divination.py liuyao "近期财运如何"
python divination.py meihua 38
python divination.py zhuge 龙天雨
python divination.py menu
```

Also supports Chinese command names: `python divination.py 六爻 近期财运`

## AI Integration

`SKILL.md` is a universal AI instruction file. Compatible with:

- **WorkBuddy** — place in `~/.workbuddy/skills/divination/`
- **QwenPaw / QClaW** — import as custom skill or feed `SKILL.md` as system prompt
- **Claude / ChatGPT / any LLM** — paste the content of `SKILL.md` into the system prompt or project instructions

## AstrBot Plugin

The `astrbot-plugin/` directory contains the AstrBot plugin version.

```bash
cp -r astrbot-plugin/astrbot_plugin_divination /path/to/AstrBot/data/plugins/
```

Commands: `/六爻`, `/梅花`, `/诸葛`, `/占卜`

## Data

| File | Description | Size |
|------|-------------|------|
| `data/hexagrams.json` | 64 hexagrams with full readings | ~30KB |
| `data/zhuge.json` | 384 Zhuge poems with interpretations | ~67KB |
| `data/liuyao.json` | Supplementary Liu Yao data | ~9KB |

## License

MIT
