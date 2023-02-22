## 4 Something interesting

​	According to the problem, we could learn from the fact that the dataset given by this problem was taken from ***Twitter***, but ***Twitter***'s data was not comprehensive since  users have the right to choose whether to report their results. Following the rules of ***Wordle***, users have six chances to get the right answer, Otherwise he/she will fail the game. This game was a little bit difficult for most of us. However, after integrating the percentage of each try times in the dataset, we find most of the users completed the game within 5 trials, and only few (2.8%) failed the game, which is not in line with our tuition, **so we take the assumption that users who reported their results are usually those who completed the game and use less chances.** 

​	"here is bar chart"



  	In order to verify our assumption, we developed a model  to simulate the process of how people guess words  in ***Wordle***.  To simplify this model, we assume people choose words which come to their mind first, which has a high correlation with word frequency in English. So we continuing using the word frequency data taken from ***wolftram***, distributing probabilities to each word according to their frequency, and choose them randomly. the algorithm flow are as follows:

​	"here is algorithm flow"



​	 We calculated each word for 20 times, getting their average try time and compare it with the true average try time, seen from the line chart , the predict data was much higher than real data. and the Mean expected difference of these (359 words) was 6.925 (11.046-4.121),which was related to our assumption.

​	then we need to test the correctness of our algorithm model. we calculated Pearson correlation coefficient, and did hypothesis testing of these 2 data the result of which are as follow:

​	"Here is the table of the tests"

​	

​	since p=0.000<0.01, we are 99% sure that these 2 data have significant correlation, and the Pearson correlation coefficient is 0.53. We can conclude our model is useful and correct to some extent.

​	 To make further analysis, we integrated all predicted data and real data, getting its distribution and drew its histogram. As can be seen from the image, users who report their data are only the tip of the iceberg of the whole data. Behind the displayed data set, there are a large number of users who fail to guess the word successfully. Most users who share their data on Twitter had figure out the puzzle and had good game scores.

​	"Here is the picture of big mountain !"

​	

​	Based on this model, we try to figure out in what  kind of situation would users like to report their grades: we divide *real value* by *predict value* and rescaling it, and draw its line chart

​	"here is the line chart !"



​	Within the allowable range of errors, we find that, unlike the expected results, the proportion of sharing data does not show a monotonically decreasing trend, but first increases and then decreases, and reaches a peak at x=4. Although generally speaking players with better results are more likely to post their grades, the percentage declines when the results are too good (the number of attempts is close to one). We reasoned that such groups guessed words based more on probability than on the amount of information in the question. Rapid success does not make users feel the fun of the game, while users in the interval of 3 to 5 guess data more rely on the information of ideas and topics constantly updated. The stronger the sense of achievement brought to users by guessing words in this interval, it is in line with the inference and expectation of psychology.

​	