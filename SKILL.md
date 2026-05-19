# Chinese Divination Skill

Perform traditional Chinese divination. Pure computation, no LLM fabrication.

## How It Works

Run the standalone Python script `divination.py`. It reads from `data/` JSON files and outputs text results.

**Important**: Always run the script to get results. Do NOT fabricate or improvise divination output.

## Commands

When the user says any of these, run the corresponding command:

| Trigger | Command | Example |
|---------|---------|---------|
| `/六爻` or "六爻" or "liuyao" | `python divination.py liuyao "[question]"` | `/六爻 近期财运如何` |
| `/梅花` or "梅花" or "meihua" | `python divination.py meihua "[input]"` | `/梅花 38` or `/梅花 山水` |
| `/诸葛` or "诸葛" or "zhuge" | `python divination.py zhuge "[3 chars]"` | `/诸葛 叶天雨` |
| `/占卜` or "占卜" or menu | `python divination.py menu` | `/占卜` |

## Execution

Run from the project directory:
```bash
python divination.py <command> [args]
```

Execute via shell/bash, capture stdout, and present the output directly to the user.

## Notes

- Pure Python 3, zero dependencies, no pip install needed
- All 64 hexagrams and 384 Zhuge poems are in the bundled JSON data
- Results are randomly generated each time (coin casting / stroke-based)
- For `liuyao`, pass the user's question as the argument
- For `meihua`, pass numbers or Chinese characters
- For `zhuge`, need exactly 3 Chinese characters
