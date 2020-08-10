# About BulkIPRepCheck
> BulkIPRepCheck is a python tool designed to extract the Reputation of IPs in bulk. The tool inputs massive amounts of IPs and queries multiple IP Reputation databases and gives a Malicious or Not-Malicious status for each IP. The tool has support for the following IP Reputation databases:
* IBM XFORCE (Requires user API key)
* Abuse.ch
* Alientvault
* CISCO Talos

## General info
There are many tools which query IP Reputations individually but I could not find any tool to do this in Bulk for many IPs. So, created this tool to query multiple databases for multiple IPs recursively and quickly.

## Screenshots
![Example screenshot](./img/screenshot.png)

## Installation
1. Clone the repository:
```
$ git clone https://github.com/tushRana/BulkIPRepCheck.git
$ cd BulkIPRepCheck
```
2. Create python environment and activate the environment:
```
python3 -m venv env
source env/bin/activate
```
3. Install dependencies:
pip install -r requirements.txt

### Dependencies:
* BulkIPRepCheck currently supports only ***Python 3***.
* BulkIPRepCheck depends on the `pandas`, `openpyxl` and `requests` python modules.

## Usage

Short Form    | Long Form     | Description
------------- | ------------- |-------------
-f            | --file        | Input file containing IPs
-s            | --sources     | Specify a comma-separated list of sources to query
-sL           | --list_sources| List all supported sources
-o            | --output      | Save the results to excel file
-h            | --help        | show the help message and exit

### Examples
* To query all supported sources against IPs in an excel file:
`python main.py -f filename.xlsx -o output.xlsx`
* To list all supported sources:
`python main.py -sL`
* To query specific sources against IPs in an excel file:
`python main.py -f filename.xlsx -s xforce,alienvault -o output.xlsx`
* To query all supported sources against IPs in a text file file:
`python main.py -f filename.txt -o output.xlsx`

To-do list:
* Adding more sources to query.

## Status
Project is: _in progress_

#### Contact
Created by [@oldsoul](https://twitter.com/rana_tushr) - feel free to contact me!
