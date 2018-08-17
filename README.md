# BrowserHistory Module
---

browserhistory is a simple Python module that extracts browsers's history from a user's local computer. It supports following browsers: Firefox, Google Chrome, and Safari. It supports the OS Platforms: Linux, MacOS, and Windows.

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
>>> import browserhistory
>>> browserhistory_ex = get_browserhistory()
>>> browserhistory_ex.keys()
>>> dict_keys(['safari', 'chrome', 'firefox'])
>>> browserhistory_ex['safari'][0]
>>> ('https://mail.google.com', 'Mail', '2018-08-14 08:27:26')
```

### The Description of browserhistory
---

```
NAME
    browserhistory

FUNCTIONS
    get_browserhistory() -> dict
        Get the user's browsers history by using sqlite3 module to connect to the dabases.
        It returns a dictionary: its key is a name of browser in str and its value is a list of
        tuples, each tuple contains four elements, including url, title, and visited_time. 
        
        Example
        -------
        >>> import browserhistory
        >>> browserhistory_ex = get_browserhistory()
        >>> browserhistory_ex.keys()
        >>> dict_keys(['safari', 'chrome', 'firefox'])
        >>> browserhistory_ex['safari'][0]
        >>> ('https://mail.google.com', 'Mail', '2018-08-14 08:27:26')
    
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