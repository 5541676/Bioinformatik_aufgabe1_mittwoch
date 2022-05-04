# Bioinformatik_aufgabe1_mittwoch

Hallo, 
ich habe eine kleine Anmerkung. Ich habe alle aufgaben bearbeitet und nur zwei davon nicht lösen können... Daher verstehe ich nicht, wieso ich nur um die 50% angerechnet bekommen habe? 
LG..


![WhatsApp Image 2022-05-04 at 19 09 51](https://user-images.githubusercontent.com/104322434/166743293-ac06d457-b78d-431c-963b-ed49a6cb415a.jpeg)
![WhatsApp Image 2022-05-04 at 19 10 05](https://user-images.githubusercontent.com/104322434/166743550-dad6d293-696c-4532-ae60-9101842bf484.jpeg)
![WhatsApp Image 2022-05-04 at 19 20 48](https://user-images.githubusercontent.com/104322434/166743901-055fad1c-028e-4b3a-8c12-6678734525fb.jpeg)



#Section 1
# Here is how you compute the sum for the first 20 integers
20*(20+1)/2 

# However, we can define a variable to use the formula for other values of n
n <- 20
n*(n+1)/2

n <- 25
n*(n+1)/2

# Below, write code to calculate the sum of the first 100 integers
n <- 100
n*(n+1)/2


# Below, write code to calculate the sum of the first 1000 integers 
n <- 1000
n*(n+1)/2


#Functions

#Run the following code in the R console:
  
  n <- 1000
x <- seq(1,n)
sum(x)
#Based on the result, what do you think the functions seq and sum do? You can use the help system.

Instructions
#50 XP
#Possible Answers

#sum creates a list of numbers and seq adds them up.

#seq creates a list of numbers and sum adds them up.# das hier ist richtig

#seq computes the difference between two arguments and sum computes the sum of 1 through 1000.

#sum always returns the same number


# log to the base 2 
log2(16)

# sqrt of the log to the base 2 of 16:
sqrt(log2(16))

# Compute log to the base 10 (log10) of the sqrt of 100. Do not use variables.
log10(sqrt(100))


#Nested functions call 2

#Which of the following will always return the numeric value stored in x? You can try out examples and use the help system in the R console.

Instructions
#50 XP
#Possible Answers

log(10^x)

log10(x^10)

log(exp(x)) #das hier ist richtig

exp(log(x, base = 2))


#Next, use the function str to examine the structure of the murders object. We can see that this object is a data frame with 51 rows and five columns.

#Which of the following best describes the variables represented in this data frame:
  
  Instructions
#50 XP
#Possible Answers

#The 51 states

#The murder rates for all 50 states and DC

#
  The state name, the abbreviation of the state name, the state's region, and the state's population and the total number of murders for 2010.
# das letzte ist richtig



# Load package and data

library(dslabs)
data(murders)

# Use the function names to extract the variable names 
names(murders)


# To access the population variable from the murders dataset use this code:
p <- murders$population 

# To determine the class of object `p` we use this code:
class(p)

# Use the accessor to extract state abbreviations and assign it to a
a <- murders$abb
# Determine the class of a
class(a)





# We extract the population like this:
p <- murders$population

# This is how we do the same with the square brackets:
o <- murders[["population"]] 

# We can confirm these two are the same
identical(o, p)

# Use square brackets to extract `abb` from `murders` and assign it to b
b <- murders[["abb"]] 

# Check if `a` and `b` are identical 
identical(a, b)



# We can see the class of the region variable using class
class(murders$region)

# Determine the number of regions included in this variable 
levels(murders$region)
length(murders$region)
length(levels(murders$region))


# The "c" in `c()` is short for "concatenate," which is the action of connecting items into a chain
# The function `c()` connects all of the strings within it into a single vector, which we can assign to `x`
x <- c("a", "a", "b", "b", "b", "c")
# Here is an example of what the table function does
table(x)

# Write one line of code to show the number of states per region



# Here is an example creating a numeric vector named cost
cost <- c(50, 75, 90, 100, 150)

# Create a numeric vector to store the temperatures listed in the instructions into a vector named temp
# Make sure to follow the same order in the instructions
temp <- c(35, 88, 42, 84, 81, 30)


# here is an example of how to create a character vector
food <- c("pizza", "burgers", "salads", "cheese", "pasta")

# Create a character vector called city to store the city names
# Make sure to follow the same order as in the instructions
city <- c("Beijing", "Lagos", "Paris", "Rio de Janeiro", "San Juan", "Toronto")


# Associate the cost values with its corresponding food item
cost <- c(50, 75, 90, 100, 150)
food <- c("pizza", "burgers", "salads", "cheese", "pasta")
names(cost) <- food

# You already wrote this code
temp <- c(35, 88, 42, 84, 81, 30)
city <- c("Beijing", "Lagos", "Paris", "Rio de Janeiro", "San Juan", "Toronto")

# Associate the temperature values with its corresponding city
names(temp) <- city


# cost of the last 3 items in our food list:
cost[3:5]

# temperatures of the first three cities in the list:
temp[1:3]


# Access the cost of pizza and pasta from our food list 
cost[c(1,5)]

# Define temp
temp <- c(35, 88, 42, 84, 81, 30)
city <- c("Beijing", "Lagos", "Paris", "Rio de Janeiro", "San Juan", "Toronto")
names(temp) <- city

# Access the temperatures of Paris and San Juan
temp[c("Paris","San Juan")]



# Create a vector m of integers that starts at 32 and ends at 99.
m <- 32:99

# Determine the length of object m.
length(m)

# Create a vector x of integers that starts at 12 and ends at 73.
x <- 12:73
# Determine the length of object x.
length(x)


# Create a vector with the multiples of 7, smaller than 50.
seq(7, 49, 7) 

# Create a vector containing all the positive odd numbers smaller than 100.
# The numbers should be in ascending order
seq(1, 100,2)


# We can create a vector with the multiples of 7, smaller than 50 like this 
seq(7, 49, 7) 

# But note that the second argument does not need to be the last number
# It simply determines the maximum value permitted
# so the following line of code produces the same vector as seq(7, 49, 7)
seq(7, 50, 7)

# Create a sequence of numbers from 6 to 55, with 4/7 increments and determine its length
seq(6, 55, 4/7)
length(seq(6, 55, 4/7))



# Store the sequence in the object a
a <- seq(1, 10, length.out = 100)

# Determine the class of a
class(a)



# Store the sequence in the object a
a <- seq(1, 10)

# Determine the class of a
class(a)



# Check the class of 1, assigned to the object a
class(1)

# Confirm the class of 1L is integer
class(1L)




# Define the vector x
x <- c(1, 3, 5,"a")

# Note that the x is character vector
x

# Redefine `x` to typecast it to get an integer vector using `as.numeric`.
# You will get a warning but that is okay
x <- as.numeric(x)


# Access the `state` variable and store it in an object 
states <- murders$state 

# Sort the object alphabetically and redefine the object 
states <- sort(states) 

# Report the first alphabetical value  
states[1]

# Access population values from the dataset and store it in pop
pop <- murders$population
# Sort the object and save it in the same object 
pop <- sort(pop)
# Report the smallest population size 
pop[1]



# Access population from the dataset and store it in pop
pop <- murders$population
# Use the command order to find the vector of indexes that order pop and store in object ord
index <- order(pop)
pop[index]
# Find the index number of the entry with the smallest population size
pop[1]



# Find the index of the smallest value for variable total 
which.min(murders$total)

# Find the index of the smallest value for population
which.min(murders$population)


# Define the variable i to be the index of the smallest state
i <- which.min(murders$population)

# Define variable states to hold the states
states <- murders$state
# Use the index you just defined to find the state with the smallest population
states[i]



# Store temperatures in an object 
temp <- c(35, 88, 42, 84, 81, 30)

# Store city names in an object 
city <- c("Beijing", "Lagos", "Paris", "Rio de Janeiro", "San Juan", "Toronto")

# Create data frame with city names and temperature 
city_temps <- data.frame(name = city, temperature = temp)
# Define a variable states to be the state names 
states <- murders$state

# Define a variable ranks to determine the population size ranks 
ranks <- rank(murders$population)

# Create a data frame my_df with the state name and its rank
my_df <- data.frame(name = states, population = ranks)


# Define a variable states to be the state names from the murders data frame
states <- murders$state

# Define a variable ranks to determine the population size ranks 
ranks <- rank(murders$population)

# Define a variable ind to store the indexes needed to order the population values
ind <- order(ranks)

# Create a data frame my_df with the state name and its rank and ordered from least populous to most 

my_df <- data.frame(name = states[ind], ranks = ind[ranks])
my_df



# Using new dataset 
library(dslabs)
data(na_example)

# Checking the structure 
str(na_example)

# Find out the mean of the entire dataset 
mean(na_example)

# Use is.na to create a logical index ind that tells which entries are NA
ind <- is.na(na_example)
# Determine how many NA ind has using the sum function
sum(ind)



# Note what we can do with the ! operator
x <- c(1, 2, 3)
ind <- c(FALSE, TRUE, FALSE)
x[!ind]

# Create the ind vector
library(dslabs)
data(na_example)
ind <- is.na(na_example)

# We saw that this gives an NA
mean(na_example)

# Compute the average, for entries of na_example that are not NA 
mean(na_example[!ind])




# Assign city names to `city` 
city <- c("Beijing", "Lagos", "Paris", "Rio de Janeiro", "San Juan", "Toronto")

# Store temperature values in `temp`
temp <- c(35, 88, 42, 84, 81, 30)

# Convert temperature into Celsius and overwrite the original values of 'temp' with these Celsius values
(temp-32)*5/9
temp <- c(1.666667, 31.111111,  5.555556, 28.888889, 27.222222, -1.111111)
# Create a data frame `city_temps` 
city_temps <- data.frame( city, temp)



# Define an object `x` with the numbers 1 through 100
seq(1,100)
x <-seq(1,100)
# Compute the sum 
1/x^2
sum(1/x^2)



# Load the data
library(dslabs)
data(murders)

# Store the per 100,000 murder rate for each state in murder_rate
murder_rate <- murders$total/murders$population*100000
# Calculate the average murder rate in the US 
mean(murder_rate)



# Store the murder rate per 100,000 for each state, in `murder_rate`
murder_rate <- murders$total / murders$population * 100000

# Store the `murder_rate < 1` in `low` 
low <- c(murder_rate < 1)
which(low)



# Store the murder rate per 100,000 for each state, in murder_rate
murder_rate <- murders$total/murders$population*100000

# Store the murder_rate < 1 in low 
low <- murder_rate < 1

# Get the indices of entries that are below 1
index <-murder_rate <1
which(low)



# Store the murder rate per 100,000 for each state, in murder_rate
murder_rate <- murders$total/murders$population*100000

# Store the murder_rate < 1 in low 
low <- murder_rate < 1

# Names of states with murder rates lower than 1
small <- murders$population < 1000000
murders$state[small]
index <-murder_rate <1
murders$state[index]



# Store the murder rate per 100,000 for each state, in `murder_rate`
murder_rate <- murders$total/murders$population*100000

# Store the `murder_rate < 1` in `low` 
low <- murder_rate < 1

# Create a vector ind for states in the Northeast and with murder rates lower than 1. 
ind <- low & murders$region=="Northeast"
# Names of states in `ind` 
murders$state[ind]


# Store the murder rate per 100,000 for each state, in murder_rate
murder_rate <- murders$total/murders$population*100000


# Compute the average murder rate using `mean` and store it in object named `avg`
avg <- mean(murder_rate)

# How many states have murder rates below avg ? Check using sum 
sum(murder_rate < avg)


# Store the 3 abbreviations in a vector called `abbs` (remember that they are character vectors and need quotes)
abbs <- c("AK", "MI", "IA")
# Match the abbs to the murders$abb and store in ind
ind <- match(abbs , murders$abb)
# Print state names from ind
murders$state[ind]


# Store the 5 abbreviations in `abbs`. (remember that they are character vectors)
abbs <- c("MA", "ME", "MI", "MO", "MU") 


# Use the %in% command to check if the entries of abbs are abbreviations in the the murders data frame
abbs%in%murders$abb


# Store the 5 abbreviations in abbs. (remember that they are character vectors)
abbs <- c("MA", "ME", "MI", "MO", "MU") 

# Use the `which` command and `!` operator to find out which index abbreviations are not actually part of the dataset and store in `ind`
ind <- which(!abbs%in%murders$abb)
# Names of abbreviations in `ind`
abbs[ind]



# Loading data
library(dslabs)
data(murders)

# Loading dplyr
library(dplyr)

# Redefine murders so that it includes a column named rate with the per 100,000 murder rates
murders <- mutate(murders,rate=total/population*100000)


# Note that if you want ranks from highest to lowest you can take the negative and then compute the ranks 
x <- c(88, 100, 83, 92, 94)
rank(-x)

# Defining rate
rate <-  murders$total/ murders$population * 100000

# Redefine murders to include a column named rank
# with the ranks of rate from highest to lowest
murders <- mutate(murders, rank = rank(-rate))


# Load dplyr
library(dplyr)

# Use select to only show state names and abbreviations from murders
select(murders, state, abb)


# Add the necessary columns
murders <- mutate(murders, rate = total/population * 100000, rank = rank(-rate))

# Filter to show the top 5 states with the highest murder rates
filter(murders, rank <= 5)



# Use filter to create a new data frame no_south
no_south <- filter(murders, region != "South" )
# Use nrow() to calculate the number of rows
nrow(no_south)


# Create a new data frame called murders_nw with only the states from the northeast and the west
murders_nw <- filter(murders, region %in% c("Northeast", "West"))
# Number of states (rows) in this category 
nrow(murders_nw)



# add the rate column
murders <- mutate(murders, rate =  total / population * 100000, rank = rank(-rate))

# Create a table, call it my_states, that satisfies both the conditions 
my_states <- filter(murders, region %in% c("Northeast", "West") & rate < 1)
# Use select to show only the state name, the murder rate and the rank
select(my_states, state, rate, rank)



# Load library
library(dplyr)

## Define the rate column
murders <- mutate(murders, rate =  total / population * 100000, rank = rank(-rate))

# show the result and only include the state, rate, and rank columns, all in one line, in that order
filter(murders, region %in% c("Northeast", "West") & rate < 1) %>%  
  select(state, rate, rank)


# Loading the libraries
library(dplyr)
data(murders)

# Create new data frame called my_states (with specifications in the instructions)
my_states <- murders %>% 
  mutate(rate =  total / population * 100000, rank = rank(-rate)) %>%
  filter(region %in% c("Northeast", "West") & rate < 1) %>%
  select(state, rate, rank)


# Load the datasets and define some variables
library(dslabs)
data(murders)

population_in_millions <- murders$population/10^6
total_gun_murders <- murders$total

plot(population_in_millions, total_gun_murders)

# Transform population (not population in millions) using the log10 transformation and save to object log10_population
log10_population<- log10(murders$population)

# Transform total gun murders using log10 transformation and save to object log10_total_gun_murders
log10_total_gun_murders <- log10(murders$total)
# Create a scatterplot with the log scale transformed population and murders 
plot(log10_population, log10_total_gun_murders)


# Store the population in millions and save to population_in_millions 
population_in_millions <- murders$population/10^6


# Create a histogram of this variable
hist(population_in_millions)


# Create a boxplot of state populations by region for the murders dataset
boxplot(population~region, data = murders)





#not all positive

#all(!x

# Assign the state abbreviation when the state name is longer than 8 characters 
new_names <- ifelse(nchar(murders$state)>8, murders$abb, murders$state)
head(new_names)


# Create function called `sum_n`
sum_n <- function(n){
  x <- 1:n
  sum(x)
}
# Use the function to determine the sum of integers from 1 to 5000
sum_n(5000)


# Create `altman_plot` 
altman_plot <- function(x, y){
  plot(x + y, y - x)
}

# Run this code 
x <- 3
my_func <- function(y){
  x <- 5
  y+5
}

# Print the value of x 
example_func <- function(n){
  x <- 1:n
  sum(x)
}


# Here is an example of a function that adds numbers from 1 to n
example_func <- function(n){
  x <- 1:n
  sum(x)
}

# Here is the sum of the first 100 numbers
example_func(100)

# Write a function compute_s_n with argument n that for any given n computes the sum of 1 + 2^2 + ...+ n^2
compute_s_n <- function(n){
  x <- 1:n
  sum(x^2)
}

# Report the value of the sum when n=10
compute_s_n(10)


# Define a function and store it in `compute_s_n`
compute_s_n <- function(n){
  x <- 1:n
  sum(x^2)
}

# Create a vector for storing results
s_n <- vector("numeric", 25)

# write a for-loop to store the results in s_n
for(i in 1:25){
  s_n[i] <- compute_s_n(i)
}



# Define the function
compute_s_n <- function(n){
  x <- 1:n
  sum(x^2)
}

# Define the vector of n
n <- 1:25

# Define the vector to store data
s_n <- vector("numeric", 25)
for(i in n){
  s_n[i] <- compute_s_n(i)
}

#  Create the plot 
plot(n, s_n)


# Define the function
compute_s_n <- function(n){
  x <- 1:n
  sum(x^2)
}

# Define the vector of n
n <- 1:25

# Define the vector to store data
s_n <- vector("numeric", 25)
for(i in n){
  s_n[i] <- compute_s_n(i)
}

# Check that s_n is identical to the formula given in the instructions.
identical(s_n, (n*(n+1)*(2*n+1))/6)



