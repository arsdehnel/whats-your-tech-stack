---
layout: tech-stack
title:  "BIW Products"
date:   2016-01-30 20:59:48
categories: tech-stacks
tags: [java, oracle, php, mysql, nodejs]
---
## What's your tech stack?

For years we've been purely a Java and Oracle shop (basically since we started making things on the web).  This started in the late 90s when we were just figuring out our place on the internet.  Front-end development wasn't a thing yet so server-rendered JSPs served us very well.  Starting in probably 2006 we had a User Experience Team (UET) that included a couple (literally 2 positions) front-end developers.  These two were largely PSD-to-HTML and CSS converters initially but progressed into two of the foundations of what is now our rapidly-growing User Interface Development team (fka Front-End Development team).

Starting in about 2011 we added a few PHP developers and a MySQL option mostly as an experiment.  The team hasn't grown very much but they certainly have found their place in the BIW development environment.  Starting in mid-2014 the front-end development team grew to the point it became it's own official team rather than being part of the larger product development team.

Our most recent change in our architecture has been to start the decomposition of our monolithic product into microservices.  This will then, in turn, be recomposed back into our next generation of products built on a variety of platforms and for a variety of customer requirements.  These services are currently being built almost entirely in Java (as we have a lot of experience, tools and comfort with it) with the exception of a couple being built in Nodejs for those services that fit that language better.  The most recent product to begin development is being developed as a Nodejs front-end application that will be the service-orchestration application as well as consolidate the server-rendering and client-rendering of our React codebase into one [universal JavaScript][universal-js] codebase.

## What other options did you consider?

Up until Q4 2015 we didn't consider anything past Java/Oracle and PHP/MySQL and even in the past few months we haven't strongly considered anything outside of Nodejs.

## What predetermined conditions did this decision have to work within?

15+ years of Java/Oracle meant that we have a lot of comfort with those options.  We have a lot of tools and infrastructure around those that makes them very compelling even if you feel they aren't the best tool for the job.  While management has indicated that "the doors are open", the reality is that adding new things to the tech stack just because they are the latest and greatest language isn't *really* an option.

## What factors made you make the choice that you made?

See above mostly. While we have intentions of getting to the point where we pick the right tool for the right job it's hard to just drop new servers and flows into the stack quickly.

## Where do you hope to expand, change or evolve your tech stack in the future?

As we move to a more fully-developed UI Dev team on the front and microservices on the back open us up for more innovation, iteration and the ability to truly use the right tool for the job without as much contraint.  The UI team has expressed interest in React Native for iOS/Android development which seems like a logical path to follow once our first universal JavaScript React web application is up and operational.

The Erlang/Elixir/Phoenix stack is very much on our radar to review and possible involve in our development. The speed and built-in socket support that this brings while still offering Ruby-like development syntax is too hard to not have this on the radar somewhere.

Scala is on the list because it runs on the JVM which we're very familiar with and it would be an easier move to make. This likely gets us some innovation space and allows our Java developers to try something new without diving off the deep end into a whole new development environment.

On the database front Cassandra is definitely the front-runner for our next place to explore.  We just signed an agreement with Oracle on the licensing of our servers to support that option for a while but we have no scalable NoSQL option right night.  We use Couchbase as a caching server on the Java services but that doesn't really play in the same space as something like Cassandra.

Postgres or Amazon's recently released Aurora are also definitely on our radar for replacing Oracle and MySQL as our go-to RDBMS.  The benefit of investing in montoring, tuning and the infrastructure for these replacements is a harder sell to management than Cassandra, but it's still a discussion we're having.

We are also looking at the [Elastic Stack][elastic] for highly performant scalable searches as well as powerful log analysis and dashboards.  This would likely be an API that we use from our UIs that reference data stored in our microservices rather than housing a large set of data directly in Elastic Search.

[universal-js]: https://medium.com/@mjackson/universal-javascript-4761051b7ae9 "Universal JavaScript"
[elastic]: https://elastic.co "The Elastic Stack"