# README

# Premier League 2025/26 Data Analysis Dashboard

An interactive Power BI dashboard analyzing the Premier League 2025/26 season — covering player performance, team statistics, discipline, and squad demographics across all 20 clubs and ~551 players.

## 🎯 Why I Built This

After my first year of uni, I had a 5-month break and tried to land an internship but it didn’t work out. Doing some research made it clear that hands-on projects would be a real asset for future internship applications, especially heading into 3rd year. Since I’m doing a Data Analytics degree and I’m genuinely into football, this felt like the natural first project to build a portfolio around.

## 🗄️ Data Source & Collection

All data was sourced from FBref, a football statistics website, covering the full 2025/26 Premier League season.

I initially tried scraping the data with Python, but ran into HTTP 403 errors (access restrictions), so I manually downloaded the relevant tables from FBref as CSV files instead — covering player info (name, age, nationality, position, club) and performance stats (goals, assists, minutes played, cards, and more) for all 20 clubs.

## 🛠️ How It Was Built

This followed a full relational database workflow, not just a straight CSV-to-dashboard import:

1. **Cleaning:** Raw CSVs were cleaned and processed with Python (Pandas) in Jupyter Notebook
2. **Database:** Built a relational SQLite database using Python’s `sqlite3` library, structured into three related tables — `Teams`, `Players`, and `PlayerStats` — with primary/foreign key relationships to normalize the data and remove redundancy
3. **Analysis:** Wrote SQL queries against the database to explore a range of football analytics questions
4. **Dashboard:** Exported the cleaned tables back to CSV and built the final interactive dashboard in Power BI, including custom DAX measures for things like per-90 efficiency, team-relative percentages, and ranking logic

**Tools used:** Python, Pandas, Jupyter Notebook, SQLite, SQL, Power BI, DAX

## 📊 Dashboard Pages

**1. Season Overview** — League-wide KPIs and top 10 rankings for goalscorers and assist providers.

**2. Team Analysis** — Goals vs assists by team, squad age vs scoring output, and a color-coded discipline heatmap ranking every team by cards received.

**3. Player Performance** — Goal contribution efficiency (per-90 minutes), each player’s share of their team’s total goals, goal distribution by position, and each team’s top scorer.

**4. Player Deep Dive** — Goals by age bracket, most-carded individual players, and squad nationality breakdown.

## 💡 Insights I Found Interesting

- **Jarrod Bowen** finished as the 3rd highest assist provider in the entire league
- **Arsenal** went the full season without a single red card
- The goals-scored-vs-squad-age chart makes an intuitive trend (younger squads scoring more) genuinely visible rather than just assumed
- **Midfielders** scored more goals than forwards across the league — not what I expected going in
- **Igor Thiago** was responsible for 41% of his team’s total goals this season

## 📁 Files

- `PremierLeague2025_26_Dashboard.pbix` — the full Power BI report

## 🚀 How to View

Download the `.pbix` file and open it in Power BI Desktop (free) to explore the dashboard interactively.

## 📝 Notes

This was my first project of this scale — built on and off over about a month (with breaks in between). The dashboard itself was the hardest and most enjoyable part, since a lot of visuals needed reworking or scrapping entirely when the original queries didn’t hold up. AI tools were used to assist with parts of the data cleaning and dashboard troubleshooting process.

---

*A personal data analytics portfolio project, built to support future internship applications.*