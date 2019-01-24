> This repository is non-functional at the moment. Once this note has been removed, you can download it and use it to quickly get InstaPy working on your system. Please have a little bit more patience.

<img src="https://i.imgur.com/sJzfZsL.jpg" width="150" align="right">

# Instapy Quickstart
If you want to get a sophisticated and full introduction to InstaPy, we recommend taking the video course   
**[Full official guide to InstaPy on Udemy]()**

### Installation
Using this repository, you will be able to install and use InstaPy with only very few steps.

1. Download the zip of this repository by clicking on the green button in the upper right corner `Clone or download`.
1. Unzip the folder and open the installation folder
1. Double click the installation file for your system
1. If you missed any installation it will tell you what you have to install
1. Once successfully installed you can edit the quickstart file or use any of the template files from the quickstart_templates folder
1. Insert your username and password and modify anything you want. Make use of the **[comprehensive documentation](https://github.com/timgrossmann/InstaPy)**.
1. ... (TODO - best way to start the quickstart file)


#### Basic quickstart file 

```python
""" Quickstart script for InstaPy usage """
# imports
from instapy import InstaPy
from instapy import smart_run

# login credentials
insta_username = ''
insta_password = ''

# get an InstaPy session!
# set headless_browser=True to run InstaPy in the background
session = InstaPy(username=insta_username,
                  password=insta_password,
                  headless_browser=False)

with smart_run(session):
    """ Activity flow """
    # general settings
    session.set_relationship_bounds(enabled=True,
                                    delimit_by_numbers=True,
                                    max_followers=4590,
                                    min_followers=45,
                                    min_following=77)

    session.set_dont_include(["friend1", "friend2", "friend3"])
    session.set_dont_like(["pizza", "#store"])

    # activity
    session.like_by_tags(["natgeo"], amount=10)
```
---

#### Already used InstaPy before `pip install instapy`?
If you've used InstaPy before the update to PyPi that allows installing with `pip install instapy`, you have to move your database and log files into the new workspace directory.   
[**Check out this very short guide on what to do!**]()

---

#### Encountering an issue while installing?
If you should encounter any problem with the installation, please use the main repository [InstaPy](https://github.com/timgrossmann/InstaPy) to report the issue instead of this repository.


###### Have fun & stay responsible!
