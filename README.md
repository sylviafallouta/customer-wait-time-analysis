<h1 align="center">Customer Wait-Time Improvement Project</h1>

<p align="center">
  <em>An independent systems engineering project that analyzes a bank branch's lunch rush and compares process designs that reduce lobby wait times with no additional staff.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Completed-2E8B57" alt="Status: Completed">
  <img src="https://img.shields.io/badge/Field-Systems%20Engineering-3B5BA9" alt="Field: Systems Engineering">
  <img src="https://img.shields.io/badge/Data-Simulated-777777" alt="Data: Simulated">
</p>

---

## Summary

| | |
|---|---|
| **Problem** | When the drive-through backs up, quick-transaction customers come inside and wait behind long transactions |
| **Goal** | Reduce lobby wait times **without adding or moving employees** |
| **Setting** | A branch with 4 lobby tellers, 2 drive-through tellers, and 3 personal bankers |
| **Key result** | A 2-window express lane cut quick-transaction waits by **41%** and overall waits by **26%** |
| **Data** | Fully simulated; no real customer or bank data used (see below) |

---

## Data and Confidentiality

All customer data in this project is **simulated for educational purposes**.

- No real customer information, transaction records, or account data was used.
- No internal bank policies, procedures, or systems are described.
- The bank is not named. Only general staffing levels were used to make the scenario realistic.

---

## Objectives

1. Map the current customer-service process.
2. Simulate a lunch rush and measure customer wait times.
3. Identify the bottleneck.
4. Compare design alternatives against the current process.

---

## Current Process

<p align="center">
  <img src="Current%20Customer%20Process.png" width="650" alt="Current customer process flowchart">
</p>

**Causes of waiting identified:**
1. **Peak demand and drive-through overflow:** when the drive-through line is long, quick-transaction customers come inside.
2. **Long service time:** long transactions (12 minutes) occupy lobby tellers while quick customers (3 minutes) wait behind them in the same line.

---

## Design Alternatives

Only the 4 lobby tellers are reassigned. Drive-through tellers and personal bankers keep their normal duties.

| Design | Tellers 1–2 | Tellers 3–4 |
|---|---|---|
| **Current Process** | Any transaction (one shared line) | Any transaction |
| **Option 1:** 1 Express Window | Teller 1 quick only; Teller 2 any | Any transaction |
| **Option 2:** 2 Express Windows | Quick transactions only (express lane) | Any transaction |

<p align="center">
  <img src="Express%20Lane%20Process.png" width="600" alt="Proposed express lane process flowchart">
</p>

---

## Results

Simulated lunch rush: 16 customers come inside between 12:00 and 12:08 (12 quick, 4 long).

<p align="center">
  <img src="Average%20Wait%20Chart.png" width="680" alt="Average wait time chart">
</p>

| Measure | Current | Option 1 | Option 2 |
|---|:---:|:---:|:---:|
| Average wait, all customers | 5.50 min | 5.50 min | **4.06 min (-26%)** |
| Average wait, quick transactions | 6.50 min | 6.50 min | **3.83 min (-41%)** |
| Average wait, long transactions | 2.50 min | 2.50 min | 4.75 min (+2.25) |
| Longest single wait | 11 min | 11 min | 10 min |

### Key Findings

- **One express window did not help.** In the shared line, tellers not tied up with long transactions were already serving quick customers, so reserving one window only changed *which* teller did that work.
- **Two express windows made a real difference.** Quick-transaction customers, most of the lunch rush, waited 41% less.
- **Trade-off:** Long-transaction customers waited about 2 minutes longer on average, since only 2 tellers serve them.

### Recommendation

Adopt the **2-window express lane** during the lunch rush. Next steps:
1. Let express tellers serve the regular line when the express lane is empty.
2. Test with a larger simulation using random arrival times.
3. With management approval, collect anonymous, aggregate timing data to confirm the results.

---

## Project Files

| File | Contents |
|---|---|
| [Customer Wait-Time Improvement Project.pdf](Customer%20Wait-Time%20Improvement%20Project.pdf) | Full project report |
| [Customer Wait Time Data.xlsx](Customer%20Wait%20Time%20Data.xlsx) | Simulated data for all 3 designs, wait-time formulas, and comparison chart |
| [Current Customer Process.png](Current%20Customer%20Process.png) | Current process flowchart |
| [Express Lane Process.png](Express%20Lane%20Process.png) | Proposed process flowchart |
| [Average Wait Chart.png](Average%20Wait%20Chart.png) | Results chart |

**Tools:** Google Sheets, diagrams.net, Google Docs

---

<p align="center">
  <sub>Prepared by Sylvia Fallouta, Systems Engineering student · November 2026</sub>
</p>
