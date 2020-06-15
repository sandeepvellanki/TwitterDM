# TwitterDM

The Jupyter notebook that acts as a local application that can send Direct Messages (DMs) to all of your followers based on the keywords in their bio and/or count of followers they have. It allows you to update your followers list with new followers whenever you want to and add these to the list of followers whom you want to send automated DMs to.

This works without any issues for twitter accounts with huge followers. 
(tested with an account having ~450k followers, but would work for even bigger accounts as well.)

## First time load times:
1. With accounts less than 75k followers: ~20-25 mins
2. With accounts less than 150k followers: 40-45 mins
3. With accounts less than 225k followers: 60-65 mins
4. With accounts less then 300k followers: 80-85 mins
and so on......

## Prerequisites:
1. Jupyter notebook server
2. Pandas
3. Tweepy
4. and Seaborn python packages

# How to:
1. Download the 'Twitter DM application.ipynb' file to a local folder.
2. Pip install all prerequisite packages.
3. Update the 'Inputs:' cell on the notebook with your parameters.
4. Keep the 'FirstLoadFlag' as 'True' for the first load and changes to 'False' for subsequent runs.

# Benefits:
1. Works across windows and MAC as it is a jupyter notebook
2. Works locally, with flatfiles as backend tables.
    1. The Twitter API keys need not be shared with anyone
    2. No worry of your followers data being with a 3rd party
3. Ability to choose the exact 1000 followers to send the DMs on any given day based on filters you provide like follower count, keywords in bios, exculded list of followers and so on.
4. Easy to backup data.
5. Visually check the following counts:
      1. Followers count at the precise moment
      2. Followers count that have been loaded in local tables
      3. Followers that meet the filter criteria
      4. Followers for whom we sent out DMs (that succeeded and failed)
      5. Followers for whome we can still send the DMS
6. Update tables with new followers and thier meta data with a click of a button.

# Screenshots:

### Daily status of DMs sent:

![Sample status chart](https://github.com/sandeepvellanki/TwitterDM/blob/master/Sample%20status%20chart.png?raw=true)

### Screenshot of meta data of followers being stored:

![meta data](https://github.com/sandeepvellanki/TwitterDM/blob/master/meta%20data%20stored.png?raw=true)

### Screenshot of time to pull 220k records:

![220k records](https://github.com/sandeepvellanki/TwitterDM/blob/master/more%20than%20220k%20records%20pulled%20in%20less%20than%2030%20mins.PNG?raw=true)

### Screenshots of DMs sent:

![DMsent1](https://github.com/sandeepvellanki/TwitterDM/blob/master/DMsentscreenshot0.png?raw=true)

![DMsent2](https://github.com/sandeepvellanki/TwitterDM/blob/master/DMsentscreenshots2.jpg?raw=true)
