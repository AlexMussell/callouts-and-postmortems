# Callouts and Postmortems
Callouts that involve calling out an engineer and postmortem management is notoriously difficult to implement correctly for many reasons. One being that it is hard to standardise any sort of practicies as everybody will have different standards they feel accetptable, another being that ticketing systems (in my opinion), are generally rubbish and highly convoluted. In fact they are so convoluted that in large companies, you have entire teams dedicated to managing callout. But what if you are a smaller company that doesn't have a dedicated team? Or, like a lot of tech people, you are fed up with having to use a million different technologies for things like documentation, callouts, engineering etc etc. I personally do not want to have 5 different logins on 5 different websites just to go about my day to day. This repo was created to provide a standardised way for you to combine callouts and postmortems into markdown and host them in github/gitlab (assuming you have private repositories). I like all my callouts about my estate being hosted here as it is very easy to navigate, everybody in thea team knows exactly where everything is, it provides as easy way to search for recurring and specific callouts, enables us to communicate with teams across a company in a standardised way, and also provides a way for us to track what we plan to do to combat recurring callouts.

## Layout
After some trial and error, I have found that the best strategy for folder structure is to divide the folders by technology, then in a `<callout-issue>-<date>` folder with a `callout.md` and `postmortem.md` underneath it. A couple of examples are put into the repo. Every callout your team receives must have both a callout and postmortem write up associated with it. 

## General rules for writeups
The key thing here is to __DO NOT CHANGE THE TEMPLATES. DO NOT ADD/REMOVE STUFF AT RANDOM.__ Copy and paste the required template and fill out as necessary. If something is not applicable in the template, do not remove the key, just add "n/a".  These are professional documents meant to be consistent across any callout issue you have. Remember that these documents may not just be read by you. They are also supposed to be sent to teams that have been effected by the callout. Obviously this isn't the case for all callouts. 

These writeups also greatly help people who are new to the team and the oncall rota. It allows for them to quickly search for previous issues if they are called out and see what steps have previously been taken through their postmortems.

The key to BOTH these documents is to keep it name and blame free. As a team, it is important to realise that stuff happens, but you are in it together when callouts arise (especially MPIs (Major Production Incidents)). Along with no names, there is no pronouns. No "I did this, I did that, he did this". Keep it technical only. 

## Postmortem Template
This usually comes after a callout of any sort. Make the `<issue>` directory name as obvious and general as possible, as even if it isn't 100% the same issue, it could be a massive help at pointing in the right direction.

The postmortems will be sent to all users affected by any sort of outage. So they need to be consistent. I find it best that once they have been written in markdown, to run them through a [markdown to pdf](https://www.markdowntopdf.com/) service to ensure all writeups look the same.

Make sure to add any dashboard material to your document as proof to users and reference for your teams. For example, if you were called out by your automated alerts which we activated when Prometheus recorded high CPU, post the dashboard link in the
Supporting Information segment of the template.

## Summary
The callout template needs to make this the first port of call engineers who receive callouts, and needs to be filled out as work is being done. The more information we have, the easier it will be to resolve issues and to generate tickets as actions in the postmortems, preventing issues appearing in the future. Which in an SRE team, should be your number 1 priority.

