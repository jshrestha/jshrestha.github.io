---
layout: post
title: BlocJams
feature-img: "img/sample_feature_img.png"
thumbnail-path: "https://d13yacurqjgara.cloudfront.net/users/3217/screenshots/2030966/blocjams_1x.png"
short-description: BlocJams for iOS is awesome!

---
layout: post
title: BlocJams
thumbnail-path: "img/sample_image.png"
short-description: BlocJams is a Spotify inspired music player.

---
## Summary
BlocJams is a Spotify inspired music player built with AngularJS.  This application allows users to view albums and play music, and features a custom control bar to easily change songs or adjust volume.

## Problem
The goal of the project was to create a new website that would display music albums as well as play back songs from the albums.  There were several features that were requested for each part of this application.  A landing page was desired to display the logo and highlight key features.  Users would need the ability to view the entire collection of albums, including a picture of each album cover and basic album information.  The application would also need to play music from each album, as well as have controls for the user to play and pause each song, change songs with next/previous buttons, and adjust the volume of the playback.

## Solution
Based upon the design requirements, I created three pages:  a landing page, a collection page to display the albums, and an album page to display an individual album.  This album page would contain the music player and controls.  For styling, I included normalize.css to minimize the potential impact of different browsers being used.  I also used Google Fonts to give the entire application a clean, consistent style.  Media queries were used for responsive breakpoints to adapt to multiple devices and screen sizes.

For the application functionality, I initially used plain JavaScript and jQuery for all of the user requirements.  On the landing page, this included using an event listener to initiate custom animation upon a user scrolling down the page.  On the collection page, the albums are displayed dynamically by storing the album templates in string variables.  For the album page, the song list is dynamically displayed by using JavaScript objects to store album information that can be inserted into the HTML.  This allows the same template to be used for displaying each album.  For song playback, event listeners are used to help the user interact with the song list.  The jQuery hover event displays a play button or changes the play button back to the original song number.  The click event determines if a song is currently playing, and either plays or pauses a given song.  Finally, a music player control bar was added to give additional functionality to the user.  This contains a play/pause button, next/previous buttons, information about the currently playing song, and volume control.  To actually play music and adjust volume, the [Buzz music library](http://buzz.jaysalvat.com/) was used.  The Buzz API allows for creation of a Buzz sound object and provides methods and events to track and manipulate audio files.  Two seek bars were added to display the current progress of the song and current volume.  To allow a user to interact with the seek bars, a generic method was created for both seek bars that would update the seek bars after a mouse click or drag event.  Depending on which action was taken, either the song playback or the volume would change to the proportional spot in the seek bar based upon where the mouse event occurred on the screen.  In both cases, the seek bar fill and icon would also adjust to visually show the change to the user.

After the application was built, I then refactored the entire project using AngularJS.  The was mainly done as a learning exercise to understand not only how to use a JavaScript framework but also to experience the pros and cons of using a framework versus vanilla JavaScript.  The functionality of the application did not change, but most of the code was updated to utilize an Angular module that was bootstrapped to the application. Controllers were used for the application's views, and song playback was handled with a service.  A custom directive was developed to control the song and volume seek bars.

## Results
The final application met all of the user requirements and worked as intended.  Testing was done throughout the implementation process as new features were added.

## Conclusion
Overall, BlocJams was a fun and challenging project.  Creating the entire application first with plain JavaScript turned out to be very beneficial.  On one hand, it gave me a good appreciation for libraries and frameworks which simplify many functions and reduce the need for "reinventing the wheel".  On the flip side, I enjoyed developing everything from scratch first and realized that in some cases, plain JavaScript can accomplish what is needed in a much simpler way.  I was surprised at how challenging it was to start using AngularJS.  There was a lot of new terminology, and I had to read through a LOT of Angular documentation as well as look at other people's example code before I started to put the pieces together.  One important lesson I learned was to look at the dates on the articles/posts when searching for helping online.  Many times I invested a lot of time and made several changes to my code to try out something I had found, only to later realize the post was from 2011 and 95% of the information was outdated.  I also learned that it is possible to reach a point of no return when trying to debug a problem.  Instead of continuing to stare at the screen for hours and hours, taking a quick break or coming back a day later often results in finding the problem much quicker.  Going into this project, I was a little intimidated by the amount of new material that I knew I would need to learn.
