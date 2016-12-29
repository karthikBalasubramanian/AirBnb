AirBnb - Home Away From Home
============================

## The Team

| Name                    |         Contact         |
|-------------------------|:-----------------------:|
| Karthik Balasubramanian | karthikb@andrew.cmu.edu |
| Ankit Goyal             | agoyal3@andrew.cmu.edu  |
| Shuting Zhang           | shutingz@andrew.cmu.edu |

## Demo

[![Project Demo](https://i9.ytimg.com/vi/HJSlw3Oxk-Q/1.jpg?sqp=CITBksMF&rs=AOn4CLDys35SW5ztglzuIpzO_WNwwJEABA)](https://youtu.be/HJSlw3Oxk-Q "Project Demo")


## Code Runbook

In order to run the project code, below mentioned libraries, accounts and api keys are required.

```
Please note that all the API keys, usernames and passwords will be changed
after two weeks from the project submission date to avoid any misuse.
However, official website url and instructions to setup account and generate
api keys are provided below.

In case of any issue, please contact one of the project members at given
email addresses.
```

## Prerequisites
  python installed (tested on v2.7)
  jupyter installed (tested on version 4.2.0)
  anaconda installed (tested on version 1.5.1)

### Additional Library Installations

```
pip install pymongo
pip install us
pip install sklearn
pip install haversine
pip install geocoder
pip install plotly
pip install yelp
pip install gmaps
```
## Database Setup
 Since the Airbnb listings data keep on changing everyday, we took the snapshot of Airbnb Pittsburgh city listings data on 14th November and stored it in the MongoDB database hosted on mlab. Mlab offers MongoDB Database as a service and has an option to create a sandbox account which provides 0.5GB of free hosting space.

 In order to replicate the setup, you need to create a free sandbox account on mlab.

 [MLab Official Website](https://mlab.com/)

 [MLab Official Documentation](http://docs.mlab.com/)

## Steps:
  * Once account is setup, create a database.
  * Add users to the database and grant full access.
  * On DB creation, MongoDB URI will be generated which will allow us to connect to the database and query it from jupyter notebook.
  * Update the connection string in the project code.
  * Execute the data loading scripts which will create required collections in the database and load the data from Airbnb API.


**Please contact us to get the database credentials or schema**
> Note: Code to load data in remote database is commented as data for Pittsburgh is already present in the database.

## 3rd Party API Keys

 We have used few third party APIs to obtain required information. All these APIs require an account to be setup for generating the access key to start using their service. All the services are unpaid  and have restrictions on the number of API calls per day.

| API Name      | Purpose                                                                           | Resource                                                                           |
|---------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Google Maps   | Displays inline maps with location marker and nearby listings.                    | [Google Maps API](https://developers.google.com/maps/documentation/javascript/)    |
| Yelp          | Obtains nearby places of interest for the input location. .                       | [Yelp API](https://www.yelp.com/developers/v2/manage_api_keys)                     |
| Plotly Python | Plotting charts (box plot and histogram) and showing user trend in the World map. | [Plotly docs](https://plot.ly/python/)                                             |
| Walk Score    | Gets walk score for a given location                                              | [Walkscore API](https://www.walkscore.com/professional/api.php)                    |
| Transit Score | Gets transit score for a given location                                           | [Transit Score API](https://www.walkscore.com/professional/public-transit-api.php) |

> Note: Transit score and walk score for the listings was preloaded in CSV file for testing purposes to avoid making API calls again and again. For different city, again the scores will have to be fetched making api calls. Method to make api call is there in the project code.

 All other details are mentioned in the code comments.

[NB Viewer Link](http://nbviewer.jupyter.org/gist/agoyal3/e848a8c6d3bb07efa24249d2a1f8bec9)

#### Additional resources

you can find resources for jupyter widgets [here](https://media.readthedocs.org/pdf/ipywidgets/latest/ipywidgets.pdf)
All other sources and references are cited inline in the notebook as link in markdown cells and as comment in the code blocks.

## Results

Unfortunately, the prediction tool and google maps output was not displayed in the nbviewer so we are attaching the screenshots of the 3 different predictions made using our prediction tool.

**Location:** *8 Mazeroski Way Pittsburgh PA*

**User input**

[![l1in.png](https://s6.postimg.org/hez7qx10h/l1in.png)](https://postimg.org/image/waxqyicf1/)

**Result**

[![l1out.png](https://s6.postimg.org/p8ztcb8td/l1out.png)](https://postimg.org/image/9nihscwv1/)

**Location:** *5600 Fifth Avenue Pittsburgh PA*

**User input**

[![l2in.png](https://s6.postimg.org/a1jtrygyp/l2in.png)](https://postimg.org/image/n5pe4n90d/)

**Result**

[![l2out.png](https://s6.postimg.org/fe8o634v5/l2out.png)](https://postimg.org/image/werkerhwd/)

**Location:** *1608 William Penn Pl Pittsburgh PA*

**User input**

[![l3in.png](https://s6.postimg.org/vdrbpn0wx/l3in.png)](https://postimg.org/image/qf3tb3x3x/)

**Result**

[![l3out.png](https://s6.postimg.org/rvfbt900x/l3out.png)](https://postimg.org/image/6yj3ol1zx/)
