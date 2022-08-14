---
layout: default
---
## About Me

I'm an undergraduate student at the University of Toronto pursuing a major in Civil Engineering (Transportation focus) and a minor in Machine Intelligence. Currently, I am performing research at the Data Driven Decision Making Lab regarding the application of reinforcement learning to traffic perimeter control.

During my undergraduate studies, I've developed a love for computer science and data science in particular. Inside of school, I've developed the relevant knowledge and experience through coursework and competitions. I've taken numerous courses with high standings such as statistics, probability, data science and machine learning. Addtionally, I've trained and succesfully engaged in algorithmic programming competitions. In 2022 I scored 9th in the University of Toronto's Undergraduate's Competitive Programming tryouts, and finished 15th/83 at the [East Central North America ICPC Regionals](https://icpc.global/regionals/finder/East-Central-NA-2021/standings). Additionally, I've applied my reinforcement learning skills to [OpenAi's official Car Racing leaderboard](https://github.com/openai/gym/wiki/Leaderboard), scoring the highest test score and beating the environment at the 2nd lowest training cost.

Outside of school, I've had research internships at Data and Transportation labs focused on the application of state of the art machine learning techniques to practical problems. Currently I'm at the Data Driven Decision making lab researching the ability of reinforcement learning agents to regulate traffic inflow to large protected regions. This is a control problem, involving multiple cooperating agents. In the summer of 2021, I was at the University Transportation Research Institute, serving as a software engineer. I aided my supervisor in the calibration of Aimsun traffic models, developping new tools to process geospatial data. Some of this work is visible in my portfolio. 

## Research Interests
Currently I am researching the application of multiple reinforcement learning agents to regulate traffic inflow to a large protected region. I would love to explore other practical applications of RL or the learning process such as imitation learning. I am also interested in spatial-temporal data and their prediction. In Transportation industry, this is used for traffic prediction, demand prediction, navigation and map services. Most importantly, I am open to exploring new areas of Data Science.

## Awards

- 9th place University of Toronto Undergraduate's Competitive Programming Tryouts
- 15th/83 East Central North America ICPC Regionals
- Highest test score OpenAI Official Car Racing Leaderboard
- Dean's Honour List (7/8 Semesters) 

## Publications

First submission December 2022

## Portfolio

&nbsp;
# Learning Reinforcement Learning via Car Racing

**2022.6** &nbsp; [Full Document](https://github.com/Ceudan/Car-Racing)

I hand coded multiple reinforcement learning algorithms for the openai Car Racing environment. Namely I applied Double Deep Q networks and Proximal Policy Optimization. The purpose of this project was to become familiar with RL libraries, algorithms and hyperparameter tuning. While exploring, I gave myself a research question. That is, can I officially beat the environment at a lower computational cost than others?

https://user-images.githubusercontent.com/78922263/177021714-fc82a6ff-e44c-4936-bf50-61a8f3a372f1.mp4

My PPO project was very succesful, obtaining the highest test score and beating the environment at the 2nd lowest training cost on OpenAI's official Car Racing leaderboard [[1]](https://github.com/openai/gym/wiki/Leaderboard). (917/900 score averaged over 100 test episodes, after 925 training episodes). I used a unique method for the environment. Mainly, I seperated the steering and thrust actions to 2 independantly trained networks to simplify the learnable relationship. Additionally, I moved speed estimation to a seperate deterministic process to reduce the computer vision load on our actor/critic models. 

&nbsp;

# Alphanumeric CAPTCHA Solver

**2021.3** &nbsp; [Full Document](https://github.com/Ceudan/Alphanumeric-CAPTCHA-Solver)

Led a team of 4 to independently design from scratch a multi-staged software that decodes alphanumeric CAPTCHA images. Motivation was a course final project. Input consists of 5 character CAPTCHAs disguised with noise and various levels of overlap, rotational, distance and colour distortions. Output is a 5 character prediction of the sequence.

![Image of a CAPTCHA and the software's predicted output](images/output.png) 

Stages:
\
&#8291;1. Preprocessing using computer vision libraries to eliminate noise.
\
&#8291;2. Character segmentation using object recognition to localize individual characters.
\
&#8291;3. Character classification using a convolutional neural network followed by several fully connected layers.

Achieved mark of 90%. Achieved an accuracy of 71% per entire CAPTCHA image and 91% per individual character. These accuracies are high given that CAPTCHAs are designed not to be bypassed by computer software. 

&nbsp;

<!-- Skills Learned: computer vision libraries, image processing, deep-learning, generating custom train data -->

# Predicting Student Question Performance

**2021.11** &nbsp; [Full Document](https://github.com/Ceudan/Predicting-Student-Question-Performance)

Led a team of 3 to write an ensemble machine learning model with bagging to predict a student's performance on diagnostic questions. Our ensemble combined 3 distinct algorithms. Motivation was a course project.

Given Data

![Diagram of given data](images/sparse_matrix.png)

Model Architecture

![Image of bagging and model architecture](images/Architecture.png)

Achieved mark of 97%. We ranked 18th in a coursewide competition (over 300 eligible competitors) with an accuracy of 70.3%. After fixing bugs and updating model to current version, accuracy increased to 71.3%, which would have ranked us 5th place.

&nbsp;

<!-- Skills Learned: pytorch, autograd, optimization, bagging, ensemble -->

# Sliding Puzzle Solver
[Virtual Game Link](https://www.proprofsgames.com/puzzle/sliding/mona-lisaq/)

There are 2 distinct stages to this puzzle. First, you must estimate the original configuration of the subpieces. Second, you must find a way to rearrange the subpieces into the original configuration while obeying the constraints of the game.

### Subtask 1: Original Configuration Estimation

**2022.3** &nbsp; [Full Document](https://github.com/Ceudan/Sliding-Puzzle-Solver/blob/main/README.pdf)

Worked in a team of 3 leveraging Deep CNN's and advanced combinatoric algorithms for the task. This subtask is identical to that of solving square jigsaws. Pipeline consisted of pre-processing raw scenic images into the puzzle structure, fine-tuning pretrained Deep CNN's to predict the likelihood of sub-peices being conjoined, then utilising a deterministic solving algorithm to estimate most the likely configuration.

![Image of configuration estimator architecture](images/Solver_Architecture.png)

All Deep CNN's achieved an adjacency prediction accuracy of over 90%. Importantly, by testing various pre-trained architectures such as RESNet, RESNext and VGG we were able to deduce useful insights regarding the application of CNN's to the problem. Namely, shorter wider CNN's outperform deeper ones. This was due to the models facing significant error when comparing images lacking in large features (ex. subpieces of the sky), where localized pixel level details become critical. We hypothesiszed this may prove difficult for Deep CNN's where location and low level information is lost in its deeper layers, especially when tuning models pretrained for object recognition. 


### Subtask 2: Tile Rearrangement
One day I hope to have enough time to return and complete this section comparing various reinforcement learning techniques.

&nbsp;

# Matching Road Sections between Databases

**2021.8** &nbsp; [Full Document](https://github.com/Ceudan/Match-Roads-Between-Databases)

I independently created software to match sections across databases using geospatial information. This was one of the many tasks I recieved at the University of Toronto Transportation Research Institute. Hurdles included:
- over 100,000 road sections per database (strong time complexity requirements)
- close proximity does not gaurentee correct match
- geographic coordinates carry up to 10 metres of uncertainty



![Visualization of road sections in Database 1](images/ex1_HERE.png) ![Visualization of road sections in Database 2](images/ex1_aimsun.png) ![Visualization of road sections in Database 2](images/ex1_match_background.png) 


Achieved an accuracy of 94% on normal road types. Accuracy is dynamic since adjustable thresholds can tradeoff quantity with quality. It was succesfully used to match sections from an Aimsun traffic simulation covering the GTHA, with HERE Technologies' observed traffic information.

<!-- Skills Learned: GeoPandas, GIS, shapefiles, search algorithms, matrix/array time dependancies-->





<span style="font-size:18px;">[Projects](./projects.html)</span>

<span style="font-size:18px;">[Travel](./travel.html)</span>

<span style="font-size:18px;">[Blog](./blog.html)</span>
