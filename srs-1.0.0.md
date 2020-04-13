# 1. Introduction
This is an SRS for version 1.0.0 of the offical CA app.

## 1.1 Purpose
The purpose of the app is to make it easier for people to find meetings and in the furtue all and any CA related information.

## 1.2 Intended Audience
The entire document is intended for memebers of the development subcommittee but parts of it may also interest other stakeholders on the *parentcommittee* and members of CA who are curious about the committees work and vision.

## 1.3 Intended Use
This document is primarily intended to serve as a SRS for the development subcommittee to CAWSITC but everything before the *System Features and Requirments* section can be read by anyone interested in the vision of the CAWSITCs development efforts for the frontend web plugin.

## 1.4 Scope

The users will be able to quickly find a meeting based on their current location or a set of search parameters. They should also be able to get a list of all meetings and contact information for their area.

The API from which the app will retrive this information can be found here [meeting API](https://github.com/CAWSCIT/caws-api).

## 1.5 Definitions and Acronyms
CA - Cocaine Anonymous

SRS - Software Requirment Specification

CAWSITC - Cocaine Anonymous World Service IT Committee

CAWS - Cocaine Anonymous World Service

# 2. Overall Description

## 2.1 User Needs
Our primary users are newcommers. The most crucial ojective of this project is to simplify finding a meeting for those who still suffer. Considering the state in which some of us came to these rooms, this needs to be a very simple task.

Our secondary users are exsting members who are either finding a new meeting in their own area or perhaps looking for one when traveling.

## 2.2 Assumptions and Dependencies

We assume that we will have access to Google Maps API keys and that we are enrolled in the Apple Developer program.
We also assume the existence of our [meeting API](https://github.com/CAWSCIT/caws-api). Most importantly we assume that there are people willing to do the work of building this masterpiece.

# 3. System Features and Requirements

Notifications?

This section describes the technical requirments for the app.

## 3.1 Functional Requirements
As a user you will have to ability to search for meetings by a combination of the following.
- [x] Meeting name
- [x] Address
- [x] Tags (A way for each area to categorize meetings)
- [x] Weekdays

Or simply by

- [x] Current location (So far no support for combining this with the other parameters exist in the backend)

Upon searching the user will be presented with the results containing the meetings that match their search. The results will display the meeting name, description, day, time, tags, address and an embedded Google map (which they can easily click to open Google Maps).

A user will be able to find the contact details for the area they are in. This includes hotline and email.
This will be implmented by querying the API which will list areas in order of proximity by the closest group to the users current position for each area (*This is not implemneted in the API but is WIP*).

A user should also be able to send suggestions and or bug reports to the app dev team. This will be implemented by leeting users send an email to `itcommittee@ca.org` (or another similar email). This can be as simple as leeting the user click on something that opens their own mail client.

*Discussion: Would it be good to be able to just list all meetings for an area instead of searching?*

## 3.2 External Interface Requirements
The plugin will have two external dependencies. The version 1.0.0 or 2.0.0 (*Discussion*) of the CAWSITC Meeting API and the Google Maps Embed API.

## 3.3 System Features

## 3.4 Nonfunctional Requirements

__Language localisation__
Will not be done for the MVP. The app is in english.

