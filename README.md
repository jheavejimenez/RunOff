# RunOff
### A program that runs a runoff election

# Background
A ranked-choice voting system. In a ranked-choice system, voters can vote for more than one candidate. Instead of just voting for their top choice, they can rank the candidates in order of preference.
Aranked choice voting system is the instant runoff system. In an instant runoff election, voters can rank as many candidates as they wish. If any candidate has a majority (more than 50%) of the first preference votes, that candidate is declared the winner of the election.

If no candidate has more than 50% of the vote, then an “instant runoff” occurrs. The candidate who received the fewest number of votes is eliminated from the election, and anyone who originally chose that candidate as their first preference now has their second preference considered. Why do it this way? Effectively, this simulates what would have happened if the least popular candidate had not been in the election to begin with.

The process repeats: if no candidate has a majority of the votes, the last place candidate is eliminated, and anyone who voted for them will instead vote for their next preference (who hasn’t themselves already been eliminated). Once a candidate has a majority, that candidate is declared the winner.

# Usage
```
$ ./runoff Elon Bill Jeff
Number of voters: 5
Rank 1: Elon
Rank 2: Jeff
Rank 3: Bill

Rank 1: Elon
Rank 2: Jeff
Rank 3: Bill

Rank 1: Bill
Rank 2: Jeff
Rank 3: Elon

Rank 1: Bill
Rank 2: Jeff
Rank 3: Elon

Rank 1: Jeff
Rank 2: Elon
Rank 3: Bill

Elon

```
