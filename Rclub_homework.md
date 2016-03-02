# Rclub homework
Liron  
**2E1** 
answer: 2  
**2E2** 
answer: 3  
**2E3** 
answer: 1  
**2E4** 
answer: It means that if you toss the globe 10 times, on approximatly 7 of these it will wall on water. By saying that "probability does not exist"he means that probability is just a way to describe reality, however, it is not reality itelf. I think that the "real" reality value requires an infinite number of tosses and sinse the subjective observer can never provide infinite values or data, than he can never describe reality as it really is.

**2M3**
answer: Pr(Earth|land) =   
(Pr(land|Earth) x Pr(Earth))/Pr(land) =   
(0.3 * 0.5)/0.65 = 0.23

**2M4**
answer:
Conditional on seeing black, # ways that a card could produce:  
white x white = 0  
white X black = 1  
black x black = 2  
Total ways to produce black = 3.   
Hence, probability to produce black x black = 2/3.  


**2M1**

1. WWW


```r
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- rep( 1 , 20 )


likelihood <- dbinom( 3 , size=3 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-1-1.png)

2. WWWL


```r
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- rep( 1 , 20 )


likelihood <- dbinom( 3 , size=4 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-2-1.png)

3. LWWLWWW


```r
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- rep( 1 , 20 )


likelihood <- dbinom( 5 , size=7 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-3-1.png)


**2M2**

1. WWW


```r
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- ifelse( p_grid < 0.5 , 0 , 1 )


likelihood <- dbinom( 3 , size=3 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-4-1.png)

2. WWWL


```r
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- ifelse( p_grid < 0.5 , 0 , 1 )


likelihood <- dbinom( 3 , size=4 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-5-1.png)

3. LWWLWWW


```r
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- ifelse( p_grid < 0.5 , 0 , 1 )


likelihood <- dbinom( 5 , size=7 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-6-1.png)

**2M5**
answer:Conditional on seeing black, # ways that a card could produce:  
white x white = 0  
white X black = 1  
black x black = 4 (2 cards)  
Total ways to produce black = 5.   
Hence, probability to produce black x black = 4/5.  

**2M6**

answer:Conditional on seeing black, # ways that a card could produce:  
white x white = 0   
white X black = 1  
black x black = 2   

probability to be pulled from the bag:  
white x white = 3  
white X black = 2  
black x black = 1  

probability to produce black x black:  
white x white = 0x3 = 0  
white X black = 1x2 = 2  
black x black = 2x1 = 2  

Total = 4. Hence, probability to produce black x black = 2/4 = 0.5.  

**2M7**

answer: 

probability of holding BxB conditional on seeing B:

p(BxB|B) = (1 x (1/3))/0.5 = 2/3 

cards left in the bag conditional on seeing B:

option 1: WxW and WxB ,probability 2/3  
option 2: WxW and BxB ,probability 1/3  

probability of holding BxB conditional on seeing W:

p(BxB|W) = ((3/4) x (2/3)) / (((3/4) x (2/3)) + ((2/4) x (1/3))) = 3/4

**2H1**

answer:    

Panda A probability of twins = 0.1    
Panda B probability of twins = 0.2  

probability of 2 successive twins births:  

Panda A = 0.1 x 0.1 = 0.01    
Panda B = 0.2 x 0.2 = 0.04    

species unknown = 0.15 x 0.15 =  0.0225  

**2H2**

answer:  

probability of panda A conditional on seeing twins:  

p(A|T) = (0.1 x 0.5) / 0.15 = 1/3  

**2H3**

Answer:  

probability of panda A conditional on seeing twins followed by singletone birth:    

p(A|S) = (0.9 x (1/3)) / 0.85 = 0.3529  

**2H4**

answer:    

probability of panda A positive:    

(0.8 + (1 - 0.65)) / 2 = 0.575  

probability of panda A coditional on A positive (AP) with no birth data:    

p(A|AP) = (0.8 * 0.5) / 0.575 = 0.69  

probability of panda A coditional on A positive (AP) with birth data:    

p(A|AP) = (0.8 * 0.3529) / 0.575 = 0.49   


```r
p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- rep( 1 , 1000 )
likelihood <- dbinom( 6 , size=9 , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
set.seed(100)
samples <- sample( p_grid , prob=posterior , size=1e4 , replace=TRUE )
```

**3E1**


```r
sum( samples < 0.2 ) / 1e4
```

```
## [1] 5e-04
```

**3E2**


```r
sum( samples > 0.8 ) / 1e4
```

```
## [1] 0.1117
```

**3E3**

```r
sum( samples > 0.2 & samples < 0.8 ) / 1e4
```

```
## [1] 0.8878
```

**3E4**


```r
quantile( samples , 0.2 )
```

```
##       20% 
## 0.5195195
```

**3E5**
 

```r
1 - (quantile( samples , 0.8 ))
```

```
##       80% 
## 0.2432432
```

**3E6**


```r
library(rethinking)
```

```
## Loading required package: rstan
```

```
## Warning: package 'rstan' was built under R version 3.2.3
```

```
## Loading required package: ggplot2
```

```
## Warning: package 'ggplot2' was built under R version 3.2.3
```

```
## rstan (Version 2.9.0-3, packaged: 2016-02-11 15:54:41 UTC, GitRev: 05c3d0058b6a)
```

```
## For execution on a local, multicore CPU with excess RAM we recommend calling
## rstan_options(auto_write = TRUE)
## options(mc.cores = parallel::detectCores())
```

```
## Loading required package: parallel
```

```
## rethinking (Version 1.58)
```

```r
HPDI( samples , prob=0.66 )
```

```
##     |0.66     0.66| 
## 0.5205205 0.7847848
```

