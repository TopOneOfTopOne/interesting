# interesting
Interesting things transposed to programming code

```ruby
# Given 70 people ignoring special events such as twins and leaps the probability of 
# two people having the same birthday is **acutally 99.9%**
#
# Inspired by the birthday problem/paradox.
# Given a set of size size, and n occurances within the set
# the function below calculates the probability of a duplicate occurance
#
# Example:
# set: [1,2,3,4,5] n: 2 (i.e. 2 numbers are chosen from set)
# calc_prob_of_dup(2, 5) #=> 0.2
#
# We can of course calculate this intuitively as 1/5
# But when n and size become larger it becomes more difficult to derive the probabilty # of a duplicate by hand
#
# Note: Duplicate in this context simply means a chosen element occuring more than once
def calc_prob_of_dup(n, size)
	1 - ((0...n).to_a.inject(1) { |product, n| product * ((size - n.to_f)/size) })
end
```
