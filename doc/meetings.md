###### tags: `SIG Best Practices`

# CDF SIG-Best-Practices

[Agenda in HackMD](https://hackmd.io/uxoIwj7fTjKkI161-IZeFw)
## 11-January-2023
- Attendees: 
    - Terry Cox, Bootstrap
    - Tara Hernandez, Google
    - Fatih Degirmenci, CDF
    - Liora Milbaum, Red Hat

- Agenda:
    - cdCon + GitOpsCon 2023
        - cdCon CFP is now open!
        - The event will take place on May 8-9, 2023 in Vancouver co-located with the Open Source Summit
        - CFP Link: https://events.linuxfoundation.org/cdcon-gitopscon/program/cfp/
        - More info is available here: https://cd.foundation/blog/2023/01/11/cdcon-2023-call-for-papers-now-open/
    - CD for Mainframe
        - Setting up a meeting to have an initial discussion with [OpenMainframe Project](https://www.openmainframeproject.org/)
        - Possibility of co-authoring a whitepaper to start the collaboration
    - CD Reference Architecture Workshop
        - The proposed date for the workshop is March 8, 2023 taking place at the regular timeslot of the SIG Best Practices which is 16:00 UTC
    - Supply Chain Maturity Model document update https://docs.google.com/document/d/1CDSbQezqauwL2BaFob7o2ztLk6dTQGZqZCMZ_szNhW8/edit
    - 

## 30-November-2022
- Attendees: 
    - Terry Cox, Bootstrap
    - Fatih Degirmenci, CDF
    - Emil Bäckmark, Ericcson
    - Tara Hernandez, MongoDB
    - Dirk Bernsau, Fujitsu
    - Colin Bowern, Octopus Deploy
    - Christopher Vig, JenkinsX project
    - Robert Reeves, Liquibase

- Agenda
    - "Measurable supply chain maturity" discussion
        - Code management notes:
            - Can we include examples of "source" that may not be managed by version control and why they should be included, e.g.:
                - shell scripts
                - sql
                - test data generation or other test artifacts
        - Discussion from Colin and Robert on where we might include review of topics like code churn as a supply chain metric
        - Suggestion from Emil on working to reconcile Supply Maturity categories with SIG-Interoperability terminology being defined here: https://github.com/cdfoundation/sig-interoperability/blob/main/docs/pipelines-terminology.md to have consistency of language usage
        - Discussion on what "supply chain" actually encompasses -- commit to deploy, or more DORA-esque definition that encompasses initial business requirement to customer engagement.
            - Best Practices SIG currently defines it thusly: https://bestpractices.cd.foundation/learn/supplychain/
        - More broadly, a basic level of supply chain maturity we think about "features to customer", at a higher level of maturity we are able to track overall changes from broader inputs of the supply chain (e.g. a new CVE patch) and automatically handles it from both a build and notifications perspective
            - cdevents allows us to be declarative about what policies we want to have the ability to automatically implement 
                - Andrea mentions SAS gave a presentation on this idea that they're currently implementing (link forthcoming)
        - Robert asks how do you capture the manual steps that can't be obviously solved programitcally
            - examples, use of a USB key as a part of test mechanism, or a business requirement that manual input of security token keys is still required.
            -  maybe solve this by use of a particular type of notification event that could be captured via email, slackbot, or other interactive mechanism that would then publish a response event that would re-enable the pipeline.
                -  the time spent waiting could be it's own metric against internal SLIs e.g.
                -  similarly, "preset" time-based events can trigger an alert if their requirements aren't met within a set time frame.

    

## 16-November-2022
- Attendees: 
    - Terry Cox, 
    - Fatih Degirmenci
    - Emil Bäckmark
    - Tara Hernandez

- Agenda 
    - Meeting held with software supply chain working group, initial [working document](https://docs.google.com/document/d/1rGvQv2GH8HYbQUZxg89LmWsYe8-MyeTEcj08nwULitw/)
        - best practices site will host final copy
        - could we make a self-assessment survey against this model?
        - can we bring in the concept of maturity that ranges from "survivability" (what is critical need e.g. correctness, lowest level) up to "max convenience" that addresses richer optimization (e.g. more focus on velocity)
        - can we bring in CD Events as part of HOW to do the measurement of these metrics -- provide suggested requirements e.g. to what Events will trigger on.  Canonical state of project here: https://cdevents.dev/
            - [Talk on this](https://www.youtube.com/watch?v=GI_Aly2PKus)
            - Targeting a 1.0 release of spec this coming year, Tekton/JenkinX early adopters? Need to identify something for the reference implementation in the documentation.
            - Proposal to make next best practices meeting a working session to review metrics against state of cdevents
    - Interoperability Whitepaper
        - Never got published, 
        - v1: https://docs.google.com/document/d/1Bgr6EHhW4wUTphU8xyMg87qzSee43PEA_gGdMnPHq9Q/edit#
        - v2: https://docs.google.com/document/d/1o5jHbuEQuspwYOruVB4L5-rG8E1wQm5chq8QN7BrrBs/edit#
        - v1 is in read-only and kept for historical reasons and the work is expected to continue on v2
    - Developer Productivity
        - Build/Test Practices - does it incorporate low level details around things like build caches, intelligent test execution, resource selection (e.g. ARM)?
        - originally idea was to treat this level of detail as case studies, in some cases it might be a "trade-off" rather than a true "best-practice". Example, a CI system that only triggers on repo changes, but it means that CVEs might be backing up and you wouldn't be as up to date from a security perspective
        -  

## 2-November-2022
- Attendees: 
    - Terry Cox, 
    - David Bendory, Google Engineering Manager / Tekton
    - Tara Hernandez

- Agenda 
    - Best Practices
        - [Assessment section](https://bestpractices.cd.foundation/learn/assess/) requires content, possible collab opportunities with some combo of #wg-supply-chain-maturity and/or #sig-software-supply-chain.  Terry to followup on this.
        - Site metrics - there was an attempt to get Google Analytics setup, but as we're a subset of the larger LF ecosystem we can't access it the normal way. There's a complicated workaround the LF has provided.  Continues to be outstanding issue.
    - Reference Architecture:
        - Next steps - identify possible discussion group members for various roles as defined in Views and Viewpoints.
            - For C-suite, perhaps start with CISOs? Tara to start on this one.  Also possible cross-pollination area for software supply chain folks.
        - Also, possible discussions around eventing e.g. CD events as part of observability model (a la Open Telemetry)

## 19-October-2022
- Attendees: 
    - Terry Cox, 
    - 

- Agenda 
    - Best Practices
        - Assessment section requires content
        - Site metrics - issue
    - Reference Architecture:
        - Next steps

## 17-October-2022
- Attendees: 
    - Terry Cox, 
    - 

- Agenda 
    - Best Practices
        - Assessment section requires content
        - Site metrics - issue
    - Reference Architecture:
        - Next steps
    - Change of meeting day
        - Proposed to change meeting to Weds to permit co-chair to rejoin

## 3-October-2022
- Attendees: 
    - Terry Cox, 
    - 

- Agenda 
    - Best Practices
        - Assessment section requires content
    - Reference Architecture:
        - Next steps

## 19-September-2022
- Attendees: 
    - Terry Cox, 
    - David Bendory, Google
    - Kara de la Marck, CDF
    - Justin Abrahms, eBay

- Agenda 
    - Reference Architecture:
        - Terry reports that the basics of the reference architecture are now in place
        - PRs are invited for others to contribute
        - next up: look at business architecture -- how do you tackle the org change needed to facilitate the movement of development to continuous delivery?
        - Need for customer collaboration. Important that we have stakeholder viewpoints represented.
        - TODO: Kara to liase with Terry on blog post on current work and call for more input from more diverse viewpoints (eg, product developement rather than engineering).
    
## 5-September-2022
- Attendees: 
    - Terry Cox
    - Rajat Gupta

- Agenda 
    - Reference Architecture:
    
## 22-August-2022
- Attendees: 
    - Terry Cox
    - Mie Lieberman, Kusari
    - Kara de la Marck
    - Christoffer Vig

- Agenda 
    - Reference Architecture:
        - Views and Viewpoints update
        - Michael to look at audit and security views
        - General discussion of trade-offs between strong governance and agile delivery
            - Need to communicate inversion of model to rapid recovery over inevitable unexpected scenarios


## 8-August-2022
- Attendees: 
    - Terry Cox
    - Fatih Degirmenci
    - Andrea Frittoli
    - Parth Patel
    - Melissa McKay
    - Thomas Schuetz
- Agenda 
    - Reference Architecture:
        - Views and Viewpoints
        - Preview of template here: https://deploy-preview-23--prod-bp-cdf.netlify.app/architecture/
        - Branch for PRs here: https://github.com/cdfoundation/best-practices-site/tree/refarch1
        - Please reach out to stakeholders who can help

## 25-July-2022
- Attendees: 
    - Terry Cox
    - Kara de la Marck
- Agenda 
    - Progress on white papers:
        - No updates

## 11-July-2022
- Attendees: 
    - Terry Cox
    - Kara de la Marck
- Agenda 
    - Progress on white papers:
        - No updates from current workstreams
    - Need to update other project streams on site status and opportunities for white papers etc.
- TODO: Kara to find out about analytics on best practices site, following LF guidelines.
- 
## 27-June-2022
- Attendees: 
    - Terry Cox
    - Christoffer Vig
    - Tracy Miranda

- Agenda 
    - Next steps:
        - Focus on documenting community projects wrt best practice implementation
        - Evangelise within community and members to gain new contributors for this phase
        - Jenkins-X white paper explaining alaignment between best practice and JX features
        - Supply Chain Security white papers to fill in gap between theory and available tooling
 
 ## 13-June-2022
- Attendees: 
    - Terry Cox

- Agenda 
    - Next steps
 
 
## 29-May-2022
- Attendees: 
    - Tara Hernandez (MongoDB)
    - Terry Cox
    - Tracy Miranda (Chainguard)

- Agenda 
    - we are published! [site](https://bestpractices.cd.foundation/)
        - LF appears to be managing the tickets, check back in August :)
    - Tracy reminds us to submit ticket in foundation repo to redirect https://cd.foundation/ "Adopt Best Practices" link to new site.
    - Terry has an open PR for Security content, Tracy to review
    - Tara to start draft for Version Control section today
    - BOF Agenda:
        - Intro of Terry/Tara/Tracy
        - Intro to site, how to use it, how to update
        - Then, either Justin is there to workshop and/or we can get into interactive questions, e.g.
            - "What is the business driver for doign this at eBay (or participant organizations)"
            - "What are the key challenges from a business perspective"
            - "What are the key challenges from an org/cultuer perspective"
            - Perhaps setup polls around things like: "In the set of version control, automated testing, automated delivery to stage, automated deployment"
        - Scenario: "how do you do automated testing at scale"
                - how to decide what to automate, how to prioritize, e.g.
        - Scenario: "you build process/dev pipeline should be considered as a product in it's own right, requires sustainable investment -- how do you figure out how many resources you may need"
            - corollary: how do you help your org understand the build system is not just a necessary evil cost center, but a critical business priority.
        - Tara to create agenda doc, "group edit"

## 15-May-2022
- Attendees: 
    - Tara Hernandez (MongoDB)
    - Terry Cox
    - Moise Kameni (Hydro-Quebec)
    - Richard Kilmurry (Vodafone Group)

- Agenda
    - No response on domain bug, Tara to followup with Kara. Justin suggests using the magic [LF jira instead](https://jira.linuxfoundation.org/plugins/servlet/theme/portals/category/4).
        - Terry suggests we may need two tickets, one to get the domain registered/paid for, one to actually set it up so it appears as best-practices.cd.foundation.
    - Moise looking for info on developing landscapes, shared [CDF landscape source link](https://github.com/cdfoundation/cdf-landscape)
    - New tracking bugs for sections missing content, need to recruit more writers!
    - Richard is working on transitioning "old school" network management into cloud native solutions. He is looking to introduce CI/CD to networking group. He and Terry are going to do some initial followups offline.
    - For BoF, topic ideas:
        - Intro of the project
        - Overview of engaging in the discussion, planning and reviewing
        - workshop an example -- Justin's game to do it with eBay scenario.
    - Justin posted one-pager in Slack channel for eBay scenario, needs review, possible use case for BoF?
    - Terry suggests having some kind of set of interview questions, Tara suggests making it a template form/worksheet to help people organize their thoughts.  Could be a link on the Resources main page, e.g.

## 02-May-2022
- Attendees:
    - Tara Hernandez (Google)
    - Terry Cox
    - Tracy Miranda (Chainguard)
    - Anne Marie Fred (Red Hat)

- Agenda 
    - Requested public domain ([bug](https://github.com/cdfoundation/foundation/issues/375)), will followup with Kara.
    - Confirmed BoF at cdCon June 7, 10:50 CDT [schedule](https://sched.co/11b10)
        - Looking for example org/company uses cases that could go into the community section of best practices site.
    - Followup: Terry got update out to "why this matters" section preparing for Tracy's updates to security content.
    - Tara STILL to followup with Tekton team.
    - Anne Marie also giving a new overview [talk](https://sched.co/11TfB), let her know when the site is up.
    - New [issue](https://github.com/cdfoundation/best-practices-site/issues/10) created to track discussion around possible compliance section, needs owner.

## 18-April-2022
- Attendees:
    - Tara Hernandez (Google)
    - Terry Cox

- Agenda
    - Continuous Delivery section still has many outstanding questions, will submit as is (now that the chapter title is updated) so further discussion can happen more easily in subsequent PRs
    - BOF talk submitted (late, but in)
    - Clarifications for Terry on a "Why This Matters" related to securing a CD/CD pipeline, he also brings up we need a stronger set of narratives that tie key concepts together, e.g.:
        - why might some companies do continuous delivery without continuous integration -- Facebook model? "Just be able to revert fast if necessary".  Could also be examples at Netflix.  Meta discussion is where do you put the heaviest investments, and how reliable do your deployments need to be?  Cat videos vs. medical systems, your business goals should help dictate your pipeline function.
        - should also think about (future work) white papers/blog posting around specific scenarios 
    - Supply chain security doc still IP, suggestion to also include other related topics such as licensing, similar.


## 21-March-2022
- Attendees:
    - Tracy Miranda (Chainguard)
    - Nicola Yap (Google)
    - Tara Hernandez (Google)
    - Justin Abrahms (eBay)
    - Terry Cox (provacteur)

- Agenda
    - 3 current objectives:
        - finalze content migration. Some copy editing is needed to improve clarity (esp. Continuous Delivery section)
        - Really need to get with Kara et al to figure out publishing
        - Need more structured approach to soliciting use-case-based implementation examples with problem scenarios and corresponding tech stacks
    - Security
        - Tracy has working draft for security content [here](https://docs.google.com/document/d/1pGUgKw2RXFaSFH9IKIlTqDoIbK_3Ba2Rv5DSzZ83Q-E/)
        - Nicola notes that DevOps/DevSecOps/Security Software Supply Chain has a lot of overlapping topics, can we use frameworks like SLSA, NIST to help organize descriptions and concepts consistently.
            - What does "Shift Left" mean practically? i.e. how would you apply different security approaches at different levels of your pipeline
            - NIST is perhaps not as opinionated as it should be, hard to apply it because of this
            - SLSA might be better at getting people started, then NIST helps identifying things later on, i.e. vulnerability management, similar
        - Tracy suggests (seconded!) that having a TOC of the various frameworks esp. iterating which were best in what scenarios would be helpful.
            - might also be helpful to include sites like deps.dev as a tool for one's arsenal (e.g. help identifying security dependencies)
    - Current action items:
        - finish edits/review of current content https://github.com/cdfoundation/best-practices-site [current PR](https://github.com/cdfoundation/best-practices-site/pull/4)
            - Tara to replace "delivery" with "deployment" for now, will have subsequent review for consistency against definitions
        - Justin to finish PR for the eBay pipeline doc (current and proposed) and create PR for updates to learn/assess section
        - Nicola to talk to editor about contributing golden path example from Google (user study example)
        - Tara to start same for Tekton
        - Tracy to finish Security draft, speak to sigstore and other frameworks related to provenance/code signing etc.
            - Probably create some reference at least to OpenSSF and mention SBOMs
            - Terry to help with Why This Matters section?
        - Propose/discuss adding a new "compliance" category under "learn" section, TBD
        - Tara to talk to Kara about BOF (and also getting domain to publish)

## 21-March-2022
- Attendees:
    - Terry Cox


- Agenda
    - PR from Tara


## 07-March-2022
- Attendees:
    - Tara Hernandez (Google)
    - Terry Cox
    - Tracy Miranda (Chainguard)


- Agenda
    - Terry created PR to add user stories and video intro. Ready for review.
    - Agreed to focus on getting content from Google Doc onto site to build out structure
    - Once existing content is across, we should have a visible structure that will make it easier for others to contribute

## 21-February-2022
No meeting - public holiday


## 07-February-2022
- Attendees:
    - Tara Hernandez (Google)
    - Terry Cox
    - Nicola Yap (Google)
    - Justin Abrahms (eBay)
    - Tracy Miranda (Chainguard)


- Agenda
    - Mauricio's examples -- as they are from the book, should fall into the resource category
    - Justin's eBay example would go under community -- he will prep a PR for review 
        - We may want to consider additional templating (i.e. more functionally specific color palletes to identify different types of examples)
    - We should now start adding tags to be able to associate incoming examples with appropriate best practice principals
    - We are still missing the content for version control - Tara to take a look, anyone else feel free to jump in
    - Tracy to take a stab at Security page.  NIST has [released updated guidelines](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-218.pdf) that should be added to Resources. 
        - Resources should be organized and/or tagged by function, e.g. secure software supply chain, compliance, etc.
    - Justin and Tracy interested in helping with Assessments section
    - Tara to start migrating Testing and Delivery content
        - Anthony has moved on from Fidelity but Juan, Nick, Jimmy may still be interested in contribution
    - Tara to followup with Tekton team to see if there are examples that can be published over
    - Meta question: can we investigate having tools/policies that would allow vendors content teams to dual publish content to CDF as part of their product content strategy, similar to Google's contributions to Terraform, Springboot doc sites.
    - For publishing:
        - Kara can help connect with creative services.
        - Chris A. for helping with another logistics, though any logos that are [here](https://github.com/cdfoundation/artwork) are fair game.  
        - Any requests for foundation help can be submitted [here](https://github.com/cdfoundation/foundation/issues)
    - Terry to take a stab at organizing user journeys as a way of navigating readers to different content areas
    - From TOC meeting, various SIGs are pretty siloed, groups being asked to ensure there are reps for each SIG in TOC meeting.
        - Related topic -- SIG summit at cdCon? Tara will ping Kara to see what may already be in planning.
    - 


## 24-January-2022
- Attendees:
    - Tara Hernandez (Google)
    - Terry Cox
    - Nicola Yap (Google)
    - Vaidik Kapoor
    - Jalandar

- Agenda
    - Netlify process working session.  Steps!
        - Pull the source:
            - ```git clone --recurse-submodules fork-of-https://github.com/cdfoundation/best-practices-site```
        - Test locally via Docker container (maybe? might be better to use non-containerized local Hugo install). Steps here:
            - https://preview-site-cdf-bp.netlify.app/community/contribute/ 
        - Need to sort out dependency checking (local and upstream)
        - Regen netlify invites for Tara (incomplete registration)
        - Set up a tracking doc to capture any formatting notes or other site display/user experience - Tara to do this 
            - having text highlights enclosed in a box vs. just a orange line highlight
            - single page vs. multi-page content and supporting different narratifve paths through the content
                - multi-page gives advantage of bringing more detail to TOC and easier bookmarking
                - Nicola suggests being creative with tags as a way of helping with this.
        - There's apparently a way to invite 'reviewers' vs. 'contributors' to netlify, reviewers would be able to see and help with PR reviews without consuming a license.
        - We still need a proper domain/brand for the site as well 

## 10-January-2022
- Attendees:
    - Tracy Miranda
    - Tara Hernandez (Google)
    - Terry Cox
    - Nicola Yap (Google)
    - Ann Marie Fred (Red Hat)
    - Vaidik Kapoor

- Agenda
    - Mauricio looking to contribute this [repo](https://github.com/salaboy/from-monolith-to-k8s) to CDF, Nicola recommending including principles in main site, and under community section put explicit implemention examples.  Action item to followup on this next meeting.
    - Staging "preview" site now up [here](https://preview-site-cdf-bp.netlify.app/community/).  Tracy to add more contributors to CDF Netlify account so they can take advantage of using the staging functionality. 
    - Interoperability SIG and Tekton group has been kicking around glossaries and translations of terms and how they're used between different solutions.  Action item to come up with how best to incorporate this into info architecture.
        - [Glossary](https://github.com/cdfoundation/glossary/blob/main/definitions.md)
        - [Rosetta Stone](https://github.com/cdfoundation/sig-interoperability/blob/master/docs/vocabulary.md)
    - Also, we need to figure out a brand for the final published site.  Tracy will organize a followup meeting and is reaching out to strategy group for suggestions.
    - Ann Marie mentions that there are two PRs on the interoperability vocabularay content that are influenced by IBM's "One Pipeline" attestation process, describes the steps (and terminology around those steps) that can be useful for any company/project to conform to a regulatory attestation. The hope is that the phases (regardless of they may be described) can be viewed consistently.
        - https://github.com/cdfoundation/sig-interoperability/pull/76
        - https://github.com/cdfoundation/sig-interoperability/pull/81
        - Terry points out that that we may need to consolidate terms between Best Practices and Interoperability SIGs 
     
## 29-November-2021
- Attendees:
    - Tara Hernandez (Google)
    - Terry Cox
    - Anthony O'Gorman (Fidelity)
    - Justin Abrahms (eBay)
    - Nicola Yap (Google)
    - Jan Bultmann (Google)


- Agenda
    - Best practices site ready for contributors [cdfoundation/best-practices-site](https://github.com/cdfoundation/best-practices-site)
        - Nicola will include instructions on how to do local versions using Docker, will create auto publish probably via Netfify
        - Also agreement on things like image files use SVG format, to start 
    - Justin interested in capturing notes from engaging in DevOps best practices efforts at eBay -- first official use case?
    - Can we also come up with a good tagging model for documents to improve discoverability e.g.
        - "here's how Foo company assessed and improved their automated testing needs involving performance stress tests", is tagged to relevant section test best practices overview docs
        - Nicole thinks this is doable
    - Proposal to add some sort of discussion around organizational maturity and how that impacts approaches to continuous delivery and DevOps best pratices.
        - e.g. Agile product driven approaches vs. large legacy enterprise vs. cloud native/greenfield
        - Having ability to map a company to a model could help them understand best places to start?
        - [SLSA model](https://slsa.dev/levels) has concepts around this from a "security levels", could we expand this a bit possibly from the perspective of "what problems are you trying to solve, does CD/DevOps helps with this"
    

## 23-August-2021
- Attendees:
    - Tracy Miranda 
    - Tara Hernandez (Google)
    - Terry Cox
    - Anthony O'Gorman (Fidelity)
    - Jan Bultmann (Google)
    - Nicola Yap (Google)

- Agenda
    - review of information architecture [proposal-in-progress](https://docs.google.com/presentation/d/1mkkgDY3bS5E51kTItvsgj41wusx4xuO3O77HSAC-ERk)
    - Recommendation to use [CDF-defined personas](https://github.com/cdfoundation/outreach/blob/main/personas.md) for use case/workflow based context
    - Next steps:
        - setup of new docs repo, will go with docsy for now as it's being used by Tekton, Kubernetes, other projects.
        - start to identify possible content contributors from other member projects.

## 23-August-2021
- Attendees:
    - Tracy Miranda 
    - Tara Hernandez (Google)
    - Terry Cox
    - Anthony O'Gorman (Fidelity)
    - Jan Bultmann (Google)
    - Nicola Yap (Google)
- Agenda:
    - [Jamboard hacking](https://jamboard.google.com/d/1FOTPWL_dzQXWH0cJKB0OCO267XNEYLX_SN4ppiQ4HHs/) for site layout
    - Welcome Jan and Nicola, pro content developers to help build out the [site](https://cdfoundation.github.io/best-practices/) with regards to content strategy, contributor workflow recommendations, etc.
         - Nicola suggests something like the [Slsa framwork](https://github.com/slsa-framework/slsa) could be useful.
    - New todo: establish "personas" or "role archtectypes" that can be used as a way to flag particular content
    - Terry has started adding MLOps content, looking for comments
    - Anthony and Juan have added some additional content to test sections, also looking for comments.
    - Also need to get Nicole and Jan added to CDF github org.

## 09-August-2021
- Attendees:
    - Tracy Miranda 
    - Tara Hernandez (Google)
    - Terry Cox
    - Juan Flores (Fidelity)
- Agenda:
    - [Jamboard hacking](https://jamboard.google.com/d/1FOTPWL_dzQXWH0cJKB0OCO267XNEYLX_SN4ppiQ4HHs/) for site layout
    - More updates and requests for review/feedback in testing section of [best practices doc](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza)


## 14-June-2021
- Attendees:
    - Christie Wilson (Google)
    - Gopinath Rebala (OpsMx)
    - Tara Hernandez (Google)
    - Terry Cox
    - Juan Flores (Fidelity)
    - Anthony O'Gorman (Fidelity)
    - Chris Riley (Splunk)
    - Siddharth Pareek (NatWest Group)
- Agenda:
    - Best Practices BoF at cdCon
        - https://sched.co/jn3J
        - Terry and Tara to moderate
        - Thursday, June 24 • 2:55pm - 3:25pm EDT
        - Terry and Tara meeting tomorrow to talk about BoF topics (message Tara if you want to join)
    - Anthony and Juan to drive Continuos Testing and ask for feedback :)
    - An expanded survey to find a good time for everyone: https://forms.gle/RFbn4WBJHGUqb2of6
        - Currently 2pm EST works for 4/6 ppl
            - Not a good time for India (midnight)
                - Should we rotate times, one that works for folks in India as well?
            - Also a challenge for Ireland
        - Maybe we can use this survey for the next quarter, do another survey with expanded times to find an alternate time? (then alternate b/w 2 times?)
    - DORA metrics, telemetry
        - Information architecture
        - Can't just have a "DORA button"
            - Folks are comparing metrics when services are not apples to apples
            - Common Information Model (CIM) for CI/CD telemtry
        - Best practices such as: ticket numbers in commit messages
    - Workshopping [best practices doc](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza) - 2 tasks:
        1. Look for missing topics
            - Possible topics:
                - Pipeline metrics are the foundation of devsecops
                    - Security in the SDLC?
                        1. Build more secure apps (sonarcube, etc.)
                        2. Secure the factory (e.g. secret access)
                        3. _______ (secure the artifacts?)
                        4. Secure production
                    - Too specific?
                        - Currently have a TODO item for security in the context of governance in the doc, could follow up with specific examples in hands on portion of doc
                        - Feel free to make contribution
                - Adding a section about what kind of setup do you need to do to be able to do calculations
                    - Overlap with SIG events? interoperability?
                        - Common information model
                            - Security world has this
                                - (SIM) security information management
        2. Keep fleshing things out and reviewing
        - Looking for feedback on [continuous testing section](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#bookmark=id.ey705iffr53i)
        - Personas
            - Relevant factors, makes "role" tough:
                - Size of company
                - Whether company develops inhouse or hires vendors
        3. Be sure to join [sig-bestpractices Slack channel](https://cdeliveryfdn.slack.com/archives/C01FQA6890D)

## 17-May-2021
- Attendees:
    - Tracy Miranda
    - Terry Cox
    - Siddarth Pareek
    - Tara Hernandez

- Agenda:
    - Looking at results for survey about time: https://forms.gle/fqtVGCrm2uFsUxmh8 (Christie can't attend today but Tracy Miranda and Tara should have edit access@)
        - Results so far: 9am PST / 12pm EST is the top choice, but only for 5/7, if anyone absolutely can't do this time plz mention this, we can expand to include other days
    - Looks like we should have a BoaF spot at cdCon, Tracy to confirm date/time (hopefully a time that works for Terry)
    - Need an outline "content/copy" -- set of links to github/docs that a landing page can point at for all working groups/SIGs.
        - Capture idea of "personas" for which content can be tailored, e.g. an exec level explanation vs. a developer level.
        - Suggestions from outeach committee: https://st1.zoom.us/web_client/f3jfhf/html/externalLinkPage.html?ref=https://github.com/cdfoundation/outreach/blob/main/personas.md
            - Possible exercise, flag the [best practices doc](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza) with the persona categories/roles?
        - Terry added "Governance" and "Instrumentation/Telemetry" categories for key talking points
    - Tracy shared the "Measure DevOps" paper from End User Council as a model for organizing best practices content.
    - Next meeting, start work on info layout via https://miro.com/ (can also be used by hopin conference platform)


## 03-May-2021
- Attendees:
    - Christie Wilson
    - Terry Cox
    - Tara Hernandez
    - Gopinath Rebala

- Agenda:
    - IEEE have launched a standard for devops: 2675
        - https://standards.ieee.org/standard/2675-2021.html
            - - https://www.researchgate.net/project/IEEE-2675-DevOps-standard
        - Launch meeting: what is devops? hard to answer!
            - Any opportunity for us to help out?
                - Terry Cox is going to be in next sitting of the working group
    - What is our Best Pratices audience?
        - Needs to be everyone; way we provide the info is almost as important as the info itself
            - Need to be able to read the info at the context/level that is relevant for you, without
              having to leave
                - Individual implementor vs. decision maker, need different granularity of detail but
                  it's all part of the same story
                - Important to go both broad and deep
                    - Need to drive solid awareness regardless of your role
    - Process that leads to these methodologies:
        - Startups are motivated to innovate (e.g. silicon valley)
        - These folks move around to different companies, spread the ideas around
        - Media hears about it, spreads the ideas, gives it labels
        - People start trying to apply the methodologies but without the context they need
            - Why are we doing this and in what circumstances
        - People say 'this is the next big thing' but it's not working, so they fiddle with it
          and redefine it, and then it means what they're already doing
    - [Best practices doc](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza)
        - Can we create this multi directional context for each bit in the doc?
            - e.g. "deployment frequency", frame this at both levels
                - exec level + technical practioner level
        - Narrative: hero's journey
                - Start with: this is the problem we're trying to solve
                - Refusual: i dont want to do this
                - Realization : i have to engage with this
            - Need to flesh out the journey so it's easy to understand
        - What kind of assumptions can we make about folks coming to the CDF?
            - e.g. Christie in her book assuming people have some tests/unit tests
                - Tara: last company, folks saying "can't write tests yet, not done implementing"
        - Next steps?
            - Create a [scratch section](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#bookmark=id.70jtt4iov1il)
              that reminds us what we're trying to flesh out
            - Views + viewpoints, depending on who the stakeholder is, they'll have a different
              perspective
        - Making organizational change happen
            - So different for different departments; some inherently invested in the status quo
            - At an exec level: things like, retraining, paying for vendors
        - Realistically many organizations will not be able to implement devops
            - Don't want to paint ourselves into a corner
            - Maybe from the perspective of folks moving into microservices and the cloud, vs for their
              huge quantities of existing software
            - Start with: contexts in which devops was designed to be used, for our first iteration
                - Not trying to boil the ocean; consistent story
                - Next: implications of wanting to introduce some elements of devops to existing software
                  and processes
                - Mismatch b/w ppl who think they are doing devops and folks who are actually capable
                  of doing devops
        

- Action Items:
    - Christie can send survey about different time (more PST friendly hopefully?)

## 19-Apr-2021
- Attendees:
    - Christie Wilson
    - Kara de la Marck
    - Tara Hernandez
    - Terry Cox
    - Tracy Miranda
    - Gopinath Rebala
    - Siddarth Pareek

- Agenda:
    - Updates to [best practices doc](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza) by Terry Cox
        - Specifically narrative lead in: why ppl need to be doing best practices, contexts, etc.: [Understanding the problem](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.o7uo3njnwqti)
        - Related effort: presentation around 4 key DORA metrics, etc., Tracy Miranda doing a write up, includes similar topics, Tracy to look at how to combine the contents
        - Thinking about audience: technical ppl already deeply involved (i.e. can skip a lot) vs ppl who know it exists but are missing the background that drives the reasoning
        - Tracy would like to create a blog post from some of this content early and get feedback
            - First need agreement on picture trying to paint and style
        - What is the scope of this doc? CI, CD, deployments, etc.?
            - All of it
    - Tracy merged [initial CD definitions](https://github.com/cdfoundation/glossary/blob/main/definitions.md#continuous-delivery-definitions), planning to give these a trial run
        - Context of these definitions? Alignment with best practices doc?
            - Can see history in PRs + doc links in those descriptions: https://github.com/cdfoundation/glossary/pulls?q=is%3Apr+is%3Aclosed
                - WIP to finesse the definitions in the best practices doc and the glossary to be aligned (see comments in doc)
    - Do we want a Birds of a Feather at cdCon?
        - yes, what scope? e.g. dora metrics as well?
            - Mulitple audiences, makes sense to have a general session and more targetted sessions
                - e.g. 100 + 400 (intro and advanced tracks)
        - anything specific to cover? or general?
            - e.g. branching and merging strategies, or at the level of "CI", "deployments"
                - branching: do you develop in a branch or on mainline with feature flags
                    - entire discussion worthy of its own category
                    - process for getting started, vs. benefits you can buy with a more complex strategy
            - could be interesting to talk about all the different ways folks are approaching CD and adopting it
            - justifying CD to management with a better argument than "because netflix"
                - Huge mismatch in communication around what it takes to effectively use CD
                - Need to provide the entry level communication for ppl to grasp onto so they can start on this journey (in addition to providing the more advanced info)
        - how long until cdCon?
            - 1 month
        - CDF should be able to speak to the maturity of "all the things" entailed in developing a software delivery lifecycle
            - can we do an industry survey to see who's using what (as far as tools, processes)
            - github, stackoverflow surveys may have some of this data
        - Siddarth raises the issue of compliance as a critical element that needs focus, particularly for high regulatory industries like finance and healthcare
            - Terry points out that many companies are more heavily invested in manual approaches to this (and in fact may cause resistance to automating this due to perceived negative impact on job security).
            - Interoperability SIG has started exploring this idea, looking at https://github.com/open-policy-agent/opa e.g. We probably want to have security compliance as its own set of sections in definitions and best practices.

- Action Items:
    - All to please review [Understanding the problem](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.o7uo3njnwqti) **by end of the week**
    - Please take a look at [initial CD definitions](https://github.com/cdfoundation/glossary/blob/main/definitions.md#continuous-delivery-definitions), discussions are on in the repo for feedback (or comment on original PR)

        - 

## 08-Mar-2021
- Attendees:
    - Tracy Miranda
    - Thomas Schuetz
    - Terry Cox
    - Siddharth Pareek
    
- Agenda:
    - Christie can't attend, can someone else handle [the agenda and notes?](https://hackmd.io/uxoIwj7fTjKkI161-IZeFw)
    - [CD definitions](https://docs.google.com/document/d/1IUSmgtw5eC2JwyfiX7IPK3twl3MSjWAsmCKmJ6Y5z-w/edit#)
        - Christie created an initial PR: https://github.com/cdfoundation/glossary/pull/10
    - [Best Practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza) should become the methodologies used to define the definitions from the CD definitions docs 
        - This needs the 'why' and 'definition' sections completed before we push it to the repo/markdown
        - Terry Cox has reference docs that he can pull a lot of these out
        - Another concept to consider: "scale appropriate fit" as it pertains to size of the problem. e.g. a single Jenkins instance can easily support a small to medium size team.  You also wouldn't use Spinnaker in a small to medium scoped problem. Can we create guidance to help evaluate their needs. Another element of this is understanding the evolution of this -- it's done in steps promted by growth of the team/product size as well as the advancement of technology.
- Action Items:
    - Terry Cox will update Best Practices doc on "why/definitions"


## 22-Feb-2021
- Attendees:
    - Mauricio Salatino
    - Christie Wilson
    - Tracy Ragan - DeployHub
    - Thomas Schuetz
    - Tara Hernandez
    - Kara de la Marck
    - Anthony O'Gorman
    - Tracy Miranda

- Agenda:
    - **Welcome Thomas Schuetz!**
        - From Dynatrace
    - **[HackMD agenda doc](https://hackmd.io/uxoIwj7fTjKkI161-IZeFw)**
        - Updating the calendar entry with the link (anyone with access to the calendar can do this)
    - **[Best Practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza) next steps?**
        - Content from Tracy Ragan, Tracy Miranda content TBD
        - Goals:
            - People can identify the "track" that best suits them (e.g. highly regulated, 10 person team vs large org, moving to cloud vs sticking with traditional platforms)
                - Assuming not one size fits all
            - Highlighted key areas that are part of continuous delivery
                - Ideally ppl can look at the list and see where they are at; live maturity model
            - Useful list for evangelizing key practices in your organization
        - Tracy Ragan:
            - This group can't do all of the above, needs to be pushed to community
            - Need to start a framework, bring in ambassadors, end users, to expand
                - Website is key
                    - Need to create a brand around the CD foundation, align ourselves as thought leaders and go to place for information
                        - Confusion in the industry, e.g. forbes article, ppl confusing Continuous Delivery and Continuous Deployment
            - Description + scope = boring, wanted to frame as a story to have more context and depth
            - Docker specific best practices: maybe need to have a different category for CI/CD in a docker world
        - Next steps:
            - Add comments?
                - Prefer just changing it directly + rewrite it
                    - Suggestions? Need some kind of review to make sure we're on the same page
                        - Create a basic structure = fine
                        - This group can't create this info, need a bigger approach, beyond our walls, need to bring in more eyes
                            - Create a process for reviewing and approving PRs?
                            - Need a small group to put initial content forward
        - Thoughts from newer folks, how does this fit with your expectations? (Anthony)
            - Anthony: Problems currently: e.g. getting branching strategy up and running (lots of different opinions), how does that work with CI/CD going forward, how do you apporach a pull request
                - Wish something like this already existed! :D
            - Anthony: Docker containers: a bit specific, depends on what you're doing at what stage
                - multi stage docker build = important conversation, changes workflows
                    - CDF = exciting right now b/c things are in flux, don't want to get to stuck in the past, i.e. cloud native vs traditional
                        - Should have whole section on cloud native CI/CD
                            - To reduce scope = don't try to do both
            - Much bigger project: need to get it out there to more ppl
                - ppl in different industries will have completely different ways of doing things and guardrails
        - Everything is so connected, hard not to define something (e.g. CI vs version control section), hard to talk about one section without referring to another
            - Just focus on definitions
        - Website
            - = best practices?
                - Just way to present best practices?
                    - Website can have history, etc.
        - Best practices don't belong here
            - Best practices are siloed by industry, defined by verticals
            - Create standard doc with definition and scope
                - What is version control, what is CI, what is CD
                    - Create a way for best practices to be expanded by industry segments
                        - Website = create open source community to write this via pull requests
                            - This group reviews PRs
                            - Funds for having other ppl do the editing?
                            - Don't just want us to curate the info
        - Can use this group to determine:
            - Structure of this information
        - Does take curation and structure to have something that is contributed to by so many people
            - Balance between: making it so folks can contribute, and keeping it focused
        - Thoughts from newer folks, how does this fit with your expectations? (Thomas)
            -  Thomas:
                -  Would love to see best practices for CD
                -  Many questions:
                    - Versioning + Continuous testing, when are you testing against which version, how can you guarantee that you test every contribution
                - Many people talk about these things but very hard to get the info you need
                - Currently working on a whitepaper about operators in the CNCF, hard to get ppl to contribute, in the end = hard work of few people
                - Agree that most needed = best pratices for CD in cloud native?
                    - Yes
                    - Mauricio: can start with definitions, ask ppl to chime in with their experiences
                        - Website: to start a discussion, need to have something to refer to
        - Are we interested in having example use cases or user stories?
            - e.g. Jenkins X has a nice way of handling testing version streams
            - Yes, every section should have case studies and tool based best practices
        - Need to pick the most impactful categories to detangle
            - Fill in A, B, C of the doc, then come up with a strategy for D and E
                - Won't be easy to get ppl to contribute, but building end user council, there are lots of ppl who want to be ambassadors
                - Once we have A, B and C, we can create some blog posts
                    - Do more evangelism?
                        - Keep it low key until we have a structure that makes it easier for ppl to contribute
        - Verticals, e.g. different areas such as MLOps, every group should be able to take our fundamentals (A, B, C) and be able to have their own best practices
            - = this is how we know we've succeeded
        - Need to figure out what table of contents will look like
            - Starting point = [Best Practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#heading=h.9ji2tp1suza)
                - Best practices should be broken up by industry (e.g. insurance, embedded, health care)
                    - Each vertical could have its own whole document, with it's own definitions
                        - White paper for each, e.g. verison control for finance
                        - Each has own neighborhood to have a conversation about what they think CD is
                            - e.g. gamers vs startup 
                                - What makes a startup different? size, budget, speed, reliance on open source
                                - What about ppl writing Python, etc.
        - Feels like we are increasing the scope a bit, start with A, B and C?
            - There will be a lot that verticals will have in common (e.g. running unit tests)
            - Get a basic structure out there
            - Have a strategy for how this can grow over time
        - Create an outline for best practices for CD for cloud native
            - Create an MVP, what would you have to do to make this apply to finance
                - Have more access to finance folks at the moment
            - Proposal:
                - 1. ABC lowest common denomniator best practices (regardless of industry)
                - 2. Continue discussing how to bring in the broader community in an open, transparent, everyone welcome way
        - Broad forums on advertised topics ahead of time? e.g. having someone come in and talk about how they are doing each
    - **Update on CI/CD Events Vocabulary new SIG**
        - Mauricio has been joining this group, have been pushing for describing the vocabulary for events
            - First meeting tomorrow with someone from Tekton
            - Want event category definition, event format, event content
        - Related: events that different tools use, how do these correlate with best practices
        - Standardized format = easier to discuss
        - Couple of ppl from Dynatrace in events working group also
    - **How to encorporate Best Practices into website updates**
        - (covered in best practices discussion?)
    - Do we want to convert [best practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7) to a markdown?
        - Can be easier to comment in doc in early stages
            - vs. PRs and discussions don't seem to get as much traction
        - hackmd?
        - maybe get all the ABCs into a clean doc, then convert to markdown and commit
            - Maybe include lowest common demoniator best practices; at least to have best practices section

- Action items
    - Update SIG best practices calendar with link to [HackMD agenda doc](https://hackmd.io/uxoIwj7fTjKkI161-IZeFw)
    - Please comment on and update [best practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7)

## 08-Feb-2021
- Attendees:
    - Tracy Miranda
    - Tracy Ragan
    - Christie Wilson
    - Tara Hernandez
- Links:
    - [Best Practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#)
- Action Items:
    - Start filling in [Best Practices](https://docs.google.com/document/d/1DojwSRqlTrAoxfE6jp2U4_SIzpefGRfu1OhKYc6_-nQ/edit?ts=602167a7#):
        - Version control, security/devsecops: Tracy Miranda
        - Continuous Integration, Continuous Deployment, Configuration Management - Tracy Ragan
        - Continuous Testing - Tara

## 25-Jan-2021
- Attendees:
    - Tracy Miranda
    - Kara del Marck
    - Tracy Ragan
    - Christie Wilson
    - Mauricio Salatino
    - Tara Hernandez
    
- Links:
    - [CI/CD Definitions](
https://docs.google.com/document/d/1IUSmgtw5eC2JwyfiX7IPK3twl3MSjWAsmCKmJ6Y5z-w/)
    - [Tools/Terms Timeline](https://github.com/cdfoundation/glossary/blob/main/timeline.md)
    - [CNCF Demo Project](https://github.com/cncf/podtato-head)
    - [Cloud Native Scenarios for CD](https://github.com/cdfoundation/sig-best-practices/blob/main/scenarios.md) *Mauricio is looking comments on this*
    
- [CDF End User Council Plan](https://github.com/cdfoundation/end-user-council/blob/main/End%20User%20Council%20Plan%202021.pdf) is focusing on Measuring DevOps Success (e.g. DORA key CD metrics) theme for 2021 Q1
    - best practice SIG would partner with this by providing resources on case studies around these topics -- there are surveys now to try and get more info around this [https://github.com/cdfoundation/end-user-council/discussions](https://github.com/cdfoundation/end-user-council/discussions)
    
- Action Items:
    - ALL - Provide comments for [Cloud Native Scenarios for CD](https://github.com/cdfoundation/sig-best-practices/blob/main/scenarios.md) 
    - Tara/TracyM/TracyR - create new Github Pages for organizing our mass o' info -- add additional timeline reference that calls out keys technologies to help provide additional context.

## 11-Jan-2021
- Plan: workshop CD Whitepaper topics

## 14-Dec-2020
- Mauricio has started use cases with a focus on what gets impacted when you make changes in a tech stack.  Will be following up with Interoperability SIG with regards to Events (which will probably be broken out into its own SIG)
    - Will review some of the talks from CDCon with related content, followups next year
- Christie has started a timeline of terms and when they came into existence, has a [PR pending review](https://github.com/cdfoundation/almanac/pull/1)
- Also, should review the list of topics in the [CD Whitepaper]( https://docs.google.com/document/d/1aZT__F57g1BMPzpsV6RAC86k_FfetkAWMhdVT22PZrM/edit#heading=h.ayrusou2822c)
    - Can we refine existing list more usefully?  Next meeting will work on this.
    - Still need to organize the Ambassadors and/or determine whether we have sufficient data from members about their CD proccesses


## 30-Nov-2020

- Setup new SIG repo, ACLs! 
    - Tracy M to setup a Youtube playlist for future 'best practice' videos 
- Should followup w/Jacque about soliciting Ambassadors regarding generating list of case studies from respective organizations. 
- Mauricio to post his WIP notes to repo
