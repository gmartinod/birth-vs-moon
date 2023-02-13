# birth-vs-moon

It is a commun saying that there is more women giving birth on full moon days. Even if I am surely not the first questionning this belief, I am using this context to generate some visualizations and apply statistical tests on data. 

## Data

After quick research, no database counting  number of births by day is available for France. Hopefully Governement of Belgium is giving access to thier numbers on https://statbel.fgov.be/fr/open-data/nombre-de-naissances-par-jour . The data is available from 1992 to 2021. Though, we are focussing on the 2010th.

I have build a CSV file with key dates of moon cycles of 2019 (moon2019.txt) : 1 is full moon, 0.5 is half (first or third quarter) moon, 0 represent new moon. I am running the statistical tests only on year 2019. 

## Development

### Smoothing data
It happen that the data is quite noisy, showing regular drops and masking the year-wise evolution. This phenomenon can be explain (see fig 1) by the organisationnal changes in the hospitals during week-ends and public holidays, as shorten staff for induced labors. 

To try to get pass these drops, we apply a 1D gaussian filter (or Moving Average) on our data. To show consistency over the years, fig 2 plot the tendancy of smoothed data over 4 years (excluding lead years). The number of births keep evolving in the same proportions.

TODO : Evaluate correlation between years

### Add the full moon parameter in the loop
Considering the impact of the full moon period on childbirth, we want to get a visual idea of it. Fig 3 shows every period of full moon on the plot of 2019 data. I enlarged the line to consider the fullmoon period as 3 consecutif days 




