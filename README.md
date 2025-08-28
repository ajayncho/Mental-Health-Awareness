# Mental-Health-Awareness
International Students Mental Health Analysis
📖 Project Overview

This project explores how studying abroad impacts the mental health of international students in Japan. Using SQL, I analyzed a dataset of students surveyed in 2018 to investigate the relationship between length of stay and three mental health indicators: depression (PHQ), social connectedness (SCS), and acculturative stress (AS). The database and analysis were conducted on DataCamp.

🔗 View the project on DataCamp

🛠️ Methods

Filter: Selected only international (Inter) students.

Group: Used GROUP BY to organize data by length of stay (in years).

Aggregate:

COUNT() → number of students in each group

AVG() + ROUND() → mean scores (rounded to 2 decimals) for PHQ, SCS, and AS

Sort: Applied ORDER BY to display results in descending order of stay.

Example Query
SELECT 
    stay AS stay,
    COUNT(inter_dom) AS count_int,
    ROUND(AVG(todep), 2) AS average_phq,
    ROUND(AVG(tosc), 2) AS average_scs,
    ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter' 
  AND stay <> 0
GROUP BY stay
ORDER BY stay DESC;

📊 Results

Depression (PHQ): Low at first, but increases sharply after 5+ years.

Social connectedness (SCS): Declines steadily with longer stays.

Acculturative stress (AS): Peaks around 4–5 years, then slightly decreases.

✅ Conclusion

The results align with a 2018 Japanese university study: international students face higher mental health risks, and social connectedness and acculturative stress are key predictors of depression. My analysis suggests that length of stay is a significant contributing factor.
