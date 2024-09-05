getwd()

setwd("econb2000_letcure")

load("Household_Pulse_data_ph4c2.RData")
#glimpse(acs2017_ny) try this later
Household_Pulse_data[1:10,1:6]

  TBIRTH_YEAR    RHISPANIC RRACE     EEDUC        MS
1         1976 Not Hispanic Black  bach deg separated
2         1961 Not Hispanic White assoc deg  divorced
3         1988 Not Hispanic White   adv deg   married
4         1956 Not Hispanic White assoc deg   married
5         1970 Not Hispanic White  bach deg   married
6         1984 Not Hispanic White   adv deg   married
7         1968     Hispanic White some coll  divorced
8         1967 Not Hispanic White   adv deg   married
9         1972 Not Hispanic White some coll   married
10        1956 Not Hispanic White  bach deg   married
   EGENID_BIRTH
1        female
2        female
3        female
4          male
5          male
6        female
7          male
8          male
9        female
10         male

attach(Household_Pulse_data)

summary(Household_Pulse_data)

  TBIRTH_YEAR          RHISPANIC       RRACE      
 Min.   :1936   Not Hispanic:64658   White:57562  
 1st Qu.:1957   Hispanic    : 6494   Black: 6345  
 Median :1969                        Asian: 3379  
 Mean   :1970                        Other: 3866  
 3rd Qu.:1983                                     
 Max.   :2006 


