## Stanford Data

### The Academic Performance of Rich and Poor Schools

It seems that Stanford data only report the public schools.

There are 52316 schools in the original DonorsChoose dataset (with school id), and 89350 schools in the Stanford dataset. After merging these two, we have 40417 schools in common.

Math and RLA (Reading Language Arts) scores were standardized with mean -0.0458 and standard deviation 0.446. The difference in Math and RLA score was standardized
to -0.00507 and standard deviation 0.146. However, math and rla scores could hardly explain the number of posts by states.
- ***Math and RLA Scores Across States***
<p align="center">
  <img src="/figures/state_scores.png" width="450" title="hover text">
</p>

- ***Math and RLA Difference Across States***
<p align="center">
  <img src="/figures/state_difference.png" width="450" title="hover text">
</p>


- ***Math and RLA Scores of High Poverty versus Low Poverty***
<p align="center">
  <img src="/figures/high_poverty.png" width="450" title="hover text">
  <img src="/figures/low_poverty.png" width="450" alt="accessibility text">
</p>

- ***Difference between Math and RLA of High Poverty and Low Poverty***
<p align="center">
  <img src="/figures/high_poverty_difference.png" width="450" title="hover text">
  <img src="/figures/low_poverty_difference.png" width="450" alt="accessibility text">
</p>

- ***Difference in Math and RLA between High Poverty and Low Poverty***
<p align="center">
  <img src="/figures/difference.png" width="450" title="hover text">
</p>

## DonorsChoose Data

### Word Clouds of Rich Schools versus Poor Schools

***Overall: Test Loss: 0.469 | Test Acc: 80.00%***
![](./figures/pov.png)

***Pre-Covid: Test Loss: 0.486 | Test Acc: 79.29%***
![](./figures/precovid.png)

***Post-Covid: Test Loss: 0.540 | Test Acc: 71.42%***
![](./figures/postcovid.png)

***Entertainment: Test Loss: 0.470 | Test Acc: 78.75%***
![](./figures/ent.png)


***Technology: Test Loss: 0.496 | Test Acc: 77.94%***
![](./figures/tech.png)


***Supplies: Test Loss: 0.471 | Test Acc: 77.94%***
![](./figures/sup.png)


***Visits: Test Loss: 0.460 | Test Acc: 77.75%***
![](./figures/vis.png)


***Arts: Test Loss: 0.498 | Test Acc: 77.98%***
![](./figures/art.png)


***PreK - 2: Test Loss: 0.453 | Test Acc: 81.35%***
![](./figures/prek-2.png)


***Grade 3 - 5: Test Loss: 0.558 | Test Acc: 71.33%***
![](./figures/3-5.png)


***Grade 6 - 8: Test Loss: 0.598 | Test Acc: 67.77%***
![](./figures/6-8.png)


***Grade 9 - 12: Test Loss: 0.516 | Test Acc: 76.77%***
![](./figures/9-12.png)

***Male: Test Loss: 0.363 | Test Acc: 85.21%***
![](./figures/male.png)

***Female: Test Loss: 0.468 | Test Acc: 81.58%***
![](./figures/female.png)


### Next I collected the projects related to math and literacy from grade 3 - 8 in the five states respectively with highest and lowest scores. I found that the algorithm is better at predicting rich and poor in high-score states

***Low RLA: Test Loss: 0.544 | Test Acc: 72.97%***
![](./figures/low_rla.png)

***High RLA: Test Loss: 0.485 | Test Acc: 76.59%***
![](./figures/high_rla.png)

***Low Math: Test Loss: 0.492 | Test Acc: 74.53%***
![](./figures/low_math.png)

***High Math: Test Loss: 0.419 | Test Acc: 81.57%***
![](./figures/high_math.png)


### Difference in Difference 

```DID = (math_{rich}-math_{poor}) - (rla_{rich}-rla_{poor})```


***Big Difference RLA: Test Loss: 0.422 | Test Acc: 80.43%***
![](./figures/small_diff_rla.png)

***Big Difference RLA: Test Loss: 0.471 | Test Acc: 77.67%***
![](./figures/small_diff_math.png)

***Small Difference Math: Test Loss: 0.362 | Test Acc: 85.29%***
![](./figures/big_diff_rla.png)

***Big Difference Math: Test Loss: 0.464 | Test Acc: 78.76%***
![](./figures/big_diff_math.png)





