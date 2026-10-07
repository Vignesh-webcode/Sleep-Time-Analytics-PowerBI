# Sleep-Time-Analytics-PowerBI
An interactive 3-page Power BI dashboard evaluating workforce sleep patterns, screen latency metrics, and lifestyle behaviors.

<img width="500" height="293" alt="Page 1" src="https://github.com/user-attachments/assets/3fc9439c-d5e4-48fc-a1c6-c8bdac1e37cd" />
<img width="500" height="296" alt="Page 3" src="https://github.com/user-attachments/assets/14cc2faa-8d0e-45ca-8627-d10376881f10" />
<img width="502" height="293" alt="Page 2" src="https://github.com/user-attachments/assets/34e94c78-196d-416a-a8dd-ef99eda8b346" />

---


**Project Overview**

Using a multi-variable sleep dataset, this mini-project analyzes the root causes of workforce exhaustion. It evaluates how acute sleep deficits alter internal recovery and tracks the precise point where late-night phone habits translate into next-day fatigue.

Dashboard Architecture


**Page 1: Executive Sleep Health Summary**

• Features top KPI cards for Average Sleep (6.27 hours), Screen Time (59 mins), and Total Snoozes.
• Breaks down population percentages across different sleep debt categories using a Donut Chart.

**Page 2: Digital Hygiene and Circadian Analytics**

• Maps screen brightness percentages against an Average Fatigue Score metric.
• Uses a cross-tab Matrix to track bedtime app usage against biological chronotypes (Night Owls vs. Morning Larks).

**Page 3: Behavioral Correlation Matrix**

• Displays deep sleep vs. REM sleep architectures across severe debt categories.
• Includes global button slicers to instantly filter the entire project by Chronotype and Occupation.

**Technical Execution**

**Power Query ETL**

• Forced strict numeric constraints on decimals and whole numbers.
• Converted the numerical 'blue_light_filter_active flag' (1/0) into a clean True/False logical switch.

**Core DAX Measures**

**DAX**
-- 1. Average Next-Day Fatigue Baseline
Average Fatigue Score = AVERAGE('bedtime_screentime_project'[next_day_fatigue_score])

-- 2. Average Sleep Duration Tracked
Average Sleep = AVERAGE('bedtime_screentime_project'[total_sleep_hours])

**Note for Users**: Open the .pbix file locally, hold down the Ctrl key, and click the top header buttons to navigate between pages.
