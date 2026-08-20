# Product Requirements

## Goal

Build a web application for Bars, Restaurants or Lounges (and similars) to publish their events and daily menus.

## Problem

Today, event flyers and daily menus are mostly shared in social media like Instagram or Facebook, and a post can be easily missed or forgoten. Also, potential clients may not follow certain pages so they are not updated with that content.

## Solution

A platform that shows flyers and daily menus, in a historical way, and indexes its content so users can easily search or filter by keywords.

The content is published by submitting a typical picture file (PNG, JPEG, etc) which is then processed by an AI vision model that retrieves all text data. The file submission can be done by chat (Instagram Direct or Facebook Messenger) or in the web page.

Page visitors are presented with submitted pictures in their prefered way: calendar, grid/masonry layout or cards. They can also filter by keywords, content type, location or date.

The long term solution will provide insights to publishers, like their content audience or what visitors are looking for.

## Users

### Publisher

Who submits content to the platform, edit or remove it.  
The user must be logged in to perform the following operations.  
The account is created by using Facebook or Instagram SSO.

### Visitor

Who navigates in the platform to search for daily menus or events.  
Can report abusive or incorrect content.

### Moderator

Who reviews reports and blocks content.  
Can block Publisher users.  
Can submit content to the platform, edit or remove it.  
The user must be logged in to perform these operations.  
Possibly accesses throught a administration application.

## Core functionality

1. File submission - when a file is submitted is processed by an AI vision model, which must retrieve all possible and relevant text. Pictures not relevant for the platform or that show content abuse, do not proceed and are placed in a separate folder.
2. Publisher can submit a picture file in the platform, by accessing the logged in page or by chatting with the platform profile in Instagram or Facebook.
2. Content report - a Visitor can report the content by clicking in a options button associated to it. As the content receives more and more reports, it gets higher evaluation in the Moderator panel.
3. Publisher block - the Moderator can block (or unblock) a Publisher from a list of registered users.
4. Content moderation - The Moderator can see a list of reported content and hide it from public.
5. Content visualization - any Visitor can see the published content (marked as public), switch between layouts and filter entries.
6. Content edition - a Publisher or Moderator can edit indexed data that was wrongly interpreted by the AI model.

## Non-functional requirements

- Web application
- Authentication required
- Supabase as database and authentication