EEDUC               MS        EGENID_BIRTH  
 less than hs:  585   NA       :  477   male  :31510  
 some hs     : 1282   married  :39339   female:39642  
 HS diploma  :10094   widowed  : 4551                 
 some coll   :15415   divorced :11585                 
 assoc deg   : 7614   separated: 1300                 
 bach deg    :19137   never    :13900                 
 adv deg     :17025                                   
     GENID_DESCRIBE       SEXUAL_ORIENTATION
 NA         :36702   NA            :  969   
 male       :15089   gay or lesbian: 2386   
 female     :18830   straight      :62989   
 transgender:  147   bisexual      : 2756   
 other      :  384   something else: 1177   
                     dont know     :  875   
                                            
                      KIDS_LT5Y    
 NA                        :63953  
 Yes children under 5 in HH: 7199  
                                   
                                   
                                   
                                   
                                   
                     KIDS_5_11Y   
 NA                       :60784  
 Yes children 5 - 11 in HH:10368  
                                  
                                  
                                  
                                  
                                  
                     KIDS_12_17Y   
 NA                        :60641  
 Yes children 12 - 17 in HH:10511  
                                   
                                   
                                   
                                   
                                   
                              ENROLLNONE   
 NA                                :66789  
 children not in any type of school: 4363  
                                           
                                           
                                           
                                           
                                           
                  WRKLOSSRV    
 NA                    : 1558  
 yes recent HH job loss: 6685  
 no recent HH job loss :62909  
                               
                               
                               
                               
                          ANYWORK     
 NA                           : 1819  
 yes employment in last 7 days:41672  
 no employment in last 7 days :27661  
                                      
                                      
                                      
                                      
                KINDWORK    
 NA                 :30263  
 work for govt      : 6654  
 work for private co:23400  
 work for nonprofit : 5025  
 self employed      : 5011  
 work in family biz :  799  
                            
                                          RSNNOWRKRV   
 NA                                            :44596  
 concerned about spreading                     :16005  
 caring for elderly                            : 3830  
 employer closed because covid                 : 2835  
 sick or disabled                              : 1022  
 am/was sick w covid or caring for sick w covid: 1021  
 (Other)                                       : 1843  
                                TWDAYS     
 NA                                : 2550  
 had 1-2 telework days in past week: 6797  
 had 3-4 telework days in past week: 4617  
 had 5+ telework days in past week :11121  
 had no telework days in past week :46067  
                                           
                                           
                                            ANXIOUS     
 NA                                             : 5480  
 no anxiety over past 2 wks                     :37174  
 several days anxiety over past 2 wks           :19618  
 more than half the days anxiety over past 2 wks: 4329  
 nearly every day anxiety                       : 4551  
                                                        
                                                        
                                             WORRY      
 NA                                             : 5580  
 no worry over past 2 wks                       :43087  
 several days worried over past 2 wks           :15509  
 more than half the days worried over past 2 wks: 3386  
 nearly every day worry                         : 3590  
                                                        
                                                        
                                                 INTEREST    
 NA                                                  : 5566  
 no days in past 2 wks with little interest in things:45234  
 several days over past 2 wks                        :14309  
 more than half the days over past 2 wks             : 3240  
 nearly every day                                    : 2803  
                                                             
                                                             
                                      DOWN      
 NA                                     : 5600  
 no days in past 2 wks feeling depressed:44300  
 several days over past 2 wks           :15438  
 more than half the days over past 2 wks: 2965  
 nearly every day                       : 2849  
                                                
                                                
                                     MHLTH_NEED   
 NA                                       :51723  
 all children need mental health treatment: 1324  
 some but not all children                : 2266  
 no, none of the children                 :15839  
                                                  
                                                  
                                                  
                                                  MHLTH_GET    
 NA                                                    :67609  
 all children get the mental health treatment they need: 2743  
 some but not all children                             :  347  
 no, none of the children                              :  453  
                                                               
                                                               
                                                               
                                                 MHLTH_SATISFD  
 NA                                                     :68076  
 satisfied with all the mental health treatment they get: 2061  
 some but not all                                       :  816  
 no, none                                               :  199  
                                                                
                                                                
                                                                
                                           MHLTH_DIFFCLT  
 NA                                               :67608  
 not difficult to get kids mental health treatment: 1244  
 somewhat difficult                               : 1332  
 very difficult                                   :  719  
 unable to get treatment due to difficulty        :  186  
 did not try to get                               :   63  
                                                          
                                SOCIAL1     
 NA                                 : 6563  
 always get social emotional support:19032  
 usually                            :23055  
 sometimes                          :12604  
 rarely                             : 5844  
 never                              : 4054  
                                            
          SOCIAL2     
 NA           : 6518  
 always lonely: 2381  
 usually      : 4847  
 sometimes    :17999  
 rarely       :23362  
 never        :16045  
                      
                                                         SUPPORT1    
 NA                                                          : 6579  
 talk on phone w family friends neighbors less than once week:11831  
 1 or 2 per week                                             :18093  
 3 or 4 per week                                             :14001  
 5 + per week                                                :20648  
                                                                     
                                                                     
                                                 SUPPORT2    
 NA                                                  : 6638  
 get together w friends or family less than once week:25546  
 1 or 2 per week                                     :25665  
 3 or 4 per week                                     : 8552  
 5 + per week                                        : 4751  
                                                             
                                                             
                                                              SUPPORT3    
 NA                                                               : 6703  
 attend church or religious ceremony never or less than 1 per year:35992  
 1 to 3 per year                                                  : 8433  
 4 to 11 per year                                                 : 3948  
 12+ times per year                                               :16076  
                                                                          
                                                                          
                                     SUPPORT4    
 NA                                      : 7353  
 attend clubs or orgs less than once week:50214  
 1 or 2 per week                         :10676  
 3 or 4 per week                         : 2909  
                                                 
                                                 
                                                 
                                                             SUPPORT1EXP   
 NA                                                                :11402  
 text on phone w friends or family or neighbors less than once week: 7990  
 1 or 2 per week                                                   :10780  
 3 or 4 per week                                                   :40980  
 5 + per week                                                      :    0  
                                                                           
                                                                           
                          CURFOODSUF   
 NA                            : 8111  
 had enough food               :42018  
 had enough but not what wanted:16391  
 sometimes not enough food     : 3442  
 often not enough food         : 1190  
                                       
                                       
                                               CHILDFOOD    
 NA                                                 :63887  
 often kids not eating enough because couldnt afford:  370  
 sometimes kids not eating enough                   : 1425  
 kids got enough food                               : 5470  
                                                            
                                                            
                                                            
                            PRICESTRESS   
 NA                               :21815  
 very stressed about price changes:18189  
 Moderate stress price changes    :13888  
 a little stress price changes    :13278  
 no stress                        : 3982  
                                          
                                          
                           TENURE     
 NA                           : 9149  
 housing owned free and clear :15998  
 housing owned with mortgage  :29700  
 housing rented               :15439  
 housing occupied without rent:  866  
                                      
                                      
                                LIVQTRRV    
 live in detached 1 family          :41925  
 NA                                 : 9749  
 live in bldg w 5+ apts             : 8145  
 live in 1 family attached to others: 4758  
 live in mobile home                : 2637  
 live in building with 3-4 apts     : 2115  
 (Other)                            : 1823  
            RENTCUR                     MORTCUR     
 NA             :55782   NA                 :41545  
 current on rent:13906   current on mortgage:28370  
 behind on rent : 1464   behind on mortgage : 1237  
                                                    
                                                    
                                                    
                                                    
                                        EVICT      
 NA                                        :69734  
 very likely evicted in next 2 months      :  190  
 somewhat likely evicted in next 2 months  :  354  
 not very likely evicted in next 2 months  :  394  
 not at all likely evicted in next 2 months:  480  
                                                   
                                                   
                                       FORCLOSE    
 NA                                        :69931  
 very likely forclosed in next 2 months    :   52  
 somewhat likely forclosed in next 2 months:  182  
 not very likely forclosed in next 2 months:  452  
 not at all forclosed in next 2 months     :  535  
                                                   
                                                   
               RECVDVACC    
 NA                 :10284  
 yes got vaxx       :52519  
 no did not get vaxx: 8349  
                            
                            
                            
                            
                              HADCOVIDRV   
 NA                                :10717  
 yes tested + or doc told had Covid:36478  
 no                                :23957  
                                           
                                           
                                           
                                           
                               LONGCOVID    
 NA                                 :36298  
 had symptoms 3mo or more Long Covid: 9685  
 no                                 :25169  
                                            
                                            
                                            
                                            
                                    SYMPTOMS    
 NA                                     :34850  
 had no covid symptoms although tested +: 1350  
 had mild Covid symptoms                :13155  
 had moderate Covid symptoms            :16783  
 had severe Covid symptoms              : 5014  
                                                
                                                
                      INCOME             EST_ST     
 NA                      :12256   California: 5215  
 HH income $100k - 149   :10444   Texas     : 3456  
 HH income $50k - 74.9   : 9461   Washington: 2892  
 HH income $75 - 99.9    : 7844   Florida   : 2613  
 HH income $200k +       : 7480   Michigan  : 2033  
 HH income less than $25k: 6782   Arizona   : 2018  
 (Other)                 :16885   (Other)   :52925  
                   PRIVHLTH    
 has private health ins:45139  
 no private health ins :12251  
 NA                    :13762  
                               
                               
                               
                               
                  PUBHLTH            REGION     
 has public health ins:24916   Northeast:10731  
 no public health ins :30126   South    :23680  
 NA                   :16110   Midwest  :15071  
                               West     :21670  
                                                
                                                
                                                
 Num_kids_Pub_School Num_kids_Priv_School
 Min.   :0.0         Min.   :0.00        
 1st Qu.:1.0         1st Qu.:1.00        
 Median :2.0         Median :1.00        
 Mean   :1.7         Mean   :1.26        
 3rd Qu.:2.0         3rd Qu.:2.00        
 Max.   :4.0         Max.   :2.00        
 NA's   :58066       NA's   :69107       
 Num_kids_homeschool
 Min.   :0.00       
 1st Qu.:1.00       
 Median :1.00       
 Mean   :1.22       
 3rd Qu.:2.00       
 Max.   :2.00       
 NA's   :70079
 
