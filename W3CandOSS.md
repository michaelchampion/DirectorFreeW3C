# Position Paper for a Proposed Meeting

For much of its history, W3C has  focused on making browsers more interoperable.  Users and  developers had to deal with the expensive problem of building appealing and functional sites that worked on the range of browsers their customers used. Standards evolved in a "spec first" manner:  Representatives from the browser implementers would convene at standards groups to draft specifications.  When the specs were reasnably stable and prototype implementations showed promise, they implementation began in browser engines. Beta testing and formal interoperability testing of experimental builds of the browsers indicated when the spec was ready to become a formal standard.  In essence, the *specifications* were tested more than the implementations; test showed whether new web platform feature had a clear enough spec for independent  teams to build browsers that implemented the feature in a way that worked the same in multiple browsers.

Deployment of new features to the real web happened at an uneven pace, since it often took years for one browser platform team to prioritize implementing features pioneered in another platform.  

Beginning with Gecko/Firefox, gathering momentum with WebKit/Safari and Chromium/Chrome, now that Opera and Microsoft have abandoned their own browser engines, *all* modern browsers are built on one of the open source engines.  This has more or less solved the browser interoperability problem:
* The most widely used browser clients -- from Google, Microsoft, Opera, Samsung, Brave, and others -- use the Chromium engine, and the common codebase means they interoperate by default.
* The fact that developers of one engine can see the code implementating  even complex features in other browsers allows them to keep the platform functionality aligned across engines.
* Even when browser clients use different engines, they may use the same open source codebase for specific features.  The clearest example is WOFF (implementation report ...).  WebRTC is another example where shared source code from WebRTC.org allowed implementations to interoperate long before the stack of underlying protocols was well-enough specified to be standardized.
* The open ecosystem allows specialized vendors such as Igalia to implement web platform features in browser engines whose owners don't have enough business incentive to invest in their own implementation,

So what should W3C do now that browser interoperability is mostly a solved problem?  Focus on the subset of web platform specs (especially CSS) that really do get done at W3C?  Find new problems such as privacy to focus on? Fade away and leave room for OSS-centric organizations such as the Linux Foundation to issue standards?  Let's consider what a world where the OSS browser implementations define the de facto standards might look like:

1. Concentration of power
2. Patent protection
3. User voice

The 3rd concerns me the most.  RFC 8890...


## Role of OSS browser projects
* Big companies that control the projects do most of the implementaiton;
* code first not spec first; this makes it easier to get interoperability between different browser products since they either share the same "engine" codebase or at least can inspect others' code ... 
* Standards orgs coordinate /facilitate more than drive
* But formal process documents still describe a spec-first process with multiple independent implementations necessary to advance
* How can process describe and shape reality without rubberstamping?
* Examples: WOFF, WebRTC are Recommendations with only one OSS implementation 
* Testing ....
* Martin Thomson's post on the relations between standards, tests & implementations  https://lowentropy.net/posts/standard-principles/

## Possible solutions
* Identify the "threat model" , identify principles that would mitigate them
* Open governance of major OSS projects



* some significant pieces of technology (WebRTC being particularly close
to my heart) rely on a single open source library; while such a library
can end up being used differently in different implementations, it
remains that this means at least part of the "double implementation"
check in the W3C process gets much more limited in depth in these
situations. It may be that a structured approach at documenting these
limitations and identifying possible mitigations if they're necessary
would help bring clarity to WGs, improve our interop impact.

* more fundamentally, as Mike Champion has noted many times, some
conversations that might have happened as standard discussions when the
goal was interoperability between proprietary systems have migrated
towards discussions on code contributions & governance in a shared open
source project; what does this mean for the long term future of the Web
& W3C? I thought Martin Thomson's post on the relations between
standards, tests & implementations brought (indirectly) some interesting
considerations to that question
https://lowentropy.net/posts/standard-principles/
