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

After Fixing the ner, the result i get is

Entity       P        R        F1       TP    FP    FN   
PERSON       0.5000   0.5000   0.5000   1     1     1    
LOCATION     0.5000   0.5000   0.5000   1     1     1    
ORGANIZATION 1.0000   0.5000   0.6667   1     0     1    
Totals       0.6000   0.5000   0.5455   3     2     3 

This signifies that te fixes made are not significant enough to change the result

for the fandom wiki text, we get the following results

(PERSON)     P: 0.1143 R: 0.1116 F1: 0.1129 TP: 24 FP: 186 FN: 191
(LOCATION)   P: 0.1250 R: 0.1250 F1: 0.1250 TP: 6 FP: 42 FN: 42
(ORGANIZATION) P: 0.0238 R: 0.0270 F1: 0.0253 TP: 1 FP: 41 FN: 36

After fixing the ner result, i get this output:
(ORGANIZATION) P: 0.0238 R: 0.0270 F1: 0.0253 TP: 1 FP: 41 FN: 36
(PERSON)     P: 0.1143 R: 0.1116 F1: 0.1129 TP: 24 FP: 186 FN: 191
(LOCATION)   P: 0.1250 R: 0.1250 F1: 0.1250 TP: 6 FP: 42 FN: 42

The punctuation fix did not significantly change the NER results for PERSON, LOCATION, or ORGANIZATION entities in the fandom wiki dataset.
The precision, recall, and F1 scores remained nearly the same before and after the fix.
This suggests that punctuation wasn't a major issue in your original NER results for this dataset.

Steps:
Get data
Identify NER
Evaluate NER
get result
fix ner
check if that changes result

##USE OF AI
Used chat gpt to correct codes and summarise key observations using prompts like:
shorten these observations
getting this directory error
it does exist, but getting this when i try to move

