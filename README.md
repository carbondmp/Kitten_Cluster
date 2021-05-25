# Kitten Cluster ('Kitten' for shorthand)

Knitting Interconnected Technical Tenants Enumerating Nonconformities 
Coincidedly Labeling Unrelated Standards Towards Effective Remediation


## Why Do We Need This?

- Fallacy of Equivocation on the word ‘privacy’ creates ambiguity
  - The sky is blue. What is blue is not happy. Thus the sky is sad.
  - Privacy is good Privacy is tracking with consent. Privacy is aggregate only tracking. Privacy is eliminating all tracking. Privacy is …. Good? What is privacy???
- Leads to Classic ‘Motte and Bailey’ Discussion
  - Person A (Motte) : A safe is a private thing. We should put the internet in a safe! 
  - Person B: No, this is neither possible nor prevents a user’s information from leaking.
  - Person A (Bailey): That’s a philosophical argument and has nothing to do with privacy. 
- Result is confusion, no productive discussion can occur

Provides 4 Uses

- The Privacy Definitions
- Self Consistency Analysis 
- Overarching Proposal Unity Analysis
- Contrary Proposal Analysis


## Short Executive Summary

Here we offer a standard for evaluating a web privacy proposal's actual privacy offering.

This proposal does NOT seek to define privacy itself, or give guidance as to which definition of privacy is best.

Privacy inconsistencies and trust violations are made more easy to Identify, Discuss and Correct.

## Executive Summary Continued

A method of detecting privacy violations **within the definition given in the individual proposal** is detailed. Methods of analysis and correction of these inconsistences are also detailed.

Ongoing W3 proposals and github issues filed in the repos of those proposals that have not been resolved under the specifications of Kitten Cluster may be tracked in the directory structure.

A method for a however to self-describe this evaluation is also given, though those neutral to or detracters from a proposal are encouraged to maintain tracking to increase fidelity.

A proposer-written Privacy Definition should be in a PrivacyDefinition.Md file in the primary proposal repo. A third party Analysis (especially one disagreeing with the self-analysis) can be performed as PRs to this repo, if there are conflicts. This will be noted on the PrivacyDefintion.md fle in this repo.

Privacy definitions (defined below) are the core of this communication and analysis model. The directory structure for this repo has an Overarching Privacy Defintion directory which contains various and distinct privacy definitions subscribed to by  W3 particpants. Very light examples are presented in the form of 'Red' and 'Blue' color privacy models until proper proposals can be added by way of example.

Snakes (threats, concerns) should be filed as issues and linked on the appropriate MD. EAch proposal should have a "## Contrary Proposals" with no bullets if none exists, and a "## Consitency Snakes" section for privacy threats inconsistent with a proposer's own definiton. Other threats should be under a "## Troublesome Snakes" header for side-effects, practical consequences, and misc concerns unrelated to the proposer's own privacy definition.

A "## Unity Snakes" should be applied to the overarching privacy deifnition's PrivacyDefinition.md

Snake resolution is best done as W3 discussions. 

## 1 Definitions

Each term defined here is explained in greater detail in the explainer. Section 1 merely exists to make reading the explainer easier as the terms will have been seen before.

### 1.0 Kitten

Shorthand for the  Kitten analysis tool. 

### 1.1 The 'Proposal'

The word 'Proposal' is always used here to indicate the privacy proposal being analyzed. Examples: Floc, SWAN, PARAKEET, etc

Thus "Proposal" would mean "floc" if floc were being analyzed.

### 1.2 Violation

A violation is piece of the Proposal that contradicts its own definition of privacy, or in some way endangers privacy (as the Proposal defines it). A violation could also threaten communication (clarity violation) or industry fair play (trust violation)

The goal of  Kitten Cluster is to find, discuss, and fix violations. When not possible, the goal is to generate clearly communicated discussions.

## 2.0.0 Analysis Tool

This tool is intended for use by third parties seeking to evaluate a proposal, but can also be used by the Proposal owner themself. To achieve greater fidelity, evaluation of third parties is encouraged.

### 2.1.0 Privacy Defintion

Here the standards for a proper privacy definition are described. These standards exist to prevent confusing or deceptive wording. 

A primary goal is to force disussion towards a USER FOCUSED persepctive by focusing on DATA over technical specs. A good definition will make it clear what data is protected, when, and how. 

The first part is the Overarching definition. This can be shared by multiple proposals. It should use 'We believe' language where possible to show it is an opinion.

The second part is the proposal specific section. It should use 'we intend' language and refer to the goals in the overarching definition. 

Further details are described below:

#### 2.1.1 Private Data Class Description

Each 'class' of 'private' data should be outlined as clearly as possibe.

Bad class description: Browsing Data

Better class description: A list of domains visited by the user. One domain is considered a list of one. A null list indicating the user has not browsed is considered a list of 0.

See how the better example makes it very clear what data is being discussed and accounts for  edge cases. These may get quite large, mostly due to edge case descriptions, and that is good.

A user can clearly know what data is considered private from this proposal.

#### 2.1.2 Disallowed Data Class Transfers

For each class of data, it should be clear what can be done, or not done, with the data.

A. "Player Specific" language should not be used here. This includes language such as 'ssp, publisher, browser.' Any company that has the ability to profit off of data is a player. Including such language leaves rooms for certain player types to **violate a user's privacy.**

If your proposal needs a player to get  special access to a class of data, try instead to provide a mechanism where all players that meet a set of requirements can access that class of data. It 'may' be acceptable if only one type of player can meet those requirements in practicality (see Privacy Violation) but the option MUST be open to all players or none. The inability to avoid player-specific language could indicate anti-competitive behavior and is considered a trust violation.

