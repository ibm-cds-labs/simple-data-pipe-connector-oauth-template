:no_entry_sign: This project is no longer maintained. 

> Hey there! So you want to build your own Simple Data Pipe connector? [Start here](https://github.com/ibm-cds-labs/simple-data-pipe-connector-oauth-template/wiki/How-to-Build-a-Simple-Data-Pipe-Connector).

***


# Simple Data Pipe OAuth sample connector 

This [Simple Data Pipe](https://developer.ibm.com/clouddataservices/simple-data-pipe/) connector template illustrates how to 

* define OAuth connectivity for a cloud data source,
* load a static set of data sets (2016 election speeches) and
* store the results in Cloudant.

### Pre-requisites

##### General 
 This sample connector illustrates how to implement OAuth connectvity for a cloud data source, such as [reddit](http://www.reddit.com).
 A valid reddit user id is required to create and run a Simple Data pipe that fetches a small data set for illustrative purposes. 

##### Deploy the Simple Data Pipe

 [Deploy the Simple Data Pipe in Bluemix](https://github.com/ibm-cds-labs/simple-data-pipe) using the Deploy to Bluemix button or manually.

##### Services

This connector does not require any additional Bluemix service.

##### Install the Simple Data Pipe connector OAuth boilerplate

  When you [follow these steps to install this connector](https://github.com/ibm-cds-labs/simple-data-pipe/wiki/Installing-a-Simple-Data-Pipe-Connector), add the following line to the dependencies list in the `package.json` file: 

```
"simple-data-pipe-connector-oauth-template": "git://github.com/ibm-cds-labs/simple-data-pipe-connector-oauth-template.git",
```

##### Enable OAuth support and collect connectivity information

 You need to register the Simple Data Pipe application before you can use it to load data.
 1. Open the [reddit](http.reddit.com) web page and log in.
 2. Click **Preferences** and select the **apps** tab.
 3. **Create another app...**
 4. Assign an application **name** and enter an optional **description**.
 5. As _redirect URL_ enter `https://<simple-data-...mybluemix.net>/auth/passport/callback`.
   > Replace `<simple-data-...mybluemix.net>` with the fully qualified host name of your Simple Data Pipe application on Bluemix.

 6. Click **create app**.
 7. Copy the application id displayed under your application name (e.g. vv5ulJR3...20Q) and the secret (e.g. j60....CFSyAmSY).


### Using the Simple Data Pipe OAuth sample connector 

To configure and run a pipe

1. Open the Simple Data Pipe web console.
2. Select __Create A New Pipe__.
3. Select __Sample OAuth Data Source__ for the __Type__ when creating a new pipe  
4. In the _Connect_ page, enter the _application id_ and _secret_ from the reddit app preferences page. 
5. Select the data set (or data sets) to be loaded.
6. Schedule or run the data pipe now.

#### License 

Copyright [2016] IBM Cloud Data Services

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
