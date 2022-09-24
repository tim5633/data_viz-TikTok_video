# data_viz-TikTok_video

## 1. Introduction
Analyzed and visualised TikTok Trending Videos dataset, to find the reason why and what makes TikTok videos so popular nowadays. We utilized `matplotlib`, `seaborn` package to present three plots.

## 2. Dataset
the TikTok Trending Videos dataset is available [here](https://www.kaggle.com/datasets/erikvdven/tiktok-trending-december-2020/ "link"). 

## 3. Results of Plots

### 3.1. Short videos made to thrive

<img width="1100" alt="Screenshot 2022-09-24 at 1 37 49 AM" src="https://user-images.githubusercontent.com/61338647/192072541-922b9ab2-bd24-458f-beaf-a97083bc908a.png">

**Trends:**  
A short video, defined as one of a content transporting way within 1 minute, has swept the world in a fast path on different media platforms such as Instagram video, YouTube Short, and LinkedIn portfolio features video. What makes TikTok stands out is the combination of short videos creators created and viewer engaged with intermittent variable rewards, the mechanism mentioned above. The platform is like addictive snacks that feed the greed of both demand and supply sides.

**Insights:**  
We now based on the personal dataset of actual 1000 trending TikTok videos recommended by the TikTok mechanism. We were originally doing a regression model but there were not significant for every variable, so we plot it out first and did see some trends between different hubs.
1. About the data processing:
- We cut the 12 group bins spacing with 5 seconds
- Each scatter, and the texts above bars represent the group preformance mean (iii.) We used scipy stats to remove outliers of |Z-score| > 3
- We standardized four counts in order to see the trend simultaneously at one plot (v.) We use make_interp_spline and linspace to smoothe the line plot
2. The graph contains four dimantions, which is:
- Creators and Viewers
- Average length of creaters tend to flim video seconds
- The amount of videos posted on tiktok seprated wirh 5 seconds as a group
- The trend of normalizing average of different gngagements such as play count, share count, digg coumt, and comment count

**Result-Video Length and Engagement Peak:**  
1. From the viewer’s perspective, According to the marketing statistics from Hubspot website, over 5% of people will drop off if the video playing on their phone is over 1 minute and 60% will if over 2 minutes. Due to the fast pace of life, traditional long-length streaming media would no longer satisfy users. Tiktok, a short streaming media application, comes as a boom hit to the world. The shorter, the better.
2. From the Creator’s perspective, If we look specifically at the gap between average posting seconds of each group is 3.53s, 5.12s, 4.33s, 4.8s, 5.76s, 4.57s, 4.75s, 4.72s, 4.95s, 5.66s, 5.24s. Besides the gap of 1st and 2md group and the lowest, a gap of 3rd and 4th group are the second-lowest and the video posting amount of 3rd is the highest. The overall amount is 370 posts, or 37% of videos fall into group 11-15 seconds. Indicating that creators tend to make videos with a 13.57 average length. Though the Engagement Peak is around 16 to 20 seconds, Both Peaks display that supply of creators and demand of viewers meet together and explain why videos below 30 seconds are nowadays trending via different media platforms to attract attention easily and quickly.

**Result-Share and Play Count of second-highest:**  
“5-Second Rule” is the best explanation in group1, 1-5 seconds. In order to let viewers grab information immediately, Few moments of the video usually would only extract extreme contents. In other words, the set of tone in the video is usually touching, impressive, or informative, which is worthy to share and as the result bringing out the play count.

**Result-Comment Count of second-highest:**  
Especially we looked at group12, 56-60seconds, of its comment count is the second-highest in the graph. We believe that the longer the videos are, people would have more feelings and thoughts. Compared to group1, 1-5 seconds, although longer videos make viewers lose interest, the content of longer videos might be rich and touching to motivate viewers to leave comments on them.

**Result-Digg Count of second-highest:**  
The group8, 36-40 seconds, is with second-highest Digg count. We did not expect to see this and did look back to the group dataset and inspect nothing. We suspected celebrities would have too much engagement and cause bias:
1. Matched the top 50 TicTok celebrities from Wikipedia but inspected only 10 videos from
celebrities would also tend to post under 25 seconds of the video.
2. Remove outlier of overall dataset of top 10 Digg count video and |Z-score| > 3 columns Eventually, the peak is still and we think removing too many values will lose the authenticity of the dataset. There might be other external factors we didn’t reach out to. We could only suppose that the simple size of group8, 36-40 seconds is too less and willing to cause bias.

### 3.2. Hashtags Interests
![Screenshot 2022-09-24 at 1 48 11 AM](https://user-images.githubusercontent.com/61338647/192072963-1aad624d-cf07-4d53-b2e2-b114d89fdac1.png)

**Trends:**  
As far as hashtags are concerned, hashtag is the most direct way to identify whether we are interested in this video before we actually watch it. Thus, a well-designed hashtag can be really useful if a blogger hope that his video can reach his target audience, however, more hashtags are sometimes averse to play count, which is consolidated by the regression output between hashtag count and play count. So, choosing hashtags is not a free rein if you expect your video to become a hit.

**Insights:**  
We noticed that there are tons of rating lists bombarding in the internet, shouting which hashtags are swaying away in the last one week. Although not every hashtag can bring a significant effect to video’s popularity, we may have to admit that some hashtags are more equal than others. To clarify, we don’t analyze hashtags themselves, but the video content categories they are on behalf.

**Hypothesis:**  
Based on this hypothesis, we want to examine that whether a specific hashtag can boost popularity of a video on its own. We selected hashtags that had been used more than ten times in dataset and rendered every hashtag as a dummy variable, so we could examine coefficient significance of different hashtags to measure if it indeed has an effect on video.

**Result:**  
We found two hashtags stood out: stitch and funny. Stitch is a novel function which allows users to slice part of a TikTok video and add their own contents. Stitch usually occurs in such scenario: bloggers are trying to give further insights to a movie, documentary or any other videos people are interested in; or they can directly call back to original bloggers by stitching their videos and making some eye-catching speeches. The interactive nature of stitch is the main reason that stitch hashtag has become the most significant hashtag in relevance to play count. As for funny, even the most stoic people sometimes need laughter. That’s all.

**Plotting Out:**  
Finally, we want to visualize this significance within hashtag community via library WordCloud. We created a word cloud shaped in TikTok logo. The font size of hashtag is weighted on average play count of videos containing this hashtag. Stitch and Funny, without question, is the top two largest words in our picture.

### 3.3. Best times to post on TikTok
![Screenshot 2022-09-24 at 1 49 20 AM](https://user-images.githubusercontent.com/61338647/192072999-59abecba-b483-4e66-aa06-0e71c7fbf804.png)

**Trends:**  
Posting a video at the right timings would certainly be an excellent strategy for creators to grow their audience base with the help of expected maximum engagement of the audiences at certain window of times during the day. After analysing over 1000 TikTok video posts of the dataset, certain days and times are found to get more engagement on TikTok than others.

**Insights:**  
See below for summary of our findings on videos with top views:
|  **Part of Day**  |  **Window of Time**  |  **Week of Day**  |
|-------|:-----:|------:|
|  Morning  |  7am - 10am  |  Monday , Wednesday, Saturday  |
|  Noon  |  3pm  |  Thursday, Friday, Sunday  |
|  After Working Hours  |  6pm - 11pm  |  Monday - Sunday, except Tuesday  |
|  Midnight  |  1am - 5am  |  Monday, Wednesday, Friday, Saturday  |

Based on our findings, one of best time windows to post on TikTok is from 7:00 AM to 10:00 AM on Monday, Wednesday and Saturday. This fall within the expectation as people are getting started on their day and tend to go online. They’re taking the morning to get caught up on articles, scroll social media for news, and get their brains ready for work. Posts on Monday have the highest view with 11 million in total at 9:00 AM as people are battling post-weekend blues, hence, engagement rate is expected to be higer.  

Another best time window to post on TikTok is after working hours from 6:00 PM to 11:00 PM from Monday to Sunday, except for Tuesday. People are checking out what they missed over the day after working hours. Also, this is when adults complete their work and are on the hunt for some mind relaxation on social media.  

Further best time to post on TIkTok is 3:00 PM on Thursday, Friday and Sunday for higher visibility due to people turn to their lunch break. Lunchtime is always great because it’s when people tend to have the biggest gaps in their schedules.
While the initial target of TikTok founders are teenagers and hence, over 60% of TikTok users are aged between 16 -24. Tik Tok is addictive to many youngsters as the apps lets users record themselves dancing or goofing around to a music or spoken-word clip and then alter the videos using a wide array of effects. Teens tend to stay up late due to some reasons such as internal clock changes as they near puberty, pushing for independence and others. This group of users is usually still staying awake at from 1:00 AM to 5:00 AM, so engagement rate is high.  

**Design Choice:**  
To make use of visual cues to tell audiences how the engagement rate by video views varies over 24 hours of 7 days of a week, we have decided to mix these details by presenting them in a tabular format, hence, heatmap is data visualisation technique that has been applied in this case. Coloured cells have been leveraged to convey the relative magnitude of the numbers of Tiktok video views. We have also annotated specific cells with views that are over 3 million to allow audiences to quickly target the points of interests and immediately get a sense of its respective number of views. The lighter the colour of the cell, for instance, from blue to yellow, the higher the number of video views. This visual cues is very effective to help direct the attention of the audience.




