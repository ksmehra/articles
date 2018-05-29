# RPA Best Practices: Recommendations for Google Chrome & Mozilla Firefox

Ksheer S Mehra ksheer13@gmail.com

- - -

## Purpose


This document attempts to provide guidelines and best practices for deploying Google Chrome (Chrome) & Mozilla Firefox (FF) in the enterprise with respect to RPA efforts. These recommendations are not specific to any organizational function, and therefore can be circulated to clients from any domain.


## Audience


This document is targeted toward:


1. IT department of the said enterprise


	_The IT can use this document as a part of the guidelines while preparing the environments, and while creating IT policies._


2. RPA COE of the said enterprise (or similar function)


	_The RPA engineers can use these guideline to plan & focus their automation effort around the versions of Chrome and FF that will be provided by their IT dept._


## Motivation


The browser landscape is rapidly changing, and it is driven by the motivation of the major vendors to become the dominant player. This has led to a _features war_, which in turn has led to a rapid-release-cycles of the browsers under consideration in this article.


Due to the nature of constantly evolving standards, certain experimental features are built and released in to the mainline releases. This has known to case severe deviations from older behaviors. This can be in terms of look & feel, user exerience, security policies, among other aspects.


With respect to RPA, rapid-release-cycle can, and previously has, led to breaking automations which were otherwise working fine.


### What this document is not


This document is _not_ an standard operating procedure (SOP). This document attempts to provide certain guidelines and recommends best practices with respect to browser deployment for RPA.


## Best Practices Recommendations


Both Chrome & Firefox maintain release lines that are geared specifically for Enterprises, and are distinct from the mainline (end-user/consumer/non-enterprise user). The main characteristic of this release line is the conservative approach to releases. The releases cycles are slower & leaner than the mainline.
For Chrome this release line is [Chrome Enterprise](https://enterprise.google.com/chrome/chrome-browser/) & for Firefox it is [Firefox ESR](https://www.mozilla.org/en-US/firefox/organizations/).

### The Recommendations

1. **Migrate to Chrome Enterprise & Firefox ESR**
	The conservative release cycles will ensure minimal deviation after updates/upgrades.


1. **Disable auto-update**
	The browsers must have release & deployment cycles of their own in each environment for RPA.


1. **Don't use Chrome and Firefox interchangeably in RPA**
	Although there is a general idea that enterprise web-based apps most probably must function identically in either browser. But in reality this is far from reality, especially for dated web-apps, which were are not written in _modern_ web UI frameworks.


1. **Certify web-apps for automation against a specific browser & specific versions of the browsers**
	Only certified versions of browsers be deployed in the environments. Promote new versions from `DEV -> UAT -> PROD` only after certifying that existing bots do not break.


1. **Deploy Chrome Enterprise & Firefox ESR using group policies**
	Deployment using group policy objects ensures that the roll-out is managed and uniform across all nodes in the RPA landscape.

### Further Reading
#### Chrome
1. Chromium Release Calendar: https://www.chromium.org/developers/calendar
2. Chromium Release Process: https://www.chromium.org/developers/tech-talk-videos/release-process
2. Chromium Group Policy Objects: https://support.google.com/chrome/a/answer/187202?hl=en


#### Firefox
1. Firefox Release Calendar: https://wiki.mozilla.org/Release_Management/Calendar
1. Firedfox ESR Landing Process: https://wiki.mozilla.org/Release_Management/ESR_Landing_Process
1. Firefox ESR deployment using Group Policy: https://developer.mozilla.org/en-US/Firefox/Enterprise_deployment

