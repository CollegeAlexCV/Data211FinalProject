This project aims to see if there are any patterns in the randomization of the shuffle feature on Youtube Playlists. While we do not have access
to the source code, a series of 100 trials of the top 100 songs in a nearly 600 song playlist should show patterns which could show there may be 
a rejection to true randomness.

Null Hypothesis: The shuffle feature is completely random at all stages of the resulting playlist. I.E. The expected frequency is equivalent to the
recorded frequency.
Alternate Hypothesis: The shuffle feature has some deterministic factor when making its resulting playlist. I.E. The expected frequency at some stage
is different enough to a recorded frequency.

Over the course between 10/17 and 11/7 I performed 96 trials with varying frequencies of trials per day. I performed 4 more trials on 11/12 to round
out the list to 100. This got my lowest category to at least five for a goodness of fit test. Speaking of categories, here they are:

Cage The Elephant: 33 out of 588 videos. Frequency of ~5.61
Poor Man's Poison: 48 out of 558 videos. Frequency of ~8.16
The Crane Wives: 35 out of 588 videos. Frequency of ~5.95
The Heavy: 35 out of 588 videos. Frequency of ~5.95
Tupperware Remix Party: 68 out of 588 videos. Frequency of ~11.56
All Other Artists: 369 out of 588 videos. Frequency of ~62.76

The data collection included the actual channel they had, how many likes the video had, how many subscribers the channel had, 
if my channel had liked/subscribed per video, where the song was in the base playlist, and where they showed up in the first
100 songs per shuffle. Scraping a lot of the initial data off of youtube required me to familiarize myself with some tools and
methods I was not used to initially but got working. It also showed me I had copies of some songs on the playlist, or songs with
different artists but the same name. Over the course of my data collection I had to make sure I knew which copies were titled 
which way, usually if the song was labeled with some moniker like 'Original Audio'.

I underestimated how time consuming recording 100 entries 100 times was. Let it be known that my professor was right and that I should have gone
with a smaller playlist for times sake, but using a large playlist I found a consistent pattern that a small playlist likely would not
have shown. So my wrist pain has turned into valuable insight.

My methodology for testing was simple. Load onto the home page of youtube, enter my playlists section, load the playlist, and use the shuffle
button at the top without loading into any song to do so. I would then scroll through the list and typed out each song until I hit 100 entries.
The google sheet I used also had colored rows to tell me when I hit my Top1/10/25/50/100 marks.

Counting through it, I noticed that whenever I shuffled I only ever landed on the first 20 videos of the playlist. I confirmed this when I made
a geom_col graph that was ordered by the positioning in my data frame and the bars only appearing on the first 20 values. The goodness of fit
test then confirmed it showing there was far less than 1% chance for the distribution to occur naturally, but every other metric I hit was
unable to reject the null hypothesis.
