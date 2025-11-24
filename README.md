# BrightTV Viewership Analytics – Full Snowflake Setup (2025)

This project contains everything you need to load, clean, and analyze the BrightTV case study data in **Snowflake** in under 2 minutes.

## Files Included
- `BrightTV_Viewership.csv` – Raw viewership sessions (already provided)
- `BrightTV_UserProfiles.csv` – User demographics (already provided)
- `brighttv_snowflake_setup.sql` – **One-click Snowflake script** (loads + cleans both tables automatically)

## How to Load Everything in Snowflake (Takes < 2 minutes)

1. Open **Snowsight** → Worksheets → New SQL Worksheet
2. Copy the entire content of `brighttv_snowflake_setup.sql`
3. Paste & run it
4. When you see the two lines with `@~` → a file-picker will pop up automatically  
   → Upload:
   - `BrightTV_UserProfiles.csv`
   - `BrightTV_Viewership.csv`
5. Press **Run All** again → Done!

Snowflake will:
- Create the database `BRIGHTTV_DB`
- Create and load the `users` table
- Load and clean the `viewership` table (UTC → SA time + duration in seconds)
- Show you instant results (top channels, hours by province, etc.)

## Tables Created
| Table        | Key Columns                                      | Notes                              |
|--------------|--------------------------------------------------|------------------------------------|
| `users`      | UserID, Name, Gender, Age, Province, etc.       | Ready for joins                    |
| `viewership` | UserID, Channel, RecordDate_SA, Duration_Sec    | Cleaned & SA time (+2h from UTC)   |

## Ready-to-Use Queries (already in the script)
- Top 10 channels by hours watched
- Total consumption by province, age, gender
- Daily & weekday trends
- Low-consumption days identification

## Next Steps for Your Presentation
- Connect Power BI / Tableau / Excel to `BRIGHTTV_DB.PUBLIC`
- Or just copy the query results into your slides
- All heavy lifting (time conversion, duration parsing, joins) is already done!

Enjoy your 20-minute presentation — you now have clean, fast, production-ready data in Snowflake!

Made with ❤️ for the BrightTV case study – Nov 2025
