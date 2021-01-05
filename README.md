# Facebook Messegener Visualization

This website/code allows you to see the number of messages you send and receive, when, to whom, etc.. If you have always been curious about your Facebook messages history, you should find some answers here.


### Running It

1. To serve it locally run: `python -m SimpleHTTPServer 8000` in your terminal
2. Open `https://localhost:8000` in a browser
3. Hit the top right button `Explore your own data` to import your own data
4. On Chrome and other browsers it may say you're downloading/uploading data, when in reality everything is happening locally on the browser. In order to make sure this is true, you can also turn off your wifi and try this.
5. Scroll through the stats on the right and hit the color wheels to see changes in how the at a is shown.
6. To Zoom In/Out make sure to use overview charts parallel to the x and y axis and drag the zones so that you can focus on a certain time period.



### General Design

The initial dataset is from a sample dataset allowing users to explore this visualization. In addition you can explore your own data with the button at the top right button. Import the messages folder from the json version of your facebook data.

Chrome may say you're uploading/downloading files, but all the files are kept locally.

What is represented here is quite simple : one point corresponds to one message sent or received. The top of the graph represents the beginning of the day (12:01 a.m.) and the bottom of the graph represents the end of the day (11:59 p.m.).

Once you have downloaded your Facebook History,  click on "Explore your own data" and load the ``message`` directory of the archive.


## Brush and Zoom



On the left-hand side of the screen, and at the bottom you can find sliders that allow you to select the hours and the date you want. Use it to zoom and select only the messages between a certain timeframe and received/sent between 2am and 6pm for example.
The blue area on the left represents the density of messages depending on the time of the day, whereas the blue area on the bottom represents the density of message depending on the date.
Those densities of messages vary when you select filters. For example if you select a conversation, you may see something like this:

<img src="" height="25%" width="25%"> 

## Filters

On the right-hand side, you can find some histograms :
- Day of the week
- Sent/Received
- Top 10 conversations
- Top 10 senders
- Length of messages

If you click on any bar of these bar charts, it filters all the data and only keeps the one selected. You can apply multiple filters, and explore some interesting stuff this way.
For instance, if you click on one particular conversation, then the top 10 senders histogram will display who speaks the most **for this conversation**. This is interesting for group conversations.

If you clicked everywhere on the filters and you want to reset everything, just click on **"Reset All Filters"** on the top right.

<img src="" height="25%" width="25%"> 

## Message Displayer

In the bottom right-hand corner, you can see the **Message Displayer**. When you mouse over the dots on the central pane, the message under the mouse is displayed here, and you can see basic information:
- The date of the message
- The sender
- The message