summary(TBIRTH_YEAR[GENID_DESCRIBE == "female"])
 Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   1936    1957    1970    1970    1983    2006 
summary(TBIRTH_YEAR[GENID_DESCRIBE == "male"])
 Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   1936    1956    1969    1970    1983    2006 
summary(TBIRTH_YEAR[GENID_DESCRIBE == "transgender"])
 Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   1936    1983    1992    1988    1998    2006 
summary(TBIRTH_YEAR[GENID_DESCRIBE == "other"])
Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   1936    1962    1978    1976    1990    2006 
summary(TBIRTH_YEAR[GENID_DESCRIBE == "NA"])
Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   1936    1956    1969    1970    1983    2006 
# here i want to find average ages of men and women
mean(TBIRTH_YEAR[GENID_DESCRIBE == "female"])
[1] 1970.346
sd(TBIRTH_YEAR[GENID_DESCRIBE == "female"])
[1] 15.56546
mean(TBIRTH_YEAR[GENID_DESCRIBE == "male"])
[1] 1969.691
sd(TBIRTH_YEAR[GENID_DESCRIBE == "male"])
16.09923
hist(TBIRTH_YEAR[(TBIRTH_YEAR < 1950)])

mean(TBIRTH_YEAR[ (GENID_DESCRIBE == "female") & (TBIRTH_YEAR > 1936) ]) 
[1] 1970.493
summary(EEDUC)
less than hs      some hs   HS diploma    some coll 
         585         1282        10094        15415 
   assoc deg     bach deg      adv deg 
        7614        19137        17025 
