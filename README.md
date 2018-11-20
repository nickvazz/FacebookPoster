# FacebookPoster

## Introduction

This repo contains a facebook group posting automation bot. This is useful if you are trying post to many groups quickly using google chrome and selenium. It has a user interface that you can login through. It has two methods of posting.

## Usage

First Method (scrape groups)
> ```console
> $ python FacebookGroupPoster.py
> ``` 

This will ask for your login information and give you the option to load data from an excel file. For this method dont load data and login with your credentials. This will open a Google Chrome window and login into facebook. It will then find all groups that your account is a member of and open a new window with each group. You are then able to check which groups you would like to post to and fill in what each post will be.


