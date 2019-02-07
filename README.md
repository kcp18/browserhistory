# BrowserHistory Module

browserhistory is a simple Python module that extracts browser history from a user's local computer and writes the data to csv files.

Platforms: Linux, MacOS, and Windows.
Suported Browsers: Firefox, Google Chrome, and Safari. 

## Installation
```sh
$ python3 -m pip install browserhistory
```

or 

```sh
$ git clone https://github.com/kcp18/browserhistory
```

## Overview
### Functions:
- get_browserhistory() -> dict
- get_database_paths() -> dict
- get_username() -> str
- write_browserhistory_csv() -> None


#### Example:
```python
Example
=======
>>> import browserhistory as bh
>>> dict_obj = bh.get_browserhistory()
>>> dict_obj.keys()
>>> dict_keys(['safari', 'chrome', 'firefox'])
>>> dict_obj['safari'][0]
>>> ('https://mail.google.com', 'Mail', '2018-08-14 08:27:26')
# Write the data to csv files in the current working directory.
# safari_browserhistory.csv, chrome_browserhistory.csv, and firefox_browerhistory.csv.
>>> bh.write_browserhistory_csv()
# Create csv files that contain broswer history
```

### The Description of browserhistory

```
NAME

    browserhistory

FUNCTIONS

    get_browserhistory() -> dict
        Get the user's browser history by using sqlite3 module to connect to the dabase.
        It returns a dictionary: its key is a name of browser in str and its value is a list of
        tuples, each tuple contains four elements, including url, title, and visited_time. 
    
    get_database_paths() -> dict
        Get paths to the database of browsers and store them in a dictionary.
        It returns a dictionary: its key is the name of browser in str and its value is the path to database in str.
    
    get_username() -> str
        Get username based on their local computers
    
    write_browserhistory_csv() -> None
        It writes csv files that contain the browser history in
        the current working directory. It will writes csv files base on 
        the name of browsers the program detects.
```

### Issue Report 


If you have any questions or find bugs in the module,  
please report the issues/questions at the follwing address.

- https://github.com/kcp18/browserhistory/issues


