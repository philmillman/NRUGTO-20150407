
# Performability
-----------------
## Performance & Scalability @ Indigo
---
#### Phil Miller
#### Manager, UI Development
#### Indigo Books & Music


---

## Who are we? 


----

> Indigo is
 Canada's largest purveyor of ideas and inspiration to enrich your life, with books, specialty toys, gifts and lifestyle
 enhancing products that affordably offer intrinsic quality, beauty and timeless design. As the largest book and
 specialty retailer in Canada, Indigo operates in all provinces under different banners including Indigo Books &
 Music; Indigo Books, Gifts, Kids; IndigoSpirit, Chapters, Coles and the online channel, www.indigo.ca.


----

## Fun Facts
* Primarily .NET/MS 
* Effectively two businesses
 * Books (data driven)
 * Gen. Merch. (heavily curated) 

Note:
- This 'split personality' in our online world leads to some very challenging performance problems
- Must optimize for large datasets 
- Also optimize for very client heavy merchandized pages

---

## What is performance? 

Note:
- How do you define performance? 

----

## What is scalability? 


----

## Performance + Scalability
## = Performability! 

<h4 class="fragment fade-in">"...a composite measure of performance and scalability"</h2>

Note: 
- I'm a little obsessed with creating portmanteaus like this
- "Performability is a composite measure a system's performance and its dependability."
- In this our dependability is intrinsically tied to scalablity so let's repurpose this
- "...a composite measure of performance and scalability"

----

## The impact of performability
* For every 1 second of improvement they experienced up to a 2% increase in conversions
* For every 100 ms of improvement, they grew incremental revenue by up to 1% <sup>[1] [Walmart]</sup>


[Walmart]: http://www.webperformancetoday.com/2012/02/28/4-awesome-slides-showing-how-page-speed-correlates-to-business-metrics-at-walmart-com/  "Walmart"

Note:
- Here is a great case for performance from an etail juggernaut 
- Now that we know there is a business case for performance, let's explore our journey

---

## Part 1 - Where we were

----

## A mixed bag
* Keynote
* Truesight
* Sitescope/Tivoli

Note: 
- The 'synthetic trap' - why is this a problem? 

----

## What wasn't working?
* Siloed and incomplete metrics
* No _real user_ performance data
* No monitoring in preproduction environments
* Unclear alerting

Note:
- Metrics existed is various different system 
- Missing key metrics, client and server
- Alerts arrived late and gave no real information
- How can you understand your users if you don't know how your application performs for them? 

----

## What did we need? 
* Real-time data
* More actionable alerts
* Business-friendly performance metrics
* Tools for capacity planning

Note:
- In enterprise eCom, time is money, the sooner we know about something, the better
- If you can't understand an alert, then it's not very useful
- What's the point of great performance if you can't share it with your boss? 
- Good performance should be predictable

----

## The obvious choice? 

----

<!-- .slide: data-background="http://storefront.nr-assets.net/assets/newrelic/source/NewRelic-logo-square.png" data-background-size="50%"-->


---

## Part 2 - Where we are today

----

## Apdex 
----------------------------
### "One metric to rule them all" 
----------------------------
* Real Users
* Business Friendly 

Note: 
- "The CIO's metric" 
- Allows us to easily tell how our customers are experiencing our applications
- Can evolve over time as we set more aggressive goals (T value) 

----

## New Relic 
* Initial rollout of APM, Browser, Server, and Plugins
* Encompassing indigo.ca, m.indigo.ca, API, and internal tools
* ~35 agents, 23 APM applications, 11 Browser applications
* 77 servers, 4 plugins

Note:
- Also present in Stage and QA environments
- These numbers are our current deployment
- Done over the last year

----

## Performance - Baseline
![browse 20140324](/img/browse_20140324.png)

Note:
- Here's our baseline performance for our Browse app
- This is after an initial set of performance improvements before we rolled out New Relic

----

## Performance - Today
![browse 20140324](/img/browse_20150323.png)

Note: 
- Here's the same app over a comparable period, a year later
- Note the drop of around ~1.5s on the client and server response time is halved
- We've also seen incremental improvements in apdex on both the server and the client
- Also note that we use Akamai so our performance is much better during the day when cache hits are high
- The overnight spikes you see are due to cache misses and a lower sample size

----

## Performance - Comparison
[![http archive][2]][1]


[2]: /img/httparchive-20140101vs20150101.png
[1]: http://httparchive.webpagetest.org/video/compare.php?tests=140101_0_A14-l%3AJan+1+2014%2C150101_0_A5A-l%3AJan+1+2015&thumbSize=200&ival=1000&end=visual "HTTP Archive"

Note:
- I'm especially proud of this slide, showing year over year improvement on the homepage
- Note how the performance is even worse than the baseline slide I showed you from march 2014
- This is from httparchive (NR is a sponsor) 
- If you dig in you'll see the the 2015 page is actually much heavier which means our code is even more efficient

----

## Capacity Planning
![scalability report](/img/scalability_browse.png)

Note: 
- As an online retailer our year is always about planning for our holiday period
- Scalability reports such as this help us predict app performance so there are no surprises
- As mentioned before thanks for Akamai, any application that can be heavily cached, scales very well

---

## Part 3 - Where we're going

----

## The Next Step
* Full implementation of Synthetics (bye Keynote!) 
* Mobile for all native apps

Note:
- Using the more advanced scripting capabilities of synthetics we hope to get even more out of our synthetic monitoring
- The selenium based scripting environment should allow for sharing of code between New Relic and BrowserStack
- New Relic for mobile should be deployed in the next few weeks and we're excited to get some insight here as we mature our in house mobile dev practice

----

## The Next Step (continued)
* Unification of alerts on new Alerts platform
* PagerDuty rollout for frontline support

Note:
- I'm really excited to try out the new alerting platform and improve our situational awareness even further
- As a result of this we hope to trial PagerDuty to communicate these alerts as effectively as possible

---

## [We're hiring!](http://www.chapters.indigo.ca/en-ca/careers/careers-at-indigo/)
* [Email](mailto:pmiller@indigo.ca)
* [LinkedIn](http://ca.linkedin.com/in/themillman)
* [Twitter](https://twitter.com/philmillman)
 



