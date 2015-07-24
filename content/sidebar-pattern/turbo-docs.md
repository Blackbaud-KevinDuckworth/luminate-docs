---
layout: layout-sidebar
order: 20
name: Turbo Docs
description: render side navigation on the left hand side of the page using H2 tags
published: true
showInNav: true
showInHeader: true
showInFooter: true
---


#Turbo Documentation


Turbo generates the latest code and assets for your theme, streamlines
the process and provides a centralized place of communication for
Luminate templated package.

Getting Started 
---------------

There are a few things to know before you begin.

-   Navigating away or refreshing the form will reset it. There is
    currently no saving/resuming functionality.
-   Chrome is the preferred browser. IE isn’t supported.
-   You should create a Github account with a username like
    Blackbaud-JasonRikard so you can communicate on issues.

Contributing 
------------

### Github

Our [Github] repository is where we collaborate on code, features,
themes, bugs and enhancements. It’s also where anyone in Blackbaud who
is interested in Turbo can come to participate. If you are using any
part of Turbo, please request access to the repository.

### Access Request

<p class="alert alert-success">To request access to this repository, email <jason.rikard@blackbaud.com>
with your Github username that is in the following format:
*Blackbaud-JasonRikard*.<p>

### Bugs and Enhancements Requests

After submitting a request for access, navigate to the issues tab on
Github and complete the form.

-   Request repository access.
-   Go to the issues tab on the right.
-   Click the new issue button.
-   Describe, label and assign your request if applicable.

### Contributing Code

Code contribution will follow a [Pull Request] workflow.

-   Fork the repository.
-   Commit your changes to your fork.
-   Create a [Pull Request] to initiate the code review process.
-   Follow the status of your pull request until successfully merged
    into the mainline.

Client Build Process 
--------------------

Implementing a new theme for a client in Turbo.

##### Overview

Once you receive the assets from the client, open Turbo. Follow the
steps to complete the form and download the archive. This archive
contains all of the assets for the template and can now be imported
manually or through the Content Upload feature of Luminate.

### Assets Required to Begin

##### Assets needed from client

-   Typography
-   Logo
-   Navigation
-   Call to Action Text
-   Brand Colors
-   Social Media Links
-   Images for slideshow (High Resolution Landscape)
    -   Slide Caption Text
    -   Side Button Text
-   Sponsors
-   Logo Footer (if Applicable)

##### Organizational information

-   Name of Organization
-   Address
-   Shortname [Site Listings]
-   Site ID [Site Listings]
-   TeamRaiser ID (Fundraising &lt; TeamRaiser &lt; See ID
    of TeamRaiser)
-   TeamRaiser Title (Full name of Event
-   Donation Form ID (Fundraising &lt; Donation Management &lt; Select
    Manage of the campaign associated with the TeamRaiser to find ID)

### **Note:**Before starting the form all custom pages should be created first so you can link them up in the Navigation section of turbo. If you are unable to create the pages at this time you can simply return to the form and fill out only the Navigation section and copy and paste the generated code into the Main Navigation reusable

Input Fields 
------------

##### Unique Theme ID

To help identify theme assets and PageBuilder pages, Turbo asks you to
define a unique TeamRaiser id. This is appended to all reusables for
uniqueness and is used to differentiate between the different theme
folders and pages. We recommend choosing an acronym that represents the
topic of the event.

##### Organization

-   Name
-   Address
-   Short Name
-   Site ID

##### TeamRaiser

-   TeamRaiser Title
-   TeamRaiser ID
-   Donation Form ID
-   Site ID

##### Choose Social Links

In this section you can reorder the links and add new icons by selecting
Choose Social Icons. When the new window opens simply select the social
icon you need and it will add it to the list.

##### Colors

Enter the clients brand colors (Hex Value) in the input fields. If you
were not provided with a color you can click in the input field and a
color picker is displayed

##### Carousel

Turbo crops and enforces aspect ratios and naming conventions for
images. It will convert your files to the appropriate file format.

Select Choose File to upload a new Image. When you are satisfied and
have the desired look click crop below. Once the new slide is added you
can click on the pencil icon to update the caption and button text of
the slide. Similarly to the Social icon section, you can reorder the
slideshow images.

##### Global Navigation

The Global Navigation has many features to allow you to best construct
the main navigation for the TeamRaiser.

There are two ways you can add a new link. The first option is to select
a link from the Common Links dropdown. This is a starter (and growing)
list of common links in TeamRaiser. Select the link you want and click
add. Lastly, you can create a custom link. In the first input field,
type what you want the name or label of the link to be called (For
Example - Contact Us). In the the second field enter the URL of that
page. We recommend creating all custom pages for TeamRaiser prior to
filling out the form but we understand that is not always possible. You
can come back to this section later to update the information and use
the generated code at the bottom of the form to copy and paste the
navigation into the appropriate reusable

The section to the left is a representation of the main navigation. Each
link can be reordered, edited using the pencil, or deleted. Click and
drag a link slightly in-ward to indent and create a sub link that will
be the dropdown of the navigation. Please note Turbo is designed to only
accommodate one level deep of dropdowns

##### Sponsors

This section operates the same as the carousel

##### Export Code Archive

This will download your assets and code



Content Upload 
--------------

Luminate has a feature for creating PageBuilder pages and uploading
images to the image library in bulk. By placing the contents of the
files on the FTP, the Content Upload tool can turn these files into
PageBuilder pages and images in the Image Library. It finds these files
by asking for a CSV that specifies the file names. Turbo generates the
CSV files (turbo.txt and turbo-img.txt), file structure, and correctly
named files to make this easy.

#### How-to:

Login to the client’s LO instance and navigate to the Content Upload
page (https://secure{number}.convio.net/{site-id}/admin/ContentUpload).
Choose ‘turbo.txt’ and select Create PageBuilder Pages to automatically
create the PageBuilder Pages from the contents of code files you
previously placed in the FTP. Next select turbo-img.txt and select
Upload Images to Image Library to add your images to the Image Library.

Notes:

-   Luminate says it wants a CSV file when really it wants a text file
    with CSV content.

-   Content Upload will not

    -   Make your required Page Builder Content Folder

    -   Mark your page as reusuable

-   Content Upload will make your page active

-   If any errors are reported, you will most likely need to create the
    pages manually. Please report reproducible errors to
    <jason.rikard@blackbaud.com>

\

Advanced Notes/Developer Comments:

-   Content Upload seems to be abandoned from a past process and we’re
    adopting it for this use case. It’s the closest thing I can find to
    a LO PageBuilder Page API.

-   If you know someone from engineering that would be willing to
    improve the Content Upload feature, please contact
    <jason.rikard@blackbaud.com> !

-   The file paths in the CSV are
    /etc/convio/site\_data/995/00000995/static\_data/{client ftp root} .
    This example is for VATEAM with site ID 995. The first 3 digits are
    the last 3 digits of the site ID and the second set of digits is the
    full site id prepended with 0s until the length is 8. If the site ID
    were 2345, the path would be
    /etc/convio/site\_data/345/00002345/static\_data/{top level of
    client FTP } intentionally leaving out the 2 on the first part.