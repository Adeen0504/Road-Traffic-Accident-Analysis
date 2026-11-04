# Road Traffic Accident Analysis (Python)

A Python analysis of 12,316 road accidents: who was driving, the road and weather, what went wrong, and how badly people were hurt. The goal is to find clear patterns that could help make roads safer.

## Questions this project answers
- Do accidents differ by time of day, or between day and night?
- Do new and experienced drivers crash in different ways?
- Which age groups appear most, and at what severity?
- What are the main causes of accidents, and do they change by place?
- How do wet roads and bad weather change the picture?

## Data
- Road traffic accident dataset (RTA), 12,316 rows and 32 columns, provided by the Imarticus module.
- One row is one accident. Columns cover the driver, vehicle, road, weather, people hurt and severity.
- The CSV is not included in this repository. To run the notebook, put it in the same folder as the notebook.

## What I did
1. **Understood the data:** checked shape, columns and types.
2. **Cleaned it:** checked blanks and repeated rows (none found), and removed extra spaces from text columns so the same place isn't counted as two. Blank values were left as they are, not guessed. One place label (`Rural village areasOffice areas`, about 20 rows) looks like two names stuck together, and I left it because I can't tell which place was meant.
3. **Added new columns:** `Hour`, `Time_period`, `Driver_experience_group` (inexperienced means under 2 years of driving or no licence) and `Day_Night`.
4. **Explored the data (EDA):** compared groups using percentages, so larger groups don't look worse just for being larger.
5. **Wrote 4 insights and 4 charts.**

## Key findings
- **Collision type is similar by day and night.** Vehicle-with-vehicle collisions are 72.6% by day and 71.1% at night.
- **New and experienced drivers crash in similar ways.** Rollovers are the one difference: 4.2% for inexperienced drivers against 3.0% for experienced ones. About 830 accidents with no experience record are left out.
- **Young drivers appear most.** Drivers aged 18–30 are 39.2% of fatal accidents and about 35% of serious and slight ones. This shows who is in the accidents, not who is most at risk.
- **Not keeping a safe distance is the top cause almost everywhere.** It is 21.4% of accidents in recreational areas, 19.0% in church areas and 18.6% in office areas. The exception is hospital areas, where changing lanes to the left comes first.
- **Wet roads matter more at night.** Wet or damp roads are 37.3% of night accidents against 18.1% of day accidents.
- **Severity:** 84.6% slight, 14.2% serious, 1.3% fatal (about 160 accidents).

## Recommendations
Run safe-distance campaigns, improve lighting and drainage, and collect cleaner place data, since the largest place group is simply labelled "Other".

## Limits
These results show patterns, not causes. They also don't account for how many people drive in each group or place. Fatal accidents are only about 160 cases, so their percentages can swing a lot.

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook.

## Files
- `Accident_Analysis_Project.ipynb`: the full analysis, from cleaning to conclusions
- `RTA_cleaned.csv`: created when you run the notebook (the cleaned dataset)

## My role
I decided what to analyse and how to approach it. AI assistance was allowed for this module project.

## Author
Meer Adeen Ali · Hyderabad · [LinkedIn](https://www.linkedin.com/in/adeen-ali) · [GitHub](https://github.com/Adeen0504)

Built during the Imarticus Postgraduate Program in Data Science and Analytics with GenAI.
