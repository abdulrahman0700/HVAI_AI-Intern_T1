# HVAI AI Intern — Task 01: Olist Business Discovery

Data analysis internship task for **HVIA (Data & AI Solutions)**. The goal isn't just to produce charts — it's to understand Olist as a business, find real frictions in how it operates, and think through where HVIA could add value as a solutions partner.

## About Olist

[Olist](https://olist.com) is a Brazilian retail technology ecosystem that helps small and medium sellers reach customers through 170+ integrated marketplaces, handling ERP, ecommerce, payments, logistics, business credit, and AI tooling in one platform.

## Dataset

[Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle) — ~100,000 real, anonymized orders placed across multiple marketplaces in Brazil between 2016 and 2018. It spans customers, orders, order items, payments, reviews, products, sellers, and geolocation data across multiple linked CSV files.

Raw data lives in [`Datasets/Task_1`](./Datasets/Task_1).

## What's in this repo

| File | Description |
|---|---|
| [`HVIA_T1_Olist_Discovery.ipynb`](./HVIA_T1_Olist_Discovery.ipynb) | Main analysis notebook — loads the Olist tables and answers the Discovery Mission questions below using pandas and matplotlib |
| `Datasets/Task_1/` | Source CSV files (customers, orders, order items, payments, reviews, products, sellers, geolocation, category translation) |
| `LICENSE` | Apache-2.0 |

## Discovery Mission — questions this notebook answers

1. **What is happening in the business?** — order volume growth over time, total revenue, and average order value.
2. **Where are the frictions or challenges?** — delivery delays, the link between late delivery and review score, and the geographic mismatch between where sellers and customers are based.
3. **What patterns or trends deserve attention?** — payment method mix and installment behavior, and the overall distribution of review scores.
4. **What would management need to understand?** — a plain-language summary tying the numbers back to business risk and opportunity.
5. **What evidence supports the conclusions?** — a summary table of the key figures behind each finding.

## Key findings

- Order volume grew substantially month over month across the sample period — Olist scaled quickly.
- **Late deliveries significantly lower customer satisfaction**: average review scores drop sharply when an order arrives after its estimated delivery date compared to on-time orders.
- **Sellers are heavily concentrated in São Paulo state**, while customers are spread across the whole country — a likely structural driver of delivery delays for more distant regions.
- Most customers pay by credit card, frequently split into several installments, pointing to price sensitivity.
- Review scores skew positive overall, but negative reviews cluster around delivery problems.

## How to run

```bash
git clone https://github.com/abdulrahman0700/HVAI_AI-Intern_T1.git
cd HVAI_AI-Intern_T1
pip install pandas matplotlib jupyter
jupyter notebook HVIA_T1_Olist_Discovery.ipynb
```

Update the `path` variable in the first code cell if your CSVs live somewhere other than `Datasets/Task_1/`.

## License

Apache-2.0 — see [LICENSE](./LICENSE).
