# nfl_project

- Author: Rodolfo Elenes
- Email contact: rodolfoe7157@gmail.com
- LinkedIn: www.linkedin.com/in/rodolfo-elenes-083311223

Hello user! I am conducting a case study on NFL Runningback players. They are known the be the most injury prone players in the sport. 
I want to find what factors contribute to the player's injuries such as usage, age, experience in the league, etc.
I want to ultimately be able to create an ML model to predict possible injuries from the upcoming players in the 2025 NFL season!

# LinkedIn Blog Posts:
- [8/27/25](https://www.linkedin.com/pulse/nflproject-blog-post-82725-rodolfo-elenes-9lxfc/?trackingId=GNbPQPNQF%2F7UJGbvhQxnwA%3D%3D)
- [9/25/25](https://www.linkedin.com/pulse/nflproject-blog-spot-92525-rodolfo-elenes-ju2qc/?trackingId=FG9gOrpb%2FHS4OhH2airSig%3D%3D)
- [12/2/2025 Post](https://www.linkedin.com/pulse/nflproject-blog-post-12225-rodolfo-elenes-5kruc/?trackingId=h%2FDxxmlbQtOk5ShsPn6RfQ%3D%3D)

# How I am making this project
I am currently developing this under jupyter notebook. I am currently planning to use only Python and python packages like pandas.
I am going to stick with saving the tables as csv files to allow easier reproducibility. I am using duckdb python package to implement SQL!
I am using github for version controlling and my linkedin to communicate significant updates!

# Constraints
- Player has to miss 4 or more weeks in a row for it to be "significant"
  - Small tweaks and rest days should not be accounted for
- Player has to be listed as a runningback (i.e. no Taysom Hill)
  - No fullbacks
- Regular season and playoffs game will be included in the data
- Players need to have at least 100 rushing attempts in their career
  - This number was decided on the collection of all available RB players gamelogs that have played since 1990 and filtered out the guys with less than 100 rushing attempts. I then took the 33rd percentile of the distribution of the data to come up with this rushing attempt number.

# Known flaws
- When updating players_ref.csv gm_log_rtrvd column from create_player_gmlogs notebook, the value will be updated to 1 at the end of **each individual player run** and not **notebook run** as pandas save to csv does not support the option to update individual rows. This way is more computationally expensive but it allows easier maintainability in case of an error
- Under gamelogs, I am not including Kick or Punt Returns yards, but itll be represented through special teams snap count. This is to reduce complexity
  - Players like Cordarrelle Patterson will be affected by this decision
- There will be various players who will have inferred INJ rows, but those rows were not from injuries but due to legal issues, waived by team, etc.

# Known skills I applied
- Python skills
- Pandas python package skills
- SQL queries skills
- Feature engineering skills

# Lessons Learned
- I have learned how to scrape data from websites
- I have been learning how to utility github (I come from Azure DevOps background)
- I have learned how to manage raw data
- I learned how to independently create my first ML model via XGBoost while applying background knowledge of ML topics

# Results
[ML Table CSV](tables/ml_predictions.csv)
