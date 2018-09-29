# MAQUI: Interweaving Queries and Pattern Mining for Recursive Event Sequence Exploration

MAQUI is web application that supports expressive querying and flexible pattern mining for exploring event sequence data. It is a collaborative effort between researchers at Georgia Tech and Adobe Research. For more information about the project, please refer to our paper at [IEEE VIS 2018](http://ieeevis.org/year/2018/welcome)):

*[MAQUI: Interweaving Queries and Pattern Mining for Recursive Event Sequence Exploration](https://terrancelaw.github.io/publications/MAQUI_vast18.pdf)  
[Po-Ming Law](https://terrancelaw.github.io), [Zhicheng Liu](http://www.zcliu.org), [Sana Malik](http://www.sanamalik.com), and [Rahul C. Basole](http://entsci.gatech.edu/basole/)  
IEEE Transactions on Visualization and Computer Graphics ([IEEE VIS 2018](http://ieeevis.org/year/2018/welcome))*

## System Demo

[This video](https://youtu.be/17jqGbyWm2w) walks you through the basic funcationality of MAQUI. [This video](https://youtu.be/UhlBhDrejK0) demonstrates how MAQUI can be used for exploring the [Foursquare dataset](https://sites.google.com/site/yangdingqi/home/foursquare-dataset).

## Running the System

You need to install Python 3 (rather than Python 2), Java, and [Flask](http://flask.pocoo.org) in order to run the system. Chrome is recommended as the system was only tested with Chrome.

The following are the instructions and commands to run the system using a Mac:

1. Clone the repository using Terminal.

```
git clone https://github.com/terrancelaw/MAQUI.git
```

2. Go to the folder named "MAQUI".

```
cd MAQUI
```

3. Go to the folder named "server".

```
cd server
```

4. Start the Python server (you need Python3 for the system to work properly).

```
python server.py
```

5. Visit http://localhost:5000/ using Chrome.

## Exploring Your Own Data

MAQUI assumes each event to have multiple attributes. Attributes associated with an event are called event attributes. MAQUI further assumes each event sequence to have multiple attributes. These attributes are called record attributes.

For example, a patient (male, 38 year old) may went through a series of events in his visit to an emergency department: *Arrival*, *Triage Start*, *Triage End***, *Exit*. The event attribute for the first event is ***Event=Arrival***. The record attributes are ***Gender=Male***, and ***Age=38***. 

Although in above example, each event only has one attribute, MAQUI can handle event sequence data in which an event has multiple attributes. It also works for datasets that do not contain record attributes.

Events and record attributes are stored respectively in [event.csv](https://github.com/terrancelaw/MAQUI/blob/master/data/events.csv) and [recordAttributes.csv](https://github.com/terrancelaw/MAQUI/blob/master/data/recordAttributes.csv) in the [data folder](https://github.com/terrancelaw/MAQUI/tree/master/data). For [event.csv](https://github.com/terrancelaw/MAQUI/blob/master/data/events.csv), the header should be in the format "ID,time,[a list of event attributes]". Time should be in the format "2015-05-01 00:43:28". For [recordAttributes.csv](https://github.com/terrancelaw/MAQUI/blob/master/data/recordAttributes.csv), the header should be "ID,[a list of record attributes]". The character "=" should not appear in any attribute values.

## Contact

Please contact [Terrance Law](https://terrancelaw.github.io) for any comments and issues running the system.