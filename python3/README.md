## Disclaimer
The code examples are to be used in testing *only* (!). They are provided as is
without any warranty of any kind, see `LICENSE` for more information.

_Note that all the JSON objects end with newline.  As such you need to listen
and read from the buffer when a full object has been transferred_

## Requirements
* Register an account to get access to the
  [forums](https://api.test.nordnet.se) and the test system
  [here](https://api.test.nordnet.se/account/register). Your username
  and password are needed to authenticated to the API
* Read about the [test system](
  https://api.test.nordnet.se/projects/api/wiki/Test_system) to
  learn about the delimitations and how the test market works
* [Python 3](https://www.python.org/downloads/) and
  [pip](https://pip.pypa.io/en/stable/installing/) installed

## Install and run
1. Download the `nordnet/next-api-v2-examples` repo
2. Run and provide your username and password as arguments
```
cd python3
pip3 install -r requirements.txt
./test_program.py [insert username] [insert password]
```
Running the test program should output something that looks similar to the following example output
```json
{
    "message": "",
    "system_running": true,
    "timestamp": 1528730480984,
    "valid_version": true
}
>> Response from logging into the session
{
    "country": "SE",
    "environment": "exttest",
    "expires_in": 300,
    "private_feed": {
        "encrypted": true,
        "hostname": "priv.api.test.nordnet.se",
        "port": 443
    },
    "public_feed": {
        "encrypted": true,
        "hostname": "pub.api.test.nordnet.se",
        "port": 443
    },
    "session_key": "01ba12bfd3244e63ad52c1731a54e2f3f98f949e"
}
>> Response from Price Feed
{
    "data": {
        "ask": 0.0,
        "ask_volume": 0,
        "bid": 65.0,
        "bid_volume": 26200,
        "close": 64.36,
        "high": 0.0,
        "i": "101",
        "last": 0.0,
        "last_volume": 0,
        "low": 0.0,
        "m": 11,
        "open": 0.0,
        "tick_timestamp": 1528726500001,
        "trade_timestamp": 1528726500001,
        "turnover": 0.0,
        "turnover_volume": 0,
        "vwap": 64.19
    },
    "type": "price"
}
```

## Common issues
* SyntaxError: check that your Python version is 3 or higher
* NEXT\_LOGIN\_INVALID\_LOGIN\_PARAMETER: double-check your [password](https://api.test.nordnet.se/login)
* NEXT_LOGIN_INVALID_TIMESTAMP: check your system clock to see if it is up to date

## Questions
If you have technical questions then,
1. Check out the code, it is documented
2. Read the [documentation](https://api.test.nordnet.se/api-docs/index.html)
3. Ask questions in the [forum](https://api.test.nordnet.se/projects/api/boards)

Otherwise, contact Nordnet trading support with the contact details provided
[here](https://api.test.nordnet.se)
