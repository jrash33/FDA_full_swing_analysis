# FDA_full_swing_analysis

- In data folder: Swing data files (each file is 1 swing) each consisting of global XYZ position for all 141 markers (real/virtual)

- Code:
1. Read in data
2. Delete bad swings not able to be properly captured
3. Chop off all data past impact
4. Spline fit all missing values
5. Separate data by player and club used
6. Grab each individual marker position data
------------------------------------------------------
7. Choose parameter of interest:
- Rotational speed variables about the body coordinate system
- Swing direction variables
- MOI Engagement variables
- Shaft Deflection Variables
- Shaft Speed Variables
- Speed/Acceleration Variables of any marker

8. Run FDA analysis function
- Interpolate variable of interest right at impact using simple polyfit function and add to matrix of each player
- Sort swings into clubs of interest (function takes in clubs you want to compare in case there are more than 2 clubs)
- Format data properly by combining all swings of interest into 1 matrix
- Register Swings at impact
- Clean data by using quantile and acceleration filter
- Fit swings using FDA parameters specified in code
- Run statistical analysis function on final data set

9. Analyze each player
- Final result is image with 4 plots
- Plot 1: Full swing overlook to see how clean the data was for each swing during swing sequence
- Plot 2: P-Value at each point in swing sequence
- Plot 3: Difference values of each club during swing
- Plot 4: snap shot of impact and values of parameter for each club at impact