**3E7**


```r
library(rethinking)
PI( samples , prob=0.66)
```

```
##       17%       83% 
## 0.5005005 0.7687688
```

**3M1**


```r
p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- rep( 1 , 1000 )
likelihood <- dbinom( 8 , size=15 , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-15-1.png)


**3M2**


```r
p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- rep( 1 , 1000 )
likelihood <- dbinom( 8 , size=15 , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
samples <- sample( p_grid , prob=posterior , size=1e4 , replace=TRUE )
plot( samples )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-16-1.png)

```r
library(rethinking)
dens( samples )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-16-2.png)

```r
HPDI( samples , prob=0.90 )
```

```
##      |0.9      0.9| 
## 0.3383383 0.7317317
```

**3M3**


```r
dummy_w <- rbinom( 1e5 , size=15 , prob=0.7 )
simplehist( dummy_w , xlab="dummy water count" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-17-1.png)

```r
dbinom( 8 , size=15 , prob=0.7 )
```

```
## [1] 0.08113003
```

**3M4**


```r
w <- rbinom( 1e5 , size=9 , prob=samples )
simplehist(w)
```

![](Rclub_homework_files/figure-html/unnamed-chunk-18-1.png)

```r
sum (w == 6) / 1e5
```

```
## [1] 0.17609
```

**3M5(3M1)**


```r
p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- ifelse( p_grid < 0.5 , 0 , 1 )
likelihood <- dbinom( 8 , size=15 , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-19-1.png)


**3M5(3M2)**


```r
p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- prior <- ifelse( p_grid < 0.5 , 0 , 1 )
likelihood <- dbinom( 8 , size=15 , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
samples <- sample( p_grid , prob=posterior , size=1e4 , replace=TRUE )
plot( samples )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-20-1.png)

```r
library(rethinking)
dens( samples )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-20-2.png)

```r
HPDI( samples , prob=0.90 )
```

```
##      |0.9      0.9| 
## 0.5005005 0.7147147
```

**3M5(3M3)**


```r
dummy_w <- rbinom( 1e5 , size=15 , prob=0.7 )
simplehist( dummy_w , xlab="dummy water count" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-21-1.png)

```r
dbinom( 8 , size=15 , prob=0.7 )
```

```
## [1] 0.08113003
```

**3M5(3M4)**


```r
w <- rbinom( 1e5 , size=9 , prob=samples )
simplehist(w)
```

![](Rclub_homework_files/figure-html/unnamed-chunk-22-1.png)

```r
sum (w == 6) / 1e5
```

```
## [1] 0.23333
```

**3H1**


```r
birth1 <- c(1,0,0,0,1,1,0,1,0,1,0,0,1,1,0,1,1,0,0,0,1,0,0,0,1,0,
0,0,0,1,1,1,0,1,0,1,1,1,0,1,0,1,1,0,1,0,0,1,1,0,1,0,0,0,0,0,0,0,
1,1,0,1,0,0,1,0,0,0,1,0,0,1,1,1,1,0,1,0,1,1,1,1,1,0,0,1,0,1,1,0,
1,0,1,1,1,0,1,1,1,1)
birth2 <- c(0,1,0,1,0,1,1,1,0,0,1,1,1,1,1,0,0,1,1,1,0,0,1,1,1,0,
1,1,1,0,1,1,1,0,1,0,0,1,1,1,1,0,0,1,0,1,1,1,1,1,1,1,1,1,1,1,1,1,
1,1,1,0,1,1,0,1,1,0,1,1,1,0,0,0,0,0,0,1,0,0,0,1,1,0,0,1,0,0,1,1,
0,0,0,1,1,1,0,0,0,0)

boys <- sum(birth1) + sum(birth2)

p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- rep( 1 , 1000 )
likelihood <- dbinom( boys , size=(length(birth1) + length(birth2)) , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
plot( p_grid , posterior , type="b" ,
      xlab="probability of boy" , ylab="posterior probability" )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-23-1.png)

I think that the parameter that maximizes the postirior probability is the size or number of observation.

**3H2**


```r
boys <- sum(birth1) + sum(birth2)

p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- rep( 1 , 1000 )
likelihood <- dbinom( boys , size=(length(birth1) + length(birth2)) , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
samples <- sample( p_grid , prob=posterior , size=1e4 , replace=TRUE )
plot( samples )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-24-1.png)

```r
library(rethinking)
dens( samples )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-24-2.png)

```r
HPDI( samples , prob=0.5 )
```

```
##      |0.5      0.5| 
## 0.5305305 0.5765766
```

```r
HPDI( samples , prob=0.89 )
```

```
##     |0.89     0.89| 
## 0.4964965 0.6076076
```

```r
HPDI( samples , prob=0.97 )
```

```
##     |0.97     0.97| 
## 0.4764765 0.6266266
```

**3H3**


```r
dummy_b <- rbinom( 1e4 , size=200 , prob=samples )
dens( dummy_b )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-25-1.png)

**3H4**


```r
p_grid <- seq( from=0 , to=1 , length.out=1000 ) 
prior <- rep( 1 , 1000 )
likelihood <- dbinom( sum(birth1) , size=(length(birth1)) , prob=p_grid )
posterior <- likelihood * prior
posterior <- posterior / sum(posterior)
samples <- sample( p_grid , prob=posterior , size=1e4 , replace=TRUE )
dummy_b1 <- rbinom( 1e4 , size=100 , prob=samples )
dens( dummy_b1 )
```

![](Rclub_homework_files/figure-html/unnamed-chunk-26-1.png)

Actual number of boys in birth1


```r
sum(birth1)
```

```
## [1] 51
```

