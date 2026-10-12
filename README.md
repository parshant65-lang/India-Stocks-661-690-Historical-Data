# India-Stocks-661-690-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 661 to 690)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-661-690-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (661 to 690)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 661 | `ARROWGREEN` | Arrow Greentech Limited | `ARROWGREEN.NS` |
| 662 | `ARSHIYA` | Arshiya Limited | `ARSHIYA.NS` |
| 663 | `ARSSBL` | Anand Rathi Share and Stock Brokers Limited | `ARSSBL.NS` |
| 664 | `ARTEMISMED` | Artemis Medicare Services Limited | `ARTEMISMED.NS` |
| 665 | `ARTNIRMAN` | Art Nirman Limited | `ARTNIRMAN.NS` |
| 666 | `ARVEE` | Arvee Laboratories (India) Limited | `ARVEE.NS` |
| 667 | `ARVIND` | Arvind Limited | `ARVIND.NS` |
| 668 | `ARVINDFASN` | Arvind Fashions Limited | `ARVINDFASN.NS` |
| 669 | `ARVSMART` | Arvind SmartSpaces Limited | `ARVSMART.NS` |
| 670 | `ARYAMAN` | Aryaman Financial Services Limited | `ARYAMAN.NS` |
| 671 | `ASAHISONG` | Asahi Songwon Colors Limited | `ASAHISONG.NS` |
| 672 | `ASAL` | Automotive Stampings and Assemblies Limited | `ASAL.NS` |
| 673 | `ASALCBR` | Associated Alcohols & Breweries Ltd. | `ASALCBR.NS` |
| 674 | `ASHAPURMIN` | Ashapura Minechem Limited | `ASHAPURMIN.NS` |
| 675 | `ASHIANA` | Ashiana Housing Limited | `ASHIANA.NS` |
| 676 | `ASHIKAG` | Ashika Global Securities Limited | `ASHIKAG.NS` |
| 677 | `ASHIMASYN` | Ashima Limited | `ASHIMASYN.NS` |
| 678 | `ASHOKA` | Ashoka Buildcon Limited | `ASHOKA.NS` |
| 679 | `ASHOKAMET` | Ashoka Metcast Limited | `ASHOKAMET.NS` |
| 680 | `ASIANENE` | Asian Energy Services Limited | `ASIANENE.NS` |
| 681 | `ASIANHOTNR` | Asian Hotels (North) Limited | `ASIANHOTNR.NS` |
| 682 | `ASIANTILES` | Asian Granito India Limited | `ASIANTILES.NS` |
| 683 | `ASIANTNE` | Asian Tea & Exports Limited | `ASIANTNE.NS` |
| 684 | `ASKAUTOLTD` | ASK Automotive Limited | `ASKAUTOLTD.NS` |
| 685 | `ASMS` | Avio Smart Market Stack Limited | `ASMS.NS` |
| 686 | `ASPINWALL` | Aspinwall and Company Limited | `ASPINWALL.NS` |
| 687 | `ASSAMENT` | Assam Entrade Limited | `ASSAMENT.NS` |
| 688 | `ASTAR` | Asian Star Company Limited | `ASTAR.NS` |
| 689 | `ASTEC` | Astec LifeSciences Limited | `ASTEC.NS` |
| 690 | `ASTRAMICRO` | Astra Microwave Products Limited | `ASTRAMICRO.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ARROWGREEN 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-661-690-Historical-Data/main/ARROWGREEN/1m/2026/10/ARROWGREEN_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
