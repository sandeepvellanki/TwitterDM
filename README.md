For any clarification or demo, send email to vellanki.sandeep@gmail.com.
Will respond to your request as soon as I can.

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
1. Jupyter notebook

# How to:
1. Download the 'Twitter DM application.ipynb' file to a local folder.
2. Fire up Jupyter notebook application and open the above file.
3. Update the Inputs cell. Most of the defaults work.
![Inputs](https://github.com/sandeepvellanki/TwitterDM/blob/master/Inputs.PNG?raw=true)
4. Run each cell one after other (Cntlr+Enter to run each cell).
5. 'Install and load ..' cell: installs all prerequsite packages and imports them
6. 'Backup data' cell: Backs the data as losing it mean running time consuming intial loads.
7. 'Status Visual' cell: Give a visual representation of followers count, DB status and DMS sent etc. See the screenshot below:
![Sample status chart](https://github.com/sandeepvellanki/TwitterDM/blob/master/Sample%20status%20chart.png?raw=true)
8. 'Update Follower IDS list' cell: Updates any new followers from last run. Intial run will load all follower IDs in Ids table.
![220k records](https://github.com/sandeepvellanki/TwitterDM/blob/master/more%20than%20220k%20records%20pulled%20in%20less%20than%2030%20mins.PNG?raw=true)
9. 'Update metadata' cell: Updates metadata like bio, followers count and so on for the followers.
![meta data](https://github.com/sandeepvellanki/TwitterDM/blob/master/meta%20data%20stored.png?raw=true)
10. 'Send DMs for today' cell: Filters, Sorts, choose and sends the number of DMs you want to send on a particular day.
![DMsent1](https://github.com/sandeepvellanki/TwitterDM/blob/master/DMsentscreenshot0.png?raw=true)

![DMsent2](https://github.com/sandeepvellanki/TwitterDM/blob/master/DMsentscreenshots2.jpg?raw=true)

# Benefits:
1. Works across windows and MAC as it is a jupyter notebook
2. Works locally, with flatfiles as backend tables. (can be updated to SQLite, but flatfiles seem just fine)
    1. The Twitter API keys need not be shared with anyone
    2. No worry of your followers data being with a 3rd party
3. Ability to choose the N followers to send the DMs on any given day based on filters you provide like follower count, keywords in bios, exculded list of followers and so on.
4. Easy to backup data.
5. Visually check the following counts:
      1. Followers count at the precise moment
      2. Followers count that have been loaded in local tables
      3. Followers that meet the filter criteria
      4. Followers for whom we sent out DMs (that succeeded and failed)
      5. Followers for whome we can still send the DMS
6. Update tables with new followers and thier meta data with a click of a button.

# Planned Updates:
A Saas tool as follows:
1. Create a frontend UI that works on twitter login and takes in inputs via a form. Same inputs as above.
2. Takes to a dashboard that shows the status of your sent DMs and other related metrics.
3. Ability to schdule DMs.
