# Assessed-Task 1
I have downloaded the following text from Wikipedia and stored it in wikipedia.txt

I run it through Stanford NER, and get the marked up text in stanford-wikipedia.txt:

Thomas Cruise Mapother IV (born July 3, 1962) is an American actor and producer. Regarded as a Hollywood icon,[1][2][3] he has received various accolades, including an Honorary Palme d'Or and three Golden Globe Awards, in addition to nominations for four Academy Awards. His films have grossed over $5 billion in North America and over $12......

My list of NERs from that text starts with:

Thomas (PERSON)
Cruise (PERSON)
Mapother (PERSON)
Hollywood (LOCATION)
North (LOCATION)
America (LOCATION)
Ron (PERSON)
Kovic (PERSON)
Hollywood (LOCATION)
Jerry (PERSON) ...


The beginning of the gold standard file wikipedia-gold.txt that I create looks as follows:

Thomas (PERSON)
Cruise (PERSON)
Mapother (PERSON)
Hollywood (ORGANIZATION)
North America (LOCATION)
Ron (PERSON)
Kovic (PERSON)
Hollywood (ORGANIZATION)
Jerry (PERSON)
Maguire (PERSON)

When I run my eval script on this, I get
Entity       P        R        F1       TP    FP    FN   
PERSON       0.5000   0.5000   0.5000   1     1     1    
LOCATION     0.5000   0.5000   0.5000   1     1     1    
ORGANIZATION 1.0000   0.5000   0.6667   1     0     1    
Totals       0.6000   0.5000   0.5455   3     2     3 

