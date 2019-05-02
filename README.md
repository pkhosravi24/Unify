# UNIFY - The Artificially Intelligent Disc Jockey  

![imageedit_1_8964998409](https://user-images.githubusercontent.com/39222728/57004128-55cacb00-6b9a-11e9-9460-8b796f4ba6ec.gif)

Unify is the world's first intelligent disc jockey network and system to seamlessly integrate with a user's music streaming service. Unify is an intelligent system designed to find dynamic solutions from smaller crowds with changing demographics. It is able to design a collaborative and seamlessly effective music system. By gathering the most recently and most played songs from every individual’s Spotify library within range, Unify can determine the most optimum set of songs to be played continuously through an external speaker via Machine Learning-based algorithms and methods. This system consists of a centralized server potential listeners can connect to using their mobile devices with a collaborative application over a wireless network, which is being monitored using an external sniffer. Additionally, every user can choose to provide real-time feedback by suggesting a particular song or by voting the current song positively or negatively. Unify is revolutionary in its industry and can bring individuals closer together through the power of music.

## Abstract

Every individual’s taste in music can be a little different from the next. Often times, it is difficult to gauge a crowd’s music taste in a public setting such as a bar or gym, considering the constant flow happening in and out of the setting. Unify is an intelligent system designed to provide dynamic solutions for crowds with static or changing demographics. The objective of this project is to design a collaborative and seamlessly effective music system. This product is able to gather the most recently and most often played songs from every individual’s Spotify library within range, and determine the most optimum set of songs to be played continuously via Machine Learning-based algorithms and methods. This system consists of a centralized server potential listeners can connect to using their mobile devices with a collaborative application over a wireless network, which is being monitored using an external sniffer. Additionally, every user can choose to provide real-time feedback by suggesting a particular song or by voting the current song positively or negatively. The main advantage of such a system is its adaptiveness to its crowd and listeners taste, a feature that is clearly absent in traditional systems like radios.

## Background 

To design Unify, numerous pltforms were incorporate and working in conjuunction with one another. Extensive research was conducted to learn the following main tools that were used: Python, Java, Android Studio and Machine Learning. 

The main Python library used for handling collected user Spotify data was the user-created Spotipy library, which is a set of classes that allow for easy access of Spotify’s API calls. For the purpose of this project we will use Python to extract user's Spotify  data, execute data analysis, train a Machine Learning algorithm, and establish a server that can communicate with a mobile interface. 

![SpotifyAPI](https://user-images.githubusercontent.com/39222728/57004157-97f40c80-6b9a-11e9-81a2-8d49f5ed068d.JPG)

## Outline 

The approach to achieving our goal will be to first exraplote all the data necessary for our anaylsis. It is important to collect a large set of diverse data. The next step is “cleaning” the data for use. This involve organizing it to make it easy to work with and analyze. Eliminating redundant data can reduce the amount of calculations required during the next step and can greatly increase efficiency. If labels and features are a factor in the situation then these must be organized in a program such as excel. “Training” an algorithm is the next step in the process. There are many algorithms that have been developed and are specific to the needs of the process.


For our purpose we will be using the Decision Matrix algorithm which will be discussed in depth. Once a specific algorithm is chosen the “cleaned” data is fed to the algorithm with a specific target value in mind. This process is known as training a classifier. Once the classifier is trained and ready for use the final step commences. “Scoring” your algorithm entails taking sample data from your set and running it through your classifier. Since the target value of your data is known a test for accuracy may take place. A percentage of the data set is run through the classifier to test it’s prediction accuracy. Each algorithm has specific methods of boosting the accuracy of it’s predictions. This by far is arguably the most important step as it is the actual evaluation of your classifier. Machine Learning is being used in a variety of applications such as medical, robotics, self-driving vehicles and many more. Giving machines the ability to learn the same way humans do with exponentially greater computational speeds the opportunities are unimaginable. 

## Unify's Methodology  

Shown below is a simplified representation of Unify's workflow.

![Untitled Diagram](https://user-images.githubusercontent.com/39222728/57004067-a4c43080-6b99-11e9-92f6-175d00f18af9.png)

To outline this process we will break it down into some steps below:

1. Spotify user's connect their individual Spotify accounts to the Unify Application 

2. The Unify application then uses a TCP socket connection to wirlessly trasnmit data over a secure connection line to a remote HTTP server 

3. This HTTP server then handles our extracted data and feeds it to a local python script waiting and running simultaneously 

4. Onces our Python script establishes our set of songs it uses the Javascript program on the mobile application and Spotify's API to play the individal songs to the users network. 

![UnifySocketProgrammingDiagram](https://user-images.githubusercontent.com/39222728/57004324-2cab3a00-6b9c-11e9-9a2b-4f491930de81.png)

## Extracting The Data
In order to extract a user's Spotify data we need to use a form of API to handle that data. Luckily, Spotify comes with its own publicly available API online with full documentation. 

Although this documentation is provided, it is by no means extensive and even pretty limiited so performing complex analysis on individual msuic tastes will need some extra lines of code to produce. 

Below we can see some example documentation of some of the features this Spotipy API documentation uses as features to ditsinguish a track

![audiofeatures](https://user-images.githubusercontent.com/39222728/57004197-0f29a080-6b9b-11e9-9d81-f95674deaccd.JPG)


Based on the Sptoifiy API documentation, we will choose to extract the following features from each Spotify user's librry of music:

1. Acousticness      6. Loudness
2. Danceability      7. Speechiness
3. Energy            8. Tempo
4. Instrumentalness  9. Valence
5. Livemess          10. Target

Features 1-9 are those found in the Spotify Python documentation, but 'Target' is a dynamic feature added a user continues to use Unify and will be discusssed in detail later on. 

Using the GET function on HTTP below we can extract these specific features and pool them into a CSV file which we can clean.

![Capture](https://user-images.githubusercontent.com/39222728/57004420-e4d8e280-6b9c-11e9-8483-ad3d59d8b8f3.JPG)

We can also perform this with a bit of Python code shown below:


## Cleaning Our Data


Once we have our data in our CSV file, we have our rating for individual songs as such below:

![pastedImage0](https://user-images.githubusercontent.com/39222728/57004494-62045780-6b9d-11e9-808c-c7f989347524.png)


## Establishing An Algorithm

Now that we have a dataset aviaalble for manipulation, we need to choose our predicitve model to train and test. Based on the constraints and objectives of this project the best model to use would be to use the random forest classifier algorithm. This is because this classifier falls under a supervised learning method which requires the data to posses a label of feature from extraction and cleaning. 

The random forest classifier 

## Setting Algorithm Parameters

## Running Tests

## Algortihm Descision Tree

## Mobile Application Deployment

