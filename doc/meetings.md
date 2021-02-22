## 08-Mar-2021
- Attendees:
- Agenda:
    - TBD
- Action Items:
    - 

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
