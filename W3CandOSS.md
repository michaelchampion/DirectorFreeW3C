# W3C standards and Open Source implementations

@michaelchampion's personal thoughts ...

Disclaimer: I'm not sure about OSS projects generally not having strong patent policies, will investigate (or accept PRs correcting any mis-statements)

## The Interoperability challenge ....
For much of its history, W3C focused on making browsers more interoperable.  Users and  developers struggled with the expensive problem of building appealing and functional sites that worked on the range of browsers their customers used.  Browsers were built with a mix of proprietary and open-source code, and  the companies built them had business incentives to keep at least some implementation code private.

W3C addressed the challenge in a *spec-first* manner:  Specifications came before implementations. Representatives from the browser implementers would convene at standards groups to draft specifications.  When the specs were reasonably stable and prototype implementations showed promise, they implementation began in browser engines. Beta testing and formal interoperability testing of experimental builds of the browsers indicated when the spec was ready to become a formal standard. 

 In essence, the *specifications* were tested more than the implementations; test showed whether new web platform feature had a clear enough spec for independent  teams to build browsers that implemented the feature in a way that worked the same in multiple browsers. But actual deployment of new features to the web happened at an uneven pace, since it often took years for one browser platform team to prioritize implementing features pioneered in another platform.  
... largely solved by Open Source implementations
Beginning with Gecko/Firefox, gathering momentum with WebKit/Safari and Chromium/Chrome,  and culminating with Opera and Microsoft abandoning their own browser engines, *all* modern browsers are built on one of the open source engines.  This has more or less solved the browser interoperability problem:
* The most widely used browser clients -- from Google, Microsoft, Opera, Samsung, Brave, and others -- use the Chromium engine, and the common codebase means they tend to interoperate by default.
* The fact that developers of one engine can see the code implementing complex features in other browsers allows them to keep the platform functionality aligned across engines.
* Even when browser clients use different engines, they may use the same open source codebase for specific features.  The clearest example is the Web Fonts Recommendation, whose implementation report states ["All user agents appear to use the Google WOFF2 library”](https://www.w3.org/Fonts/WG/WOFF2/Implementation.html).  WebRTC is another example where shared source code from WebRTC.org allowed implementations to interoperate long before the stack of underlying protocols was well-enough specified to be standardized.
* This open ecosystem allows specialized vendors such as Igalia to implement web platform features in browser engines whose owners don't have enough business incentive to invest in their own implementation.  This further improves interoperability on even web platform features that cater to small audiences.

## Accept the inevitable?
So what should W3C do now that browser interoperability is mostly a solved problem?  Focus on the subset of web platform specs (especially CSS) that really do get done at W3C?  Find new problems such as privacy to focus on? Fade away and leave room for OSS-centric organizations to issue standards?  Let's consider what we would lose in a world where the OSS browser implementations define the de facto standards without W3C's input:
1. Distribution of power: The large companies that control the OSS projects do most of the implementation and would have even more control over the web platform than they do today.
2. Patent protection:  OSS projects tend to not have as strong patent policies as W3C does, so it would be less clear that the implementers are contributing their patents as well as their copyrights (and employees’ labor) to the web platform.
3. Horizontal review: While the big implementers have strong business and legal incentives to ensure accessibility and internationalization, there would be no formal, public process to guarantee that.
4. User input: The web platform would evolve in a manner that is “open” mainly to highly technical people who can credibly push back on the costs, benefits, and unintended consequences of platform changes; ordinary users and website developers would find it difficult to participate.

In short, without the standards organizations  active input, the web platform would be developed *code-first* manner. Specifications would be an implementation by-product, used to document the features that are supposed to be interoperable and for test suites to reference.  “Standards” would   be mostly *de facto*, whatever works.

## One way forward: open governance of open source

Putting in a governance structure for the major OSS browser projects could mitigate the concerns above. There will be challenges:
* The big companies who invest in OSS projects do so for business / personal economic reasons; giving up control might undermine that rationale.
* Most OSS projects are effectively [DO Ocracies](https://communitywiki.org/wiki/DoOcracy) so formal control may not be effective.
* Under OSS copyright licenses, participants have the option of forking existing code into a new project if the governance structure seems oppressive.

Nevertheless, openly governed versions of Chromium, Webkit, and/or Gecko might:
* Put measures in place to minimize the risk of a single company dominating the project's agenda. 
* Try to reform the "geek" cultures of the projects to be more welcoming to *users*; consider [RFC 8890](https://www.rfc-editor.org/rfc/rfc8890) and the various [discussions] (https://github.com/WebStandardsFuture/Users1st) of its [implications](https://www.mnot.net/blog/2020/08/28/for_the_users) and make a good-faith effort to bake those principles into the governing documents.
* Explicitly identify and attempt to mitigate the other issues, e.g. define more explicit royalty-free patent policies, add processes or review guidelines to encourage acessibility, internationalization, privacy, etc.
* 
## Another way forward:  clear OSS / SDO division of labor

Alternatively (or perhaps in conjunction with OSS governance reform), change the W3C mission, processes, and policies to reflect the new reality and project a vision of how W3C could better-collaborate with the OSS implementers.

* Redefine the mission to be a steward, or facilitator, of the web platform rather than presuming to “Lead the Web to its Full Potential”. 
* Change processes to accommodate code-first realities. For example, accept that many core specifications will have only one implementation, or that one organization may contribute most of the code for a feature to multiple projects.  There can be various checks and balances to ensure that the single implementer doesn't abuse its power.  For example, the W3C process could recognize that browser *clients* essentially vote for or against the desirability of a platform feature by deciding whether to ship that part of the platform code that implements it.   
* Refine governance and processes to reflect the "users first" orientation outlined in RFC 8890. User representatives could be better-empowered to shape web platform reality without rubber-stamping whatever the implementers do.
* Testing .... Martin Thomson's post on the relations between standards, tests & implementations  https://lowentropy.net/posts/standard-principles/