library(tidyverse)

summary(EST_ST)
 Alabama               Alaska 
                1074                  825 
             Arizona             Arkansas 
                2018                  932 
          California             Colorado 
                5215                 1860 
         Connecticut             Delaware 
                1237                  693 
District of Columbia              Florida 
                 757                 2613 
             Georgia               Hawaii 
                1957                  764 
               Idaho             Illinois 
                1099                 1625 
             Indiana                 Iowa 
                1387                 1204 
              Kansas             Kentucky 
                1166                 1107 
           Louisiana                Maine 
                1021                  759 
            Maryland        Massachusetts 
                1634                 1892 
            Michigan            Minnesota 
                2033                 1461 
         Mississippi             Missouri 
                 781                 1350 
             Montana             Nebraska 
                 680                  896 
              Nevada        New Hampshire 
                1001                  981 
          New Jersey           New Mexico 
                1287                 1340 
            New York       North Carolina 
                1381                 1410 
        North Dakota                 Ohio 
                 474                 1287 
            Oklahoma               Oregon 
                1195                 1880 
        Pennsylvania         Rhode Island 
                1906                  691 
      South Carolina         South Dakota 
                1170                  752 
           Tennessee                Texas 
                1385                 3456 
                Utah              Vermont 
                1551                  597 
            Virginia           Washington 
                1896                 2892 
       West Virginia            Wisconsin 
                 599                 1436 
             Wyoming 
                 545 
summary(INCOME)
 NA HH income less than $25k 
                   12256                     6782 
 HH income $25k - $34.9k    HH income $35k - 49.9 
                    5156                     6192 
   HH income $50k - 74.9     HH income $75 - 99.9 
                    9461                     7844 
   HH income $100k - 149     HH income $150 - 199 
                   10444                     5537 
       HH income $200k + 
                    7480 
Household_Pulse_data %>%
  group_by(EST_ST) %>%
  summarize(
    avg = mean(2024 - TBIRTH_YEAR),
    stdev = sd(2024 - TBIRTH_YEAR), 
    n_obs = n()
  ) 
  
