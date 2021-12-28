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


- ***Poverty Level (continuous)***
- `perfrl ~ 1 + SUBJECT + LEVEL + ln + lp + ls + cs_mn_avg_ol + lw + ave_sentiment + Average_Grade_Level`
- where lw: log ave number of words, ave_sentiment: average sentiment ofthe projects, Average_Grade_Level: readibility level (high means more difficult)
<p align="center">
<img src="/figures/reg4.png" width="800" title="hover text">
</p>
