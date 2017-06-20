# 💏 Coition Diary - Specification

Created by Daniel Tombor<br/>
Created on Jun 19., 2017

## Table of contents
1. [Outline](#outline)
    1. [Purpose of this document](#purpose-of-doc)
    2. [Purpose of the project](#purpose-of-proj)
2. [Go server](#server-spec)
    [Server functionalities](#server-funcs)
3. [iOS client](#mobile-client)
4. [Schedule](#schedule)
5. [Further development opportunities](#furhter-dev)

## <a name="outline"></a>Outline

### <a name="purpose-of-doc"></a>Purpose of this document

This document is not a full functional specification.
It is a guide for the development which we can refer to.
It has to cointain the main purposes, some of the use-cases and functionalities.

### <a name="purpose-of-proj"></a>Purpose of the project

The main purpose of the project is the ability to track & count intercourses.
However, the users may want to know more than just a sum, sometimes they wan to know the date and location, if they single they may want to remember the partner, etc.

Some other extra features are:
* add other users as partners
* display coitions on map
* add note, media and rating
* default settings for easy log

## <a name="server-spec"></a>Go server

The server will be a RESTful API written in Golang and will use PostgreSQL as database.
Its functions are to manage accounts and store and list coitions in the database.
The application can be used without registering, but the server does not implement full syncing logic.

API specification will be available in Swagger.

### <a name="server-funcs"></a>Functionalities

* User management 
    * Sign up/in/out 
    * Forgot pwd
    * Delete acc
    * Profile (name, birthdate, gender, nationality, job title, avatar, relationship status)
    * Privacy handling
* Coition management
    * Add/edit/delete entry
    * List by date/location
    * Filter & search by partners/location/date/rating

## <a name="mobile-client"></a>iOS client

Since the mobile client has only 3 main feature (user management, add & list coitions), a tabbed ui architecture with 5 tabs is a great way to display the records from multiple perspectives. 

Tabs and their functions:
* User profile - auth, profile edit
* Add new entity - quick add, append details
* Display entities on map - clustered map
* List entities chronological - search, filter
* Statistics - weekly, monthly and yearly statistics

The main functions are available without having to sing up, but this way entries won't be uploaded to the server.
If the users would like to register later, their records will be uploaded to the server only from one of their devices.

Intercourse details: When selecting a partner, the user has to know the username of the partner, since the app won't list the users because of privacy issues. Or the user can just type in a name without linking it to anouther user.
Only 3 media items can be uploaded to a coition and the videos are restricted to a length of maximum 15s.

## <a name="schedule"></a>Schedule

* Jun 20. - API Specification
* Jun 23. - Application wireframe + Design
* Jun 30. - iOS app with offline storage
* Jul 3. - Jul 30. - Developer is on holiday
* Aug 8. - Server side
* Aug 16. - iOS App networking -> store data on server

## <a name="furhter-dev"></a>Further development opportunities

**New features**

* Social login (Fb, Twitter, Google)
* Add Kama sutra
* Wish list (location, partner)
* secret intercourse

**Gamification**

* Number of countries/cities
* Public domain
* Strong couple award
* Partner abc
* Country abc
* Number of logs

**Statistics**

Statistics by number of intercourses, rating, frequency

* Gender war
* Countries bottle
* Distribution by age 
* Pleasure of jobs
* In a relationship vs Singles


👉👌