<p align="center">
  <a href="https://everfund.com"> 
   <img alt="Everfund" width="350" src="./docs/logo.svg"/>
   </a>
  <h1 align="center">Full-stack engineer technical test</h1>
</p>


This is the technical screening is part of Everfund's interview process for full-stack engineers. Please familiarise yourself with the contents of this README, as specific feature requirements are discussed in this document.

## About Everfund
Everfund is the dev-first donation platform for modern nonprofits. Use a composable SDK to take control of all the components needed for modern donations, without building from scratch. Save time and integrate the best donation experiences faster to help nonprofits focus more on their causes.


## Objective

This technical test requires you to assemble a dashboard view for a mock payments system. For some tasks, you will need to complete **GraphQL** resolvers in a way you see fit, so as to present real, accurate values to the front-end components. Additionally, you may wish to exhibit your **CSS** flair by improving visual aspects of the dashboard. Please see the full lists of primary and extension tasks below.
## Structure

This project consists of a basic **Redwood** application, written in **TypeScript with strict mode enabled**. The application is split into _web_ and _api_ directories.

## Tasks

### Primary
We expect completion of the following primary tasks:

1. Implement the requisite queries to populate the values for the following stats cards:
    * Total number of donations
    * Total amount donated (£ GBP)
    * Donations with Gift Aid (%)
2. Implement a table showing the newest 20 donations for the selected non-profit. You can improve the look-and-feel of the table as you see fit. We provide a _Table_ component, viewable in **Storybook**.

### Extension
If you have time remaining, it would be good to see you tackle the following extension tasks:
1. Replace table columns with iconography (This can be done with [heroicons](https://heroicons.com/) as it's already installed) or other styling to best display the data stored in those columns.
2. Add additional stats cards to the dashboard, choosing other stats that you feel may be useful to a non-profit worker.
3. Add a "Top Donations" component to the dashboard, which shows the top 5 donations ever made to the selected non-profit.

We understand and appreciate that there are many different approaches to these problems, and opportunities to showcase individuality. Please feel free to lean on NPM libaries to help complete the objectives. Specifically, you need to be able to explain your approach, including architectual decisions and use of any libraries. Show us what you can do!

## Things to make note of

- The terms donation and payment are used interchangably throughout this document and codebase. Typically, a donation is a payment with additional metadata.
- Amounts are stored in the database in pennies, but should be displayed as £xx.xx.
- Resolvers should only return records or data pertinent to the selected non-profit. Revealing information about other non-profits is bad!
- Gift Aid is applied at the standard UK rate (25% of the donated amount).
- Stats cards should only be concerned with donations in the _succeeded_ state.
- The donations table should not be concerned with the status of a donation.
- The non-profit that is selected can be accessed through the **React** context that is found at _MainLayout.context.tsx_.
- Look out for **TODO** comments; they may help to guide your approach, although it is also valid to disregard their advice.

## Get Started
**Prerequisites**

 - Redwood requires [Node.js](https://nodejs.org/en/) (>=18.x) and [Yarn](https://yarnpkg.com/) (>=1.15)
 - Are you on Windows? For best results, follow Redwood's [Windows development setup](https://redwoodjs.com/docs/how-to/windows-development-setup).


Start by installing dependencies:

```
yarn install
```

Then change into that directory and start the development server:

```
cd technical-interview
yarn rw prisma migrate reset or yarn rw prisma migrate dev
yarn redwood dev
```

To start storybook to see the components:

```
yarn rw storybook
```

## Submission

The quickest way to submit your work is by [forking](https://github.com/everfund/technical-interview/fork) this repository, then sending us a link.

Alternatively, you can copy this repository to your personal space, and send us a link to your branch (if you make your repo private, you'll need to [invite us as collaborators](https://help.github.com/en/articles/inviting-collaborators-to-a-personal-repository)).

If this is an unsolicited application, you can contact us with the link to your fork and your CV to [email](mailto:jobs@everfund.com?subject=Everfund%20Fullstack%20Engineer%20Job%20Application&body=Please%20attach%20your%20resume%2FCV%20and%20let%20us%20know%20a%20little%20about%20yourself%20below.%0D%0A%0D%0A%0D%0AWhy%20you%20want%20to%20work%20at%20Everfund%20(if%20not%20attaching%20cover%20letter)%3A%0D%0A%0D%0ALocation%20you’re%20based%20in%3A%0D%0A%0D%0AGitHub%20profile%3A%0D%0A%0D%0ALinkedIn%20profile%3A%0D%0A).
