# FacebookPoster

## Introduction

This repo contains a facebook group posting automation bot. This is useful if you are trying post to many groups quickly using google chrome and selenium. It has a user interface that you can login through. It has two methods of posting.

## Usage

## First Method (scrape groups)
> ```console
> $ python FacebookGroupPoster.py
> ``` 

This will ask for your login information and give you the option to load data from an excel file. For this method dont load data and login with your credentials. This will open a Google Chrome window and login into facebook. It will then find all groups that your account is a member of and open a new window with each group. You are then able to check which groups you would like to post to and fill in what each post will be.

## Second Method (Preset groups)
> ```console
> $ python FacebookGroupPoster.py
> ```

This will ask for your login information again with the option to load data. When load data option is chosen, an excel file is loaded. The excel file allows posts to become more complex and personalized.

# How to use excel file

The following table shows how the the excel file is set up for this personalization. You must compile the group's links into the url column (with mbasic added to the front of the url) as well as the name of the group. Inside the post you must include the structure of your post with curly brackets inclosing the column name that you want to replace. This makes using the same post for each group with specific names easy to generalize to many posts.

| group      | url                                                          | post                                                                                                           | entry0 | entry1            |
|------------|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------|-------------------|
| TestGroup1 | https://mbasic.facebook.com/groups/567925213654496?refid=27  | this is a loading test post for {entry0} and to see that it properly adds the other entries like {entry1}      | GROUP1 | this one here pal |
| TestGroup2 | https://mbasic.facebook.com/groups/2152468034787683?refid=27 | this is also a loading test post for {entry0} and to see that it properly adds the other entries like {entry1} | GROUP2 | or even this one  |


## Ryan's - TODO

Feature List:

#####can create “group list”
- name list
- enter fb credentials
- return selectable list of groups
- select groups to add
- save list to DB

#####can start a “promotion” instance
- enter FB URL
- select group list
- Add FB event column in DB for posting status
- Share event to group via selenium
- Check if posted/ sent to admin
- via fb page check or activity log

#####update groups
- checks fb groups and reported if any new groups were added, renamed (verified by url), or deleted
- option to add, rename, delete

#####can have various prompt tables with associated list of vars
- for example a “super stacked” prompt would have a [group descriptor] and a [location descriptor] that is different for each group
- every time a new group is added to the list, you hav the option of updating its entries, if it exists within a prompt table. Or if it doesn’t, you have the option to add it into the prompt table
