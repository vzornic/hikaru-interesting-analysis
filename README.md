# [WIP] Analysis of Hikaru Nakamura 2023 chess.com games and probability of cheating

Given the recent "accusations" made by former chess world champion Vladimir Kramnik I have decided to start an open source
project which will deal with this matter. Note that I wrote "accusations" as GM Vladimir Kramnik never actually accussed GM Hikaru Nakamura but rather all he said
is that his winning streak is "interesting".

What we will be doing here is taking all GM Hikaru Nakamura games from 2023 and analyze the data
we find. We will be trying to find an unusual patterns in streak games that GM Vladimir Kramnik finds "interesting". The data we have is taken
from chess.com published API, and we will use a stockfish engine to enrich this data for our analysis.

This analysis will not be a simple probability calculation to give us estimate but rather we will look into the data from different aspects to try to find
unusual patterns.

The project will consist of two jupiter notebook files which can be used in google colab
if you wish to collaborate on this project. More on collaboration you can find in sections below.

First file is related to data extraction and enrichment and the other file is related to
actual analysis. Once I'm done with my analysis I'll write [report](report.md) on my findings.

You can use [data](data.ipynb) and [analysis](analysis.ipynb) to see 
how I evaluated these games and to follow my thoughts when I was writing this report.


## $whoami & motivation 

### Personal

As a software engineer with 9 years of experience working mainly with Java, I've recently decided
to get a more knowledge and better experience in ML and AI space. The reason for that is the anxious feeling I started
developing with all the GPTs and AI hype. While I do have basic understanding on
how all of these work, I've decided to spend 6 months - 1 year (starting 12/2023) on learning and practicing ML specifically.

My end goal here is to obtain skills necessary to build and work with ML solutions. 

That said, this topic seemed interesting for me as a practice specifically on working with python and relevant tools such as pandas which is important in data science world.

### Community

GM Kramnik did, in several occasions on his blog, mentioned that he is unhappy because chess.com is not publishing analysis on this matter I've 
decided to push a community driven analysis where GM Kramnik may contribute with his analysis as well. I believe this is a good place to put our numbers
and see what a statistic shows.

## Disclaimer

The content provided in this blog post is based on my personal analysis as a software engineer on the road of learning DS (ML). 
While I strive for accuracy, I am not a data scientist or mathematician and the information presented here should be taken as my own interpretation and perspective, and not as professional advice.

Additionally, the data used for analysis might have limitations or biases that I might not be aware of. Please use your own judgment and consider seeking guidance from experts in the specific domain.

## Problem and analysis

Now before going into analysis itself we need to figure out on how can we detect cheating. For average players it would be much easier
as we could easier detect "suspicious" behaviour. However, for GMs such as Hikaru Nakamura it is quite more tricky as they can 
pretty much play moves as stockfish would play. Moreover, GMs would not need to cheat on many moves, as GM Hikaru Nakamura said in his YouTube videos
all he would need to do is to get a "signal" that in some position he just needs to spend more time thinking because there is a move which gives him edge. As you can tell it is extremely hard to detect if GMs are occasionally cheating. 

In this project we'll attempt to find was there "suspicious" behaviour in winning streak games made by GM Hikaru comparing it to other data we have from chess.com.

Our first step is to extract the raw data, enrich it and save into several data sets we will be using for our analysis. [More on data](data.ipynb)

After we have enriched data we'll move to [Analysis](analysis.ipynb) where we will be doing deep dive into this data and stats.

## Contribution

There are two ways on how you can contribute to this analysis, depending on whether you are experienced with python or not.

If you are experienced python engineer who want to contribute please feel free to open Pull requests out of forked repository which I'll try to look at frequently, review and merge.

If you are not a python engineer and you still want to contribute, please file a GitHub issue specifying details on what you think needs to be done so I or other contributors can apply it.

