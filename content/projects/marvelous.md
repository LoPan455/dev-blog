---
title: "Marvelous"
date: 2021-08-14T10:23:08-05:00
draft: true
---

# The Origin Story of Marvelous

Marvelous is Spring Boot / Kotlin application that is designed to interact with the Marvel comic book API.  

I started working on this app back in the Fall of 2018, when I first joined Target Corp as an Engineer. The projects my team maintained were all Spring Boot & Java of Groovy. Having come from an team that maintained a framework-less LAMP stack application, I had a lot to learn. 

I got to work using a learning strategy that works pretty well for me: identify a small project or task that seems fun and dig into the learning resources to build some basic functionality. Fortunately, my company provided excellent learning resources, so I jumped in with a project goal in mind: use the Marvel comics public API to fetch and log out some data.  That seemed like a reasonable little "Hello World" task.  I was excited to play around with come cool content in order to make it realistic and fun.

Fortunately for me, the Marvel API is well-designed widely recognized REST standards.  Resource paths are clearly defined, related data is easy to fetch from a given context, and it's overall familiarity with what I already knew about REST APIs made it easy to get started.

I really struggled enjoyed getting my application to work.  Over the past few years, as my understanding of Spring and JVM Languages deepened, I would revisit this little app to improve it. I recently migrated it to Kotlin due to it being the primary language I used on my team at Target.  Marvelous has also served as a sandbox to play around with various Spring features like Webflux, Webclient and various other Spring features I wanted to discover.  I anticipate using this project as the base to explore a wide variety of Spring features.

# Architecture

As a Spring Boot app, Marvelous exhibits some standard characteristics of a REST API:

* HTTP Controller endpoints exposed to the outside world to handle Create / Read / Update / Delete (CRUD) requests
* A Service layer to process inbound requests, make calls to external data sources.  In its most basic form, the Marvel API itself is the only external data source, but we could easily integrate other data sources
* A Data Access layer to persist data to a database

Another characteristic of Marvelous that posed a challenge was the need to authenticate my API requests.  The Marvel API [documentation](https://developer.marvel.com/documentation/authorization) outlines a specific set of data headers that need to be present on any calls to its API.  This was the most difficult thing to build correctly during my learning process.  

# A Basic GET API call To Fetch Some Data

