#Title: Econmeterics B2000 Homework 1.

#Group members: Sun Wu Kim, Nene Oumou and Arifa Begum. 

#One surpise of the data that the average age of the Northeast was 1970 which means that the average age of this region is 54. That is much older than I expected. 

#Some questions I have about the data are what are the average incomes of the baby boomers generation or people born before 1965 or the average age people have bachelors degree or more? 

#In my experiment I rolled one die normally and got 3 sixes out of 20 times or 15 percent. The second die was wet and rolled on sandpaper to rig the roll to favor sixes but instead it gave me 2 sixes or 10 percent. 

getwd()

setwd("econb2000_letcure")

load("Household_Pulse_data_ph4c2.RData")
#glimpse(acs2017_ny) try this later
Household_Pulse_data[1:10,1:6]

attach(Household_Pulse_data)

summary(Household_Pulse_data)

summary(TBIRTH_YEAR[GENID_DESCRIBE == "female"])

summary(TBIRTH_YEAR[GENID_DESCRIBE == "male"])

summary(TBIRTH_YEAR[GENID_DESCRIBE == "transgender"])

summary(TBIRTH_YEAR[GENID_DESCRIBE == "other"])

summary(TBIRTH_YEAR[GENID_DESCRIBE == "NA"])

# here i want to find average ages of men and women
mean(TBIRTH_YEAR[GENID_DESCRIBE == "female"])

sd(TBIRTH_YEAR[GENID_DESCRIBE == "female"])

mean(TBIRTH_YEAR[GENID_DESCRIBE == "male"])

sd(TBIRTH_YEAR[GENID_DESCRIBE == "male"])

hist(TBIRTH_YEAR[(TBIRTH_YEAR < 1950)])

mean(TBIRTH_YEAR[ (GENID_DESCRIBE == "female") & (TBIRTH_YEAR > 1936) ]) 

summary(EEDUC)

library(tidyverse)

summary(EST_ST)

summary(INCOME)

Household_Pulse_data %>%
  group_by(EST_ST) %>%
  summarize(
    avg = mean(2024 - TBIRTH_YEAR),
    stdev = sd(2024 - TBIRTH_YEAR), 
    n_obs = n()
  ) 
  
  Household_Pulse_data %>%
  group_by(EST_ST) %>%
  summarize(
    age90th = quantile((2024 - TBIRTH_YEAR),probs = 0.9),
    age10th = quantile((2024 - TBIRTH_YEAR),probs = 0.1), 
    n_obs = n()
  ) %>%
  arrange(desc(age90th), .by_group = TRUE)
  
  table(EEDUC,GENID_DESCRIBE)
  
  xtabs(~EEDUC + GENID_DESCRIBE)
  
  prop.table(table(EEDUC,GENID_DESCRIBE))
  
  mean(TBIRTH_YEAR[(REGION == "Northeast")])
  
  # alternatively
restrict1 <- as.logical((REGION == "Northeast"))
dat_northeast <- subset(Household_Pulse_data, restrict1)

detach()
attach(dat_northeast)

mean(TBIRTH_YEAR)