EST_ST                 avg stdev n_obs
   <fct>                <dbl> <dbl> <int>
 1 Alabama               55.1  16.1  1074
 2 Alaska                53.7  15.6   825
 3 Arizona               56.6  16.0  2018
 4 Arkansas              54.2  16.2   932
 5 California            53.9  15.8  5215
 6 Colorado              53.2  16.1  1860
 7 Connecticut           54.4  15.9  1237
 8 Delaware              57.2  15.8   693
 9 District of Columbia  45.3  14.3   757
10 Florida               57.2  16.1  2613
# ℹ 41 more rows
# ℹ Use `print(n = ...)` to see more rows


  Household_Pulse_data %>%
  group_by(EST_ST) %>%
  summarize(
    age90th = quantile((2024 - TBIRTH_YEAR),probs = 0.9),
    age10th = quantile((2024 - TBIRTH_YEAR),probs = 0.1), 
    n_obs = n()
  ) %>%
  arrange(desc(age90th), .by_group = TRUE)

EST_ST        age90th age10th n_obs
   <fct>           <dbl>   <dbl> <int>
 1 Arizona          77      34    2018
 2 Florida          77      34    2613
 3 Hawaii           77      37.3   764
 4 New Mexico       77      35    1340
 5 Delaware         76      35     693
 6 Idaho            76      34    1099
 7 Nevada           76      34    1001
 8 New Hampshire    76      35     981
 9 West Virginia    76      34     599
10 Arkansas         75.9    32     932
# ℹ 41 more rows
# ℹ Use `print(n = ...)` to see more rows
  
  table(EEDUC,GENID_DESCRIBE)
  
GENID_DESCRIBE
EEDUC            NA male female transgender other
  less than hs  342   98    134           3     8
  some hs       713  233    319           3    14
  HS diploma   5279 1929   2818          15    53
  some coll    7877 3200   4204          41    93
  assoc deg    3987 1373   2200           8    46
  bach deg     9842 4432   4721          49    93
  adv deg      8662 3824   4434          28    77
  
xtabs(~EEDUC + GENID_DESCRIBE)

GENID_DESCRIBE
EEDUC            NA male female transgender other
  less than hs  342   98    134           3     8
  some hs       713  233    319           3    14
  HS diploma   5279 1929   2818          15    53
  some coll    7877 3200   4204          41    93
  assoc deg    3987 1373   2200           8    46
  bach deg     9842 4432   4721          49    93
  adv deg      8662 3824   4434          28    77  

  prop.table(table(EEDUC,GENID_DESCRIBE))

GENID_DESCRIBE
EEDUC                    NA         male       female
  less than hs 4.806611e-03 1.377333e-03 1.883292e-03
  some hs      1.002080e-02 3.274680e-03 4.483360e-03
  HS diploma   7.419328e-02 2.711097e-02 3.960535e-02
  some coll    1.107067e-01 4.497414e-02 5.908478e-02
  assoc deg    5.603497e-02 1.929672e-02 3.091972e-02
  bach deg     1.383236e-01 6.228918e-02 6.635091e-02
  adv deg      1.217394e-01 5.374410e-02 6.231729e-02
              GENID_DESCRIBE
EEDUC           transgender        other
  less than hs 4.216326e-05 1.124353e-04
  some hs      4.216326e-05 1.967619e-04
  HS diploma   2.108163e-04 7.448842e-04
  some coll    5.762312e-04 1.307061e-03
  assoc deg    1.124353e-04 6.465033e-04
  bach deg     6.886665e-04 1.307061e-03
  adv deg      3.935237e-04 1.082190e-03 
 
  mean(TBIRTH_YEAR[(REGION == "Northeast")])
[1] 1970.11  
  # alternatively
restrict1 <- as.logical((REGION == "Northeast"))
dat_northeast <- subset(Household_Pulse_data, restrict1)

detach()
attach(dat_northeast)

mean(TBIRTH_YEAR)

[1] 1970.11 
