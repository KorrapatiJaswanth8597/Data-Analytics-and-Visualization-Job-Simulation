# 📊 Content Popularity Analysis Based on Reactions

This project performs an analysis of content popularity based on user reactions using structured data. The goal is to identify the **top 5 content categories** with the highest engagement scores, where *popularity is quantified by the sentiment score associated with each reaction type*.

## 🧠 Objective

To provide the client with insights into which **content categories resonate the most with users**, helping guide future content strategies.

---

## 🗃️ Datasets

The analysis is based on three datasets:

1. **Content.csv**
   - `Content_ID`
   - `User_ID`
   - `Type` (e.g., video, GIF, audio)
   - `Category` (e.g., animals, food, technology)
   - `URL`

2. **Reactions.csv**
   - `Content_ID`
   - `User_ID`
   - `Type` (reaction type like "love", "adore")
   - `Datetime`

3. **ReactionTypes.csv**
   - `Type` (reaction type)
   - `Sentiment` (qualitative sentiment)
   - `Score` (numeric value representing sentiment intensity)

---

## 🛠️ Tools & Technologies

- Microsoft SQL Server
- SQL for data querying and aggregation
- Data visualization tools (optional)
- Microsoft Excel

---

## 📌 Query Used

```sql
SELECT TOP 5  category, SUM(Score) AS Reaction_Score
FROM merged_content_reactions
GROUP BY Category
ORDER BY Reaction_Score DESC;

---


## **Insights on Top 5 Popular Content Categories**

1) Animals top the chart with a total score of 68,624, indicating that content 
related to animals generates the strongest emotional connection and engagement from users.


2) Science (65,405) and Healthy Eating (63,138) are also highly popular 
  categories, showing a strong user interest in educational and wellness content.

3) Technology (63,035) and Food (61,598) closely follow, suggesting that innovation
   and lifestyle content continue to be important pillars of engagement.

---


