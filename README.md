# JP-Morgan-Chase-Forage
 Establishing financial data feeds and visualization for traders using Perspective framework and tools.
 
 ### Proof of Work
 ![](https://raw.githubusercontent.com/Grv-Singh/JP-Morgan-Chase-Forage/main/Screenshot%202020-10-02%20124524.jpg)
 <h2>How to Run</h2>
To start the server, run

	python server3.py

this will create random market called 'test.csv' in working directory if one does not already exist.

If encounter an issue with `datautil.parser`, run this command: 

	pip install python-dateutil


To start the example client, run:

	python client3.py

To unit test the example client, run:
	python client_test.py

<h2>How to request from the server using curl</h2>
<!--See also [client.py](https://github.com/texodus/exchange_simulator/blob/master/client.py)-->
### Query:

	$ curl 'http://localhost:8080/query?id=1'
	{"id": "1", "top_ask": {"price": 129.18, "size": 70}, "timestamp": "2016-08-06 12:32:11.821574", "top_bid": {"price": 128.79, "size": 61}}

<h2 id="task"> Task Overview </h2>
<p>JP Morgan Chase's frameworks and tools
Implement JP Morgan Chase’s Perspective open source code in preparation for data visualization</p>
<p> <b>Aim:</b>Use Perspective, to make a graph that updates manually, and make it work with the code from previous learning such that it now updates automatically by continuously requesting from the server application</p>

<ol>
	<li>[goal-a] In the client application, observe that when new data feed is retrieved on clicking the 'Start Streaming Data' button, the previous entry is re-entered into the table. Update the application so that the table does not have duplicated entries</li>
	<li>[goal-b] We also want the react app to keep continuosly requesting data from the python server. Currently, the data feed is called only once every time the 'Start Streaming' button is clicked. Change the application to continuously query the datafeed every 100ms when the 'Start Streaming' is clicked.</li>
	<li>[goal-c] Currently, the Perspective element only shows the data in table view after the data loads. Add Perspective configurations so that when the data is loaded, it shows the historical data of ask_price ABC in the Y line chart.</li>
</ol>

<h2 id="installation" >Set up / Installation</h2>
<p>In order to get the server and client application code working on a machine, run `npm install & npm build`

### How to Run

<p>Start the data feed server by running the python server.</p> 
<p>Make sure terminal / command line is in the repository first before doing any of this.</p>
<code> python datafeed/server3.py </code>

If encounter an issue with `datautil.parser`, run this command: 

	pip install python-dateutil

Run <code>npm install && npm start</code> to start the React application.

Open http://localhost:3000 to view the app in the browser. The page will reload if you make edits.
