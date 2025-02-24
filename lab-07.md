Lab 07 - Conveying the right message through visualisation
================
Lilly McClendon
02-28-2025

### Load packages and data

``` r
library(tidyverse) 
```

### Exercise 1

``` r
df <- tribble(
  ~date, ~count, ~mask,
 "7/12/2020", 25.2, "mask", 
 "7/12/2020", 9.8, "no mask",
 "7/13/2020", 19.8, "mask",
 "7/13/2020", 9.0, "no mask", 
 "7/14/2020", 19.7, "mask", 
 "7/14/2020", 8.5, "no mask",
 "7/15/2020", 20.5, "mask",
 "7/15/2020", 9.8, "no mask", 
 "7/16/2020", 19.8, "mask", 
 "7/16/2020", 9.9, "no mask",
 "7/17/2020", 19.85, "mask",
 "7/17/2020", 9.5, "no mask", 
 "7/18/2020", 20.5, "mask", 
 "7/18/2020", 9.5, "no mask",
 "7/19/2020", 19.9, "mask",
 "7/19/2020", 9.0, "no mask", 
 "7/20/2020", 20.5, "mask", 
 "7/20/2020", 8.5, "no mask",
 "7/21/2020", 21.25, "mask",
 "7/21/2020", 8.5, "no mask", 
 "7/22/2020", 19.9, "mask", 
 "7/22/2020", 8.6, "no mask",
 "7/23/2020", 19.9, "mask",
 "7/23/2020", 8.3, "no mask", 
 "7/24/2020", 20.5, "mask", 
 "7/24/2020", 9.9, "no mask",
 "7/25/2020", 19.0, "mask",
 "7/25/2020", 9.95, "no mask", 
 "7/26/2020", 19.3, "mask", 
 "7/26/2020", 10.1, "no mask",
 "7/27/2020", 17.0, "mask",
 "7/27/2020", 9.5, "no mask",
 "7/28/2020", 16.2, "mask",
 "7/28/2020", 9.55, "no mask",
 "7/29/2020", 16.3, "mask",
 "7/29/2020", 9.6, "no mask",
 "7/30/2020", 16.5, "mask", 
 "7/30/2020", 10.0, "no mask",
 "7/31/2020", 16.0, "mask",
 "7/31/2020", 8.8, "no mask",
 "8/1/2020", 16.1, "mask",
 "8/1/2020", 9.0, "no mask",
 "8/2/2020", 15.8, "mask",
 "8/2/2020", 8.85, "no mask",
 "8/3/2020", 15.9, "mask",
 "8/3/2020", 9.3, "no mask",
)
```

### Exercise 2

``` r
library(ggplot2)
ggplot(df, aes(x = date, y = count, group = mask, color = mask)) +
  geom_line() + 
  labs(title = "New Visualization of Kansas Covid-19 Average of Daily Cases Per 100,000", subtitle = "Mask Mandate Counties vs. No Mask Mandate Counties", caption = "Source: Kansas Department of Health and Environment", x = "Date", y = "Average Daily Cases Per 100,000") + 
  scale_color_manual(values=c('darkblue', 'darkred')) +
  theme(axis.text.x = element_text(angle = 45, hjust = 1)) + 
  theme(plot.title = element_text(hjust=0.5))
```

![](lab-07_files/figure-gfm/kansas-data-new-visualization-1.png)<!-- -->
