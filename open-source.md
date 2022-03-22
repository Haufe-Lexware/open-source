## Open Source

### Why Open Source?
Open-source software (OSS) is a software development model that underpins many Haufe Group products and most of the technology products in our everyday lives. At Haufe Group, we choose to develop and use OSS for the following reasons:

* **Culture**: We are fundamentally invested in sharing.
* **Trust**: We believe in the tight bond of trust OSS engenders between the company, our developers, and the broader community of users.
* **Quality**: We benefit from a community of developers who will test the software we build.
* **History**: History has proven that open standards win (e.g. HTML, WebKit, USB, Wifi).
* **Recruiting**: Smart people attract other smart people.
* **Portability** (No Lock-in): Developers want to know that the tools and applications they make are not tied solely to the success of a particular company.
* **Reuse**: Let’s not reinvent the wheel!

### What we tend to open
We believe in putting powerful tools in the hands of developers. In many cases, this means open sourcing what we are working on early and often in accordance with our policy and core values. When contributing to other open-source projects we strive to follow best practices and licenses set by that open source community. As a rule of thumb, we will open source, under various licenses, the following types of software:

* **Generic tools**: A tool, library, or other utility that solves a generic problem
* **Non-core**: Software not part of our core value proposition as a business
* **Discretionary**: Code that we collectively decide provides greater value to our community of developers than the incremental value it may provide to Haufe Group if kept proprietary
* **Derived work**: As it is often faster to develop using open tools, we correspondingly open derived works based on those tools in adherence with the license terms and conventions.

### How we do Open Source

#### General
Open Source is a commitment and entails responsibilities. It is not 'dump it and leave it'. **It is also a statement about our company -  What we value and how we work.** No one likes to live on a street with broken glass, abandoned houses and litter everywhere. Similarly, our Open Source should reflect our professional attitudes and aspirations.

Nothing is more frustrating than getting excited about some tooling or code and tripping over outdated documentation, debugging broken code or outdated dependencies. 

So, think before you act. Open Source is valuable to us because it reflects dedication to sharing and professionalism in maintaining we aspire to in our daily work. If you want to do Open Source, you should hold yourself to the same standards.

#### The Process

- [Get Approval](#get_approval) - Submit a request to open source to the Head of Technology of your business group.
- [Use Github](#use_github) - Request a repo on our corporate Github account
- [Document and Test and Build](#document_and_test_and_build) - Check in your code, add automated testing and wire it up to our external CI/CD pipeline
- [Review](#review) - have someone unconnected to the project review it to make sure it is actually usable. 
- [Engage](#engage) - Blog, tweet, publicize and evangelize. This is when the fun really starts.

Now you have published your first open-source project, but you are not done. Continue reading [here](#fight_entropy).

##### Get Approval
The first step to open-source code from Haufe Group is to get the necessary executive level approval. This is as simple as sending an email to your Head of Technology explaining:

* What you want to open source, 
* Why you want to open source it
* And, a justification that it is not valuable intellectual property (IP) or business critical

Since we follow the 4-Eye Principle for approvals (Vier Augen Prinzip),  it is the responsibility of the executive to discuss the request with at least one other person, like the head of the Line of Business. That person should be knowledgeable enough on the subject to have an informed opinion. It is also  the responsibility of the executive to inform the head of our legal department (LD) if necessary. 

The response to your email should clearly state who was involved in the decision-making process and a statement if it is approved or not. If it doesn't, ask for the necessary clarifications. 

Once you have the approval, you can now proceed to open source the assets.

##### Use Github
All of our open source is hosted on our [corporate Github account](https://github.com/Haufe-Lexware). You can request a new repo from our [Release Engineering (RE) team](mailto:_DevInfra@haufe-lexware.com).

Our standard license for source code is Apache 2. Please use the standard `LICENSE` template provided by Github and place it at the root of your repo.

##### Document, Test, and Build
Once you check in your code, add automated tests, and hook it up to our public CI/CD pipeline for automatic builds, the RE team will be able to help you. 

If your code is also used internally, do not deploy from your public Github repo. Use a separate repo on our internal version control system and deploy it internally via our internal CI/CD pipeline from there. This introduces a so called [air gap](https://en.wikipedia.org/wiki/Air_gap_(networking)) between our publicly available open source and our internally deployed systems. The internal repo should **not** automatically replicate all changes on the public repo. Instead each merge from the public repo to the internal repo needs be manually reviewed to avoid potentially compromised code from being deployed internally. 

**All of our internal systems are built and deployed using our internal Gitlab repo and internal CI/CD pipeline. All our public source is built and deployed using our public Github repo and public CI/CD pipeline. All changes on the public repo are reviewed before merging to our internal repo. No exceptions.**

##### Review
Before it gets published, schedule a review by someone who is unconnected to the project. His or her responsibility is to make sure your source is usable **without your help**. Any issues should be tracked in the issue tracker of the repo. Anything marked as "blocking" must be resolved before it can be published.

##### Engage
[If a tree falls in the forest ...](https://en.wikipedia.org/wiki/If_a_tree_falls_in_a_forest) No one will know about your awesome project unless you let them know. Engaging the community can take multiple forms: you can blog about it on our [developer blog](http://dev.haufe-lexware.com), [tweet](https://twitter.com/haufedev) about it, present at conferences, reach out to industry analysts and evangelists, etc. pp. Just don't fool yourself into thinking [that if you build it ...](https://www.entrepreneur.com/article/227850), they will come. 

And, if you get questions, comments or - the largest reward of all - active contributors, treat them as you would like to be treated. Always be professional, and helpful. If folks ask seemingly simple questions over and over again, it is a sign that you urgently need to update your documentation. 

**It is your responsibility to make anyone engaging and contributing feel valued. Open sourcing code is not about you, but about giving back to the community, which we are all part of. Treating any single member of the community as a 2nd-class citizen reflects back on our company and our own values.**

As we wrote above, there is no higher appreciation for your open source project than others contributing to it because they see value in it. In order to protect the integrity of the code released under the Haufe Group name, under the Apache 2 license, we ask that contributors submitting pull requests sign a [Contributor License Agreement (CLA)](https://gist.github.com/DonMartin76/b35182c830fad771d31e2cd98be2b9ac). Our CLA is s a derivative from the [GitHub Contributor License Agreement](https://cla.github.com/agreement), used with GitHub's permission under the [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) license. Please add an explicit reference to the CLA to the customary `CONTRIBUTING.md` file in the root of your project and configure the freely available [cla-assistant](https://cla-assistant.io) to enforce acceptance of the CLA for pull requests to your project repo (you can find a sample pull request [here](https://github.com/apim-haufe-io/wicked.portal/pull/8)).

#### Fight Entropy
Code not maintained is dead code. This is also true for open-source projects. We expect you to be a responsible owner and maintain the code while engaging the community and representing our company to your best abilities. This is the basic bargain we offer in return for open sourcing code and making a name for yourself in the community.

As with everything, code gets stale, technology moves on. It is ok (and expected) that only very few repos will have an active lifespan of more than a year or two. In order to avoid accumulating dead code and repos, we need to be committed and diligent in fighting entropy but also must take down repos which have not seen significant activity. This is especially true for repos with code not used internally.

#### Moving on
There is a time when we all move on. Either taking a new role, or a new job or otherwise not being able to maintain the commitment to your open-source project anymore. **It is your responsibility to find a new owner or - if that is not possible - put a clear message into all relevant parts of the documentation, project README etc. that the this project is unmaintained and should not be used any more.** Do not rely on others to clean up after you. 
