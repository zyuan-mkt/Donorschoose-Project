# DonorsChoose Data

## Schools

It seems that Stanford data only report the public schools. However, since this dataset does not include kindergardens, there were 50,000 rows of "prek-2" observations dropped. Stanford report of the grade level is different to that of Donorschoose. Then we consider standardize the level: elementary, middle, and high.

There are 52316 schools in the original DonorsChoose dataset (with school id), and 89350 schools in the Stanford dataset. After merging these two, we have 40417 schools in common.

Math and RLA (Reading Language Arts) scores were standardized with mean -0.0458 and standard deviation 0.446. The difference in Math and RLA score was standardized
to -0.00507 and standard deviation 0.146. However, math and rla scores could hardly explain the number of posts by states.

## Projects 

### Description Table
|   | GRADE     | SUBJECT  | projects_0.0 | projects_1.0 | Classification    | price_0.0 | price_1.0 | students_0.0 | students_1.0 | projects_ratio | price_ratio | students_ratio |
|---|-----------|----------|--------------|--------------|--------------|-----------|-----------|--------------|--------------|----------------|-------------|----------------|
| 0 | PreK-2    | Language | 37869        | 264269       |   79.40%      | 542.94    | 503.54    | 38.94        | 39.37        | 6.98           | 0.93        | 1.01  
| 1 | PreK-2    | Science  | 20137        | 114351       |   80.13%   |601.05    | 539.14    | 48.51        | 45.92        | 5.68           | 0.9         | 0.95           ||
| 2 | PreK-2    | Others   | 24403        | 171853       |  77.10%      | 527.0     | 502.92    | 68.66        | 72.86        | 7.04           | 0.95        | 1.06           |
| 3 | Primary   | Language | 38200        | 261611       |   78.02%      | 580.22    | 542.18    | 84.36        | 79.84        | 6.85           | 0.93        | 0.95           |
| 4 | Primary   | Science  | 39155        | 212684       |  79.38%     |724.95    | 657.86    | 122.53       | 106.96       | 5.43           | 0.91        | 0.87           | 
| 5 | Primary   | Others   | 31426        | 201932       |     77.10%      |662.9     | 634.02    | 183.21       | 172.62       | 6.43           | 0.96        | 0.94           |
| 6 | Secondary | Language | 3954         | 43889        |    82.50%      |628.36    | 643.47    | 168.95       | 134.89       | 11.1           | 1.02        | 0.8            |
| 7 | Secondary | Science  | 6547         | 55449        |    79.10%      |1030.85   | 814.34    | 158.4        | 133.78       | 8.47           | 0.79        | 0.84           | 
| 8 | Secondary | Others   | 5589         | 65247        |    77.94%        |951.69    | 849.77    | 164.16       | 159.68       | 11.67          | 0.89        | 0.97           |

### Regressions
- ***Number of Projects***
- `ln ~ 1 + SUBJECT + LEVEL + perfrl + cs_mn_avg_ol`
- where ln: log number of projects, perfrl: free or reduced lunch ratio, cs_mn_avg_ol: average rla and math grades
<p align="center">
<img src="/figures/reg1.png" width="800" title="hover text">
</p>

- ***Price per Project***
- `lp ~ 1 + SUBJECT + LEVEL + perfrl + ls + cs_mn_avg_ol`
- where lp: log ave price of projects, ls: log ave number of students involved
<p align="center">
<img src="/figures/reg2.png" width="800" title="hover text">
</p>



- ***Number of Students per Project***
- `ls ~ 1 + SUBJECT + LEVEL + lp + perfrl + cs_mn_avg_ol`
<p align="center">
<img src="/figures/reg3.png" width="800" title="hover text">
</p>


- ***Price per Project***
- `perfrl ~ 1 + SUBJECT + LEVEL + ln + lp + ls + cs_mn_avg_ol + lw + ave_sentiment + Average_Grade_Level`
- where lw: log ave number of words, ave_sentiment: average sentiment ofthe projects, Average_Grade_Level: readibility level (high means more difficult)
<p align="center">
<img src="/figures/reg4.png" width="800" title="hover text">
</p>




