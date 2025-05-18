# 🥊 UFC Fighter Stats Database (SQLite)

Welcome to my very first custom-built database project, where I collected and structured real-world fighter data into a powerful SQLite database. This is part of a larger journey I'm on — learning how to engineer insights from raw data.

---

## 🚀 Project Summary

I built this from the ground up, starting with a Google Sheet of UFC fighter stats and transforming it into a fully queryable relational database using SQLite.

What seemed like a simple data import ended up teaching me:
- How to **clean and reshape real-world data**
- How to define a **robust SQL schema** for analytics
- How to use the **SQLite CLI** to build, import, and explore data
- The value of debugging weird CSV quirks and primary key errors 😅

---

## 🧠 Skills Demonstrated
- SQL: Schema design, querying, table constraints
- SQLite CLI: File-based database creation, `.import`, `.schema`, `.mode box`
- Data wrangling: Formatting CSV headers, primary key management
- GitHub: Uploading, managing CSV files for public access

---

## 📊 Example Query: Wins by Submission
```sql
.headers on
.mode box
SELECT Name, WinsBySubmission
FROM fighters
ORDER BY WinsBySubmission DESC
LIMIT 10;

TABLE:

-- MMA Fighters Table Schema
CREATE TABLE fighters (
    ID INTEGER PRIMARY KEY,
    Name TEXT NOT NULL,
    Nickname TEXT,
    Age INTEGER,
    Weight_Class_Lbs INTEGER,
    Stance TEXT,
    Height_cm INTEGER,
    Reach_cm INTEGER,
    Wins INTEGER,
    Losses INTEGER,
    Draws INTEGER,
    No_Contests INTEGER,
    Average_Fight_Time TEXT,  -- Stored as 'mm:ss' string
    Strikes_Landed_per_Minute REAL,
    Striking_Accuracy_Percent INTEGER,
    Strikes_Absorbed_per_Minute REAL,
    Striking_Defense_Percent INTEGER,
    Takedowns_Average_per_15min REAL,
    Takedown_Accuracy_Percent INTEGER,
    Takedown_Defense_Percent INTEGER,
    Submission_Average_per_15min REAL,
    Wins_by_KO_TKO INTEGER,
    Wins_by_Submission INTEGER,
    Wins_by_Decision INTEGER
);

💡 Next Steps
This is just the start. I plan to:

Connect this data to Tableau or Power BI

Build a prediction engine for upcoming UFC fights

Use this dataset to create visuals and insights for my YouTube channel The Data Terminal 🎥📊

Stay tuned for Part 2 where I explore fight outcome prediction using fighter stats!

📂 Files Included
fighters.db — SQLite3 database with full fighter data

fighters.csv — Original CSV with headers

fighters_noheader.csv — Cleaned CSV for import

schema.sql — Custom SQL schema used for table creation

📬 Connect with Me
If you enjoy combat sports + data or you're learning SQL too, let’s connect!

📧 tonyxia.eth
📸 YouTube: https://www.youtube.com/@Thedataterminal
💼 LinkedIn: https://www.linkedin.com/in/tony-xia-4b9201237/

