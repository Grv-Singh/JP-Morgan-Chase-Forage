<br>
<p align="center">

<h1> Introduction</h1> 
<p>Try out what real work is like in the technology team at JP Morgan Chase & Co. Fast track to the tech team with our work.</p>

<h2 id="task">Task Overview </h2>
<p>Interfacing with a stock price data feed and set up our system for analysis of the data</p>
<p> <b>Aim:</b> We want to process the data feed of stock A and stock B’s price to enable us to analyse when trading for the stock should occur.</p>

<h2 id="installation" >Set up / Installation</h2>

<p>In order to get the server and client application code working on a machine. Install NodeJS & run `npm install & npm build`

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
Query:

	$ curl 'http://localhost:8080/query?id=1'
	{"id": "1", "top_ask": {"price": 129.18, "size": 70}, "timestamp": "2016-08-06 12:32:11.821574", "top_bid": {"price": 128.79, "size": 61}}