B. "Business Specific" language should also not be including. Restricting data for only some business cases such as 'advertising' provides other use cases (valuable data science, data sales, etc) a loop-hold to **violate a user's privacy** and also created market discrimination. (See Privacy Violation)

C. Any other discriminatory practice that allows 1 segment of the market to use data **in any way** forbidden to another is a Trust Violation. It ensures a user's data is not private, and shifts power to specific companies that benefit from the privacy violation.

#### 2.1.3 Privacy Violation

If a Proposal allows any player to use, transfer, collect etc user data of a protected privacy class in a way forbidden by the class in the Proposal's Privay Definition, this is a Privacy Violation. 

A proposal in violation of its own privacy definition is a threat to user privacy and must be fixed. (See Fixing Violations)


### 2.2.0 Trust Statement

A proposal should also describe what it is trusting all players to do when relevant. The trust statement should cover all cases where a class of private data is possessed by players, and those players could choose to violate a user privacy as the Propoal defines. 

A. The statement should begin with: “No participant is more trustworthy than others.“ OR, clearly outline groups it claims are more trustworthy and why, though doing so will be flagged as a Trust Violation. It also should not use use-case, player or business specific language. 

B. For situations in which only one player is able to access the data, consider exposing the data to other players as well to avoid the Trust violation. If that is not an option, consider making it impossible, to the satisfaction of all other players, for the data to be misused. The other players should have a hand in this process to ensure fidelity (i.e. public audit).

bad example:
Our proposal gives SSPs everything about a user. They know everything. We trust them to not use it to make money, and we will not expose this dat to anyone else because well isnt making more people have the data a privacy risk? So yeah trust the ssps.

This is a clear Trust Violation. It gives the SSPs special access to data, whether they use it or not, that no one else has. It is clear this will lead to abuse in time and threatens a user's privacy. Users will actually be misled into thinking no one has their data potentially worsening the situation. 

Better example:
“No participant is more trustworthy than others. There is a case where the class of private data entitled User's Real Name may be possessed by any player. We trust the players not to Transfer this data off of the client in any way. Local Storage is fine. This trust is valid because this trust is enforced by Legal Agreement and Public Audits of All Data Sales by spec XXXX

No player has special treatment. No player is able to cheat on a user's privacy. Public methods exist to catch ad punish cheaters to encourage proper incentives.

#### 2.2.1 Trust Violation

If a Proposal gives unequal access to private classes of data by design, it is inherently a Trust Violation and must be fixed. Actual use is not required for this to be a violation; as long as a party can access a private class others cannot, this is assumed to be a violation. After all, to assume otherwise would require trust (hence the name).

### 3.0 Scope

The scope of the W3 WICG and other groups as defined in the charter is anything that can be implemented by a browser or other user agent. Kitten CLuster provides a forum to discuss issues that would be off topic on a particular proposal but relate to it, and are very much on topic for the propoal's introduction into a standard (or rejection).  Any argument that a violation is out of scope within kitten cluster is invalid if it can be fixed by or in the user agent, or if the user agent itself is the culprit. Such dismissive arguments should be seen as silencing behavior.

#### 3.1 Operating Systems and Scope

While Operating Systems and other programs that user agents run on are indeed out of scope, every proposal should agree that an OS is a player. The proposal should always forbid an OS from engaging in Privacy Cheating Behavior, and should never take steps to enable it. This is within a proposal's power.

A good way to do this without using player specific language is for a proposal to use the phrasing

"No player should deliberating pass information to or collaborate with forces higher on the stack of any given device in an attempt to circumvent privacy safeguards."

This includes the user agent of course. It is acceptable for that to be specified if unclear, as it applies to all players.

This wording is also general not to mention operating systems, as other extra-agent players could also potentially be culpable.

### 4.0 PrivacyDefinition.md

This file should begin with the version of Kitten Cluster it references. Currently there is only V1.

It should contain a Privacy Statement. A Trust Statement, and a statement on Operating System Scope as defined in 3.1  (when applicable) are recommended.  

### 5.0 What to do when you find a violation

#### 5.1 Report it on the Proposal

File a github issue on the Proposal. Clearly describe the specifics of the problem in the proposal, and why you believe it is a Violation. To help the proposer, reference specific sections of Kitten, including the subsection if applicable, and the type of violation.

Calm, reasonable discussion is best at this stage. Assume the proposer really does want to fix the issue. If they use deceptive methods to gaslight the poster or avoid disguessing the issue, then the poster will have the ability to act later. For now assume the best.

Also suggest to the proposer a good method of fixing the violation. Hopefully the proposer will then fix the violation, if it is still determined to exist.

#### 5.1 Report it here

If unsatisfied with the proposer's response, or if the proposers does not respond at all, file a ticket on this github. Include a link to the original issue.

Various community members can discuss the violation, and determine if it is serious enough to warrant tracking here.

#### 5.2 Add to PrivacyDefinition.mD

If 5.1 leads to the conclusion that the proposer is unable or unwilling to fix the violation, and if it is significant, a link to the kitten issue should be added to the bottom of this repo's PrivacyDefinition.md for that Proposal. If one does not exist it should be created. Anyone can make this pull request when they deem it necessary.

#### 5.3 Alternatives

Any alterntives after the issue is tracked here and added to the PrivacyDefinition.mD is tbd. If the W3 adopts this method it may become part of voting analysis. 



