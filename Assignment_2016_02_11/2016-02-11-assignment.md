---
title: "Rclub homework"
author: "Liron"
output: html_document
runtime: shiny
---
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

``` {r}
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- rep( 1 , 20 )


likelihood <- dbinom( 3 , size=3 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )

```

2. WWWL

``` {r}
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- rep( 1 , 20 )


likelihood <- dbinom( 3 , size=4 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )

```

3. LWWLWWW

``` {r}
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- rep( 1 , 20 )


likelihood <- dbinom( 5 , size=7 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )

```


**2M2**

1. WWW

``` {r}
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- ifelse( p_grid < 0.5 , 0 , 1 )


likelihood <- dbinom( 3 , size=3 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )

```

2. WWWL

``` {r}
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- ifelse( p_grid < 0.5 , 0 , 1 )


likelihood <- dbinom( 3 , size=4 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )

```

3. LWWLWWW

``` {r}
p_grid <- seq( from=0 , to=1 , length.out=20 )


prior <- ifelse( p_grid < 0.5 , 0 , 1 )


likelihood <- dbinom( 5 , size=7 , prob=p_grid )


unstd.posterior <- likelihood * prior


posterior <- unstd.posterior / sum(unstd.posterior)

plot( p_grid , posterior , type="b" ,
      xlab="probability of water" , ylab="posterior probability" )
mtext( "20 points" )

```

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



