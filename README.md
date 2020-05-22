# Smart-Cab-Self-driving-cab-
A self-driving cab company wanted to design a simulation of a self-driving cab.

Problem Statement: 
A self-driving cab company Smartcab wanted to design a simulation of a self-driving cab.

Goal: 
Demonstrate the use of RL techniques to develop an efficient and safe approach for tackling the issue.

Project Description:
The Smartcab's job is to pick up the passenger at one location and drop them off in another. Here is a list of things that they would love our Smartcab to take care of:

● Drop off the passenger to the right location.

● Save passenger's time by taking minimum time possible to drop off

● Take care of passenger's safety and traffic rules

There are different aspects that need to be considered here while modeling an RL solution to this problem: rewards, states, and actions.

Company also wanted to allow users to book a cab by sending a free text SMS containing source, destination and time of travel. Since SMS is a free text, different users can send same message in different ways, e.g.,

1. I want to book a cab from cyber city to sector 48 at 5 pm.

2. Please book my cab with pick up from cyber city, destination sector 48, and time of pick up 5 pm.

3. Book a cab for me from sector 48, my pick-up is from cyber city at 5 pm.

So, the challenge for the company is to parse this free text and fetch three entities:

● Pick up location

● Destination

● Time to pick up

Process Flow/Overall solution:

Solve Open AI Gym environment “Taxi v2” using Q learning algorithm to learn a task of pickup, drop passengers and then evaluate the learned environment on the given data:

sms.txt: This file contains 1000 text messages containing information of pickup location, drop location, and time of pickup

Task to be solved:

Train:

1. Train a model using Q learning algorithm on tax v2 environment.

Evaluation:

1. Take text from "sms.txt" and fetch pickup and drop from it.

2. Generate the random state from an environment and change the pick-up and drop as the fetched one from sms.txt

3. Evaluate you model performance on all the texts given in sms.txt. We have generated text for four locations given in city.csv

4. Have a check if the fetched pickup, drop is not matching with original pickup, drop given in “orig_df.csv”

5. If fetched pickup or/and drop does not match with the original, add penalty and reward -10

6. Calculate the Total reward, penalties, Wrong pickup/drop predicted and Average time steps per episode.

