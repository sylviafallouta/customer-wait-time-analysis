Customer Wait-Time Improvement Project

Simulated a small-branch customer queue and showed that an express line, which sends long transactions to an existing staff member, cuts average wait time by about 75% (6.9 → 1.75 minutes) without adding employees.

Independent Systems Engineering project · Operations and process improvement · Inspired by queue patterns I observed working as a bank teller.

Note: All data is simulated for educational purposes. No real customer or bank data is used.

Problem

During busy periods, customers at a small branch can wait a long time before being served. The goal was to find what causes the waiting and design a process change that reduces it without adding staff.

Stakeholders and Requirements
Stakeholder	What they need
Customers	Short, predictable wait times
Tellers	A steady, manageable flow of customers
Branch manager	Better service with no added labor cost

Requirements

R1: Reduce average customer wait time.
R2: Add no employees (use existing staff only).
R3: Don't make long-transaction customers wait unreasonably long.
Current Process

One teller serves every customer, first come, first served.

Show Image

Root causes of waiting

Peak demand: several customers arrive close together (9:30–9:33).
Long transactions block the line: a 12- or 15-minute transaction makes every quick customer behind it wait.
Proposed Improvement: Express Line

Transactions expected to take 10 minutes or more go to the personal banker, who is already on staff. Quick transactions stay with the teller.

Show Image

Method
Item	Value
Customers simulated	8 (arrivals 9:00–9:33, with a peak at 9:30–9:33)
Service times	3–4 min (quick) and 12–15 min (long)
Long-transaction rule	10+ minutes goes to the personal banker
Current process	1 teller serves everyone
Express line	1 teller (quick) + 1 personal banker (long), same staff
Queue rule	First come, first served at each server
Measure	Wait time = service start − arrival time
Tools	Google Sheets / Excel, diagrams.net

Both scenarios use the same customers and the same service times, so the only thing that changes is the process. The full calculations, with formulas, are in customer_wait_time_data.xlsx, and the raw data is in customer_wait_time_data.csv.

Results

Show Image

Metric	Current process	Express line
Average wait, all customers	6.88 min	1.75 min
Average wait, quick transactions	6.83 min	0.67 min
Average wait, long transactions	7.00 min	5.00 min
Longest single wait	28 min	10 min
Staff serving customers	1	2 (no one added)

Average wait dropped by about 75% without adding employees.

Trade-offs
Long-transaction customers still wait. Customer 7 (15-minute transaction) waited 10 minutes because the personal banker was busy with customer 5. Long-transaction customers are still better off on average (7 → 5 min), but this is where the remaining wait is concentrated.
The personal banker's other work is interrupted. Their time spent on the express line isn't available for their usual tasks.
The rule depends on sorting customers correctly. Someone (a greeter or the teller) has to estimate the transaction length up front. Customers sent to the wrong line would reduce the benefit.
Limitations and Next Steps
The sample is small (8 customers) and simulated. The results should be validated with real, anonymized timing data before implementing.
Test different arrival rates and peak sizes.
Test other thresholds for "long" (for example, 8 or 12 minutes). The spreadsheet's threshold cell can be changed to do this.
Compare other options, such as appointments for long transactions or a shared queue for both staff.
Files
File	Description
customer_wait_time_data.xlsx	Both scenarios with formulas, plus a summary tab
customer_wait_time_data.csv	Raw simulated data for both scenarios
current_process.png	Current process flowchart
express_line_process.png	Express-line process flowchart
wait_time_comparison.png	Results chart
Customer Wait-Time Improvement Project.pdf	Project report
Skills Demonstrated

Process mapping · Bottleneck and root-cause analysis · Queue simulation · Requirements and stakeholder analysis · Trade-off evaluation · Spreadsheet modeling · Data visualization · Technical documentation

Potential next steps include testing different customer-arrival rates, evaluating service capacity, and comparing alternative process configurations to determine whether the improvement remains effective under different conditions.

## Project Type

Independent Systems Engineering project focused on operations and process improvement.
