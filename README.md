# Amex-Hackathon
 
## Background
- American Express has a Merchant Recommender to help connect an Amex Credit Card Customer with an Amex Merchant (Shop that accepts Amex cards)
- This capability recommends (show on a marketing channel) personalized merchants to Customers, to help Customers discover merchants near to them to shop &
increase spend on merchants. These recommended merchants are decided by an algorithm.
- A Customer transacting on a recommended merchant within 30 days of recommendation date is tagged as a successful activatiom
- However, a Customer could have transacted with merchants even though it was not recommended by Amex (organic activations). Think about all the shops you Visit
without these shops being marketed to you.

## Problem Statement:
The goal is to find merchants for each customer that have maximum 'Incremental activations' (and hence minimum organic activations). Incremental Activations means
activations on merchants that the Customer would not have discovered otherwise, unless recommended.

## Evaluation Criteria:
- Some merchants are randomly Recommended & Not-Recommended at the Customer level.
- The goal is to maximize Incremental Activation Rate on Top 10 merchants by prediction for each Customer (collated at a dataset level).
- Incremental Activation rate = Recommended Activation Rate minus Not-Recommended Activation Rate
- Activation rate = No. of Activations/No. of Recommendations, at Customer x Merchant level

## Expected Outcome:
For each Customer x Merchant combination in Round 1 submission data, calculate a score such that Incremental Activation Rate on Top 10 merchants by prediction for
each Customer (collated at a dataset level) is maximized. The final output file to be uploaded should have 3 columns — Customer, Merchant & predicted_score.