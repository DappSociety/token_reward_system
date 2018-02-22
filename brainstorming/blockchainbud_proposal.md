# Token Reward System Proposal

* Author: @BlockcahinBud
* Version: 0.1
* Created: February 21, 2018
* Updated: February 22, 2018

This document serves as my draft proposal for a token reward system which incentivizes a group to collaborate on projects through task-based bounties.

## Preface
Some, but not all, of the functionality in this document has been written and tested in a (quick-and-dirty) proof-of-concept Solidity contract. There are still certain assumptions being made that have not been translated to code. Given the limitations of the blockchain's immutability, and transaction costs, alterations will, without a doubt, be made during development.

## Why: Purpose, Reason, Benefits
The main goal I would like to achieve with this system is the ability to bootstrap projects without any need to inject startup capital. I believe this is one of the "killer apps" for cryptocurrency and blockchain technology. The true potential for this could be staggering.

This bootstrapping is done by creating an entirely new currency (token) with no real-world value. However, by distributing the new tokens as rewards for work done on a project, they do represent actual value that was contributed. They enable us to capture value at a point in time, and then continually quantify that value indefinitely into the future. This is not unlike giving out shares in a startup, except in this model the opportunity to participate is permissionless.

When a project is brand new, unfinished, and with zero users, any value contributed to it is not actually providing real-world value. Therefore, captured value (tokens) should not have any real-world value. But as the project begins to provide real value to the world, it makes sense that the value captured in those early stages should be recalculated to its true worth. Tokens enable this recalculation to happen automatically through the free market (assuming liquidity develops).

Another purpose for this initiative is to enable more open source software to be developed and shared with society. To find a new way for making open source careers sustainable.

>Open source is treated as the 'non-profit' alternative of the technology world, but the reality isn't that simple. The philosophy that software should be free does not mean that we shouldn't be able to sustain open source careers. The misaligned incentives leaves large value on the table, year over year.
>
>Right now, developers are creating for open-source even when it's against their incentives. Imagine what would happen if we could find (a combination of) better ways.
>
> [Vivek Singh via Medium](https://medium.com/gitcoin/oss-today-some-wins-some-losses-89d1ab46ceb6)

It's common for people to lose interest in maintaining their open source projects. Sure, they can be continued on through forks, but many go abandoned. A large amount of open source projects that push forward are funded by corporations.

I believe open source contributors should get something in return. Even if that something is just score keeping, recognition, and voting power within the project's micro-economy. Gamers spend countless hours earning in-game achievements with no expectation they can ever sell those for money. But this is not surprising since achievement and respect are some of our highest needs according to [Maslow's Hierarchy](https://en.wikipedia.org/wiki/Maslow%27s_hierarchy_of_needs).

In my opinion, having such a mechanism in place decreases the chances of in-fighting or the team/project dying out. Because there are objective factors at play, and each valuable task is rewarded, a decentralized team can move the project forward without relying on any one person.

We don't need to convince everyone to work for "worthless" tokens. For each project, you only need to convince a small core team to believe in the concept and get the ball rolling. When others see value being created, that ball has the potential to build a lot of momentum, and the core team will be rewarded most for their foresight.

## Are We Reinventing the Wheel?
My eyes were first opened to these possibilities upon stumbling across [GitCoin](https://gitcoin.co/). Additionally, there are many other articles, papers, and projects that have heavily influenced my thinking on this, which is being maintained in [this resources document](https://github.com/DappSociety/token_reward_system/blob/wip/master/brainstorming/resources.md).

It is true that we could simply create a new ERC-20 token and use the bounty systems already in place. However, that would severely limit the amount of creativity we can apply in developing new models.

My hope is that by taking lessons from existing projects, but also exploring new territories on our own, we can validate some novel uses cases which can then be incorporated as custom options into an eventual set of standards.

This space is too new to simply take any current standards at face value. We must challenge assumptions and push boundaries to find out what really works.

I see this token reward system as a great opportunity to build something of value and contribute to blockchain history alongside other great projects like ConsenSys, Colony, GitCoins, Status, Aragon, and more.

We are essentially creating a [curation market](https://medium.com/@simondlr/introducing-curation-markets-trade-popularity-of-memes-information-with-code-70bf6fed9881) in which the decentralized curation of valuable tasks results in the completion of a valuable project.

>Curation Markets is a model that allows groups to more effectively coordinate & earn from value they co-create around shared goals.
>
>[Simon de la Rouviere via Medium](https://medium.com/@simondlr/introducing-curation-markets-trade-popularity-of-memes-information-with-code-70bf6fed9881)

The key differentiators of this system include:

* Delegating tokens from a shared pool
* Post-funding a bounty (not simply tipping a *person*)
* Continuous funding of a bounty for real-time valuation
* Multiple payees on a bounty
* Group consensus on task completion (not up to bounty creator)
* Self-contained ecosystem within the scope of a project

## Timeline Expectations
Many projects within the blockchain ecosystem are running on private chains and/or test nets, and ours will be no different at the start. We will need to go through much trial and error, testing out multiple integrations and economic models until we find a system that fits.

This means value will not actually be rewarded in real tokens until this is all sorted out.

When we do eventually roll out to the main net, we should begin with support for parameter tweaking and upgradeability though a contract owner (likely a multisig setup). Over time, once the system/economy is deemed stable, the contract can be made permanent by removing the owner. This achieves the true promise of smart contracts in that everyone can verify the rules and no one can change them.

## Project Requirements
This section serves as a rough outline of some required attributes for the project.

* Tokens are not pre-mined; total supply starts at zero
* Tokens can only enter circulation through completed bounties
* Unused, uncirculated tokens are recycled back into the bounty pool
* Bounties can be attached to any task, not just Git actions (tool-agnostic)
* Reputation system for whitelisting addresses to prevent fraud
* Reputation system for punishments against attackers and cheaters
* Standardized enough so any project can use their own instance
* Attempt to be compatible with StandardBounties (collaborate, don't compete)
* Value of a task is calculated by the "wisdom of the crowd"
* Allow for funding bounties after completed (tipping)
* Allow for multiple people to fund a bounty
* Allow for multiple people to collaborate on claiming a bounty (they must decide payout share)
* A positive UX front-end for viewing, funding, claiming, and managing bounties
* Allow for batch claiming bounties to save on transaction fees
* Mechanism for last-resort contract upgrade and 1:1 value transfer (critical bugs)
* Library based and modular rather than one huge contract

## Monetary Policy
My education in economics consists simply of reading a few books on the subject, studying investing/asset management, a career in advertising psychology, analyzing and thinking about in-game incentive models, intuitively making inferences from existing cryptoeconomic models, and reading articles while designing this particular system.

Clearly nothing formal, so anyone with more experience, please poke holes in my theories, assumptions, and reasoning.

Reading more books on economics, game theory, and mechanism design is on my todo list and will hopefully improve this model further.

### Starting Supply of Zero
As a best practice, the total token supply starts at zero, with none being pre-mined.

The purpose of this is so that no core founders of the new currency have any arbitrary control over millions, even billions, of tokens. All influence within the project is earned. This increases trust in the system. Credit is given where credit is due.

The downside of this is that you cannot pre-sell tokens to raise capital and you cannot reserve tokens for future initiatives. For some projects, a pre-mine could make sense, but that comes with a tradeoff in overall trust.

However, future initiatives (e.g. a project foundation) could be set up as bounties, with all current participants deciding how many tokens to allocate to each. This eliminates the need for a questionable pre-mine while still achieving the same result over time.

### How Tokens are Minted
Tokens are minted at a fixed rate per unit of time to the contract address. This means no one actually owns them and they are not in circulation. Transferring them directly from this address to another address is not allowed by the code.

These tokens can be thought of as a shared pool in which each participant has the power to delegate a proportional share towards bounties of their choosing. We will come back to this topic of delegation shortly, but first, let's address inflation.

### Inflation
We must be careful of the supply schedule we put into place so that a project's tokens remain relevant within the project over time. It is my belief that the inflation rate should start out very high, and then adjust down over time. Similar to Bitcoin's supply schedule.

The rationale for this is to incentivize and properly reward early contributors to a project, while also protecting their value from being diluted too much over time. Tokens should be easier to earn when a project is new and they have no value. But as a project gains momentum, and the tokens potentially gain value, they should not be as easy to earn.

There are many different formulas we could come up with for defining the supply schedule. A few quick examples could be:

* __Simplistic:__ Target 1,000,000 tokens the first year, 50% inflation rate the second year, then halving every year after that until a minimum rate of 2% of total supply is reached.

* __Continuous:__ Target 1,000,000 tokens the first year with a starting inflation rate of 100%, adjusted down on a continual (by the second) basis to a target of halving every 365 days until a minimum inflation rate of 2% of total supply is reached.

* __Oracle:__ Issue $50,000 USD equivalent per year, with a max issuance of 1,000,000 per year (issuance doesn't decrease until token is worth more than $0.05).

Additionally, although the premise is based on tokens being minted when purchased (providing instant liquidity), this article on [Bonding Curves for Continuous Token Models](https://hackernoon.com/how-to-make-bonding-curves-for-continuous-token-models-3784653f8b17) could also be used as a source for ideas on supply formulas.

Another consideration regarding inflation is the case in which a project becomes inactive, with no bounties being created, and no tokens entering circulation. In this case, I believe inflation should be paused. This can be done by setting a max balance for the shared pool. I cannot see any benefit in letting the shared pool of an inactive project grow indefinitely.

As you can see, there are an infinite number of possibilities here. Deciding on which to use is an important decision, but we could implement a way to modify the parameters until the system is deemed mature and the contract is made permanent through removal of its owner.

In any case, this is something that will require a lot of research and careful thought by the group. As a framework to other projects who might use this system, we should provide premade supply formulas and best practices.

## Delegating Shared Tokens to Bounties
The way in which shared tokens are entered into circulation is through bounties (i.e. tasks). Members delegate their portion of shared tokens towards bounties they deem important. When a bounty is marked as successfully complete, the person(s) who did the work is able to claim those tokens to their own address.

Members can delegate tokens based on how much of the pool they have claim to. The formula for calculating a member's claim is:

`(total tokens in pool / total active verified users) - tokens they have currently staked in active bounties`

If more members are added to the list of verified addresses, the total share of the current supply goes down. When this happens, existing member did not "lose" any tokens, they simply have less weight to vote on bounties. You can maximize your weight by delegating your tokens before new members are added (avoiding any dilution).

In order for this system to work, we need to use identity verification, e.g. linking addresses to usernames, to prevent anyone from creating multiple addresses and claiming an unfair share of the pool.

## Reputation System
A reputation system is required to determine who can participate in delegating tokens from the shared pool.

Without a reputation system for whitelisting addresses, anyone could create tens or hundreds of addresses to control a disproportionate amount of the shared tokens. The reputation system needs to link 1 address to 1 verified group member.

### Verifying Members
One solution may be to use an existing blockchain identity platform like uPort to create verified identities. Hopefully we can integrate custom reputation metrics into their system.

If not, we could create our own system based on reputation within the group. A user is only eligible to have their address whitelisted within the contract after accumulating a certain reputation score.

We still need to discuss which metrics are factored into our reputation score (in collaboration with our Governance Model Research Group), but the system must allow for new users to bootstrap reputation from zero while still making it unrewarding for attackers to create multiple identities.

### Inactive members
If members go inactive, but still have claim to a portion of the shared pool, their share is effectively locked and unable to ever enter circulation.

To prevent this, we can periodically mark addresses as inactive so they are not locking up a portion of the pool. Once a member is marked inactive, the proportion available to other members is automatically adjusted by the formula given in the previous section on Delegating Tokens.

The effect of this is that unused bounty tokens are automatically recycled into the pool. They were never "owned" to begin with, so no one is actually losing anything here. This incentivizes everyone to make their best judgement on what bounties to fund in a timely manner rather than to procrastinate.

If an inactive member wants to become active again, all it takes is a blockchain transaction to do so. To prevent intentional locking of funds (continually reactivating without any intention of participating), we could implement a strike against their reputation. If reputation drops too low, the address is removed from the whitelist.

## Creating New Bounties (Tasks)
Creating a new bounty will be as simple as using a web interface to interact with the contract. Any whitelisted member can create a bounty for any task or any proposal.

The bounty will then show up in the web interface and can be linked to from anywhere. In the future, if we implement the StandardBounties contract interface, our bounties could even be listed in other marketplaces and be compatible with standard tools like the [GitCoin Chrome extension](https://chrome.google.com/webstore/detail/gitcoin/gdocmelgnjeejhlphdnoocikeafdpaep?hl=en).

### Smaller Tasks Are Better
Ideally, bounties should be a single-person task. This provides the least chance of conflict and scope creep. Breaking a project up into smaller tasks would also end up valuing each task, and therefore the work distribution in the project as a whole, more fairly.

A bounty should never be a large project. Large projects should be broken down into tasks. Those resulting tasks are good candidates for bounties.

The exception to this would be in the case of a fund raising bounty. For example, to raise tokens to be reserved for a marketing initiative once liquidity is achieved. This would be okay because the "worker" that the funds are paid out to would be another contract (a single entity) who's purpose is to hold them.

## How Tasks Are Valued
Just as we will have a web interface for creating bounties, we will also have a web interface for viewing all bounties and individual bounties. Group members can view all bounties and choose which to allocate their shared tokens to, or they may be directed, via links, to an individual bounty for allocating tokens to it.

Since bounties must be funded, their value is decided by group consensus, decreasing the potential for manipulation.

This should give us a good approximation of the value of a task. The more people who think it is important, the more will contribute. If a task already has a lot of contributions, more than what is deemed fair value, then any member can decide more are not needed and choose to allocate their tokens elsewhere.

If a task gets enough funding it should be deemed important. If not, someone can still choose to work on it and hope to collect post-funding (tips) after. Post-funding is discussed later in its own section.

### Additional Funding
In the previous section we were referring to allocating tokens from the shared pool. However, if a user feels strongly about a particular bounty, they can also contribute more funds from their wallet.

These funds could be more of the project's native tokens, or for a larger incentive boost, could even be ETH. (It is possible we could include support for other ERC-20 tokens as well, but sticking to native tokens and ETH is probably a good design decision).

### Re-Allocating Funds
What if you allocated tokens to a certain task, but then a new one comes along that you think is a better candidate? Or what if you allocated tokens to a task and later you find it is receiving more support than necessary?

As long as the task has not been completed, you can choose to withdraw your tokens from the bounty. Even if people have already started working on it.

The rationale is that if a certain task is taking too long, or suddenly becomes unimportant, funds should be able to be withdrawn and re-allocated.

Allowing this has a few additional benefits:

* Prevents anyone from marking a bounty as "started" but not actually making progress. There is an incentive to complete the task or risk getting de-funded.
* Allows for more funds to come into a bounty as progress is shown or if it becomes more important.
* Incentivizes users to break larger tasks down into smaller tasks, which as was mentioned, are more easily valued and have less risk of conflict.

## Working on Bounties
In order to prevent an attack where a user creates a bounty, funds it, and then marks it complete, anyone electing to work on a bounty must first submit a "bid." This is not a bid in the traditional sense where it includes a price. It is simply announcing to be a worker on the task.

In order to bid for work on a bounty, a user must stake tokens. However, none of these tokens are at risk. Once the bounty is marked complete, all staked tokens are returned. Even to bidders who were not the ones to complete the task.

However, staked tokens could be taken away as punishment for bad behavior. If foul play is suspected, a member of the group can challenge the bid. If the bid is found to be in violation of rules, then that party's staked tokens are rewarded to the challenger.

**Note:** There is an obvious issue here in that any new users (which includes everyone at the start) do not personally have tokens available to stake as good-faith for working on a bounty. One possible way to address this issue would be to also consider a small amount of ETH to be a valid staking token.  

### Multiple Parties Working Separately
The first bid to complete the bounty (verified by group consensus) is awarded the full bounty.

However, each party working on a bounty will have submitted a bid, so everyone working on a task can see who else is working on it. Any party can, at any time, drop out and reclaim their staked tokens.

Additionally, because we will support multiple payees, bidders can decide to team up by merging their bids into one and defining a ratio at which they will share the reward. This issue of multiple payees sharing the bounty is discussed below in "Multiple Bounty Winners."

## Completing Bounties
Bounty tasks are marked as sufficiently complete based on consensus vote by all verified project members. When a bidder believes a bounty is complete, they must submit their work for voting.

To promote prudence and prevent wasting community time on premature submissions, if any entry is determined to be incomplete, a portion of their staked tokens (tokens they owned) will be sent to the shared pool. In the case where ETH was staked, we could send this to the contract and use it to subsidize transaction fees.

### Who Can Vote?
All verified members (excluding those who have bid on the bounty) can vote on whether or not a submission satisfies the task. However, those who have funded the bounty are given slightly higher weight with the rationale that they have more interest in the work being completed and are therefore better judges.

When work is submitted, all bounty funders are notified to vote and/or leave comments, and are required to do so. If a member funds a bounty, but then doesn't vote on it, they get a reputation strike. Too many and they receive a temporary suspension from access to the shared pool.

All competing bidders on that bounty also get a chance to challenge by submitting their work to the vote and/or leaving comments. Due to conflict of interest, bidders on a bounty are not allowed to vote on it.

### How Does Voting End?
To prevent locked votes, we stop the vote after a set number of days or as soon as statistical significance is reached (any more votes won't change the outcome).

Once a task is deemed complete, funds are locked in the bounty. No one other than the payees can take funds out, but anyone can still put more funds in. This post-funding is discussed in more detail later.

## Killing Bounties
Not every bounty that is proposed, funded, or even worked on will end up being completed. Therefore, we must have a way in which bounties are killed.

Users can effectively vote to kill a bounty by removing funds from it. If funds are removed, the incentive to complete it decreases. But that alone isn't enough because such a bounty is still active, polluting a project's task list.

We would need to set an expiration date on bounties such that if no activity has taken place for a certain amount of time, the bounty is marked dead. Life-extending activity could be defined as any transaction taking place on the bounty. We could even have a button labeled `Extend Bounty Expiration Date`. This would ensure that only bounties which were truly abandoned end up being killed.

Once a bounty is marked as dead, any shared funds are recycled back into the pool. For additional, non-pool contributions, contributors would be required to claim their funds from the dead bounty. We could notify them of this using events.

## Claiming Bounties
Bounty winners can easily claim their tokens uses the web interface. They simply select the bounties they want to claim from. If their (MetaMask) address is listed as a payee, the transaction will be approved, and the contract will transfer the tokens to their address.

To save on transaction fees, users should be able to claim bounties in batches. The contract function signature would be along the lines of: `claimBounties(uint[] bountyIds)`

### Multiple Bounty Winners
In the case where there are multiple winners on a bounty, each of them can claim their share that is proportional to the ratio set by them in the contract.

This share percentage can be set and changed at any time if all parties are in agreement, using a multisig mechanism. This ratio will be stored within the contract, viewable on the bounty, and strictly enforced by code. Disputes may arise, but they would be minor since tasks should aim to be as small as reasonably possible.

To give an example, if after a two-person bounty is completed and funds are claimed at a current rate of 60/40, they could then agree that any additional funding should be claimed at a rate of 90/10. I'm not speculating on why such an agreement would take place, just that the option for doing so should be available.

The total amount contributed to the bounty and total amount withdrawn by each participant would be kept on record within the contract so claim to any new funds can always be accurately calculated based on the current ratio.

## Post Funding
Pre-funding bounties is obviously necessary to incentivize members to work on them, but I also believe post-funding bounties can go a long way to further align incentives.

Members should be able to take initiative before something gains traction, and then get rewarded after completion if other members believe it was more valuable than initially perceived.

For some tasks, the usefulness might not be immediately apparent. This could be the case for creative work where the end results are subjective or for outreach work where the ultimate impact of the task is unknown. Even objective, feature-based tasks could benefit from this.

Bounties should not require marketing as if they are sales pitches. It's easier for people to see the value when something is completed than when it is simply being proposed. Reddit and SteemIt are good analogies to use here. As something gets more popular (has more perceived value) it captures more value.

This should also increase the rate of progress, reducing instances where someone creates a task but doesn't actually work on it because it didn't get funded, or postpones getting started because they believe it could end up getting more funding over time.

### Time Limits for Post-Funding
It is probably a good idea to set a time limit on post-funding. After that time limit has passed, no more contributions are allowed on that bounty. The expiration time could be an arbitrary amount after the task has been completed, or it could be one that gets extended after each addition.

Without any time limit in place, we could end up with old, popular tasks receiving too much of the new token supply, and in turn, less funds being allocated to new and important issues. No time limit also increases the risk of funds being allocated to old addresses where the owner no longer has the key to claim them.

## Possible Attacks
In order for a decentralized system to survive, it must assume it will be attacked, and have pre-planned mechanisms in place for deterring the attacks. A few attacks were mentioned within the narrative of the previous sections, but this section can serve as a dedicated place to collect additional attacks.

We will need to come together as a group, looking at this from all angles, to sufficiently prepare for all attacks. Even with our best efforts, once real value is at stake, a vulnerability will likely be exposed. We will have to be prepared for that by initially providing for upgradeability in our contracts.

Please help out by suggesting any possible attacks and solutions. The more we anticipate, the more robust our system will be. You may submit them as GitHub Issues on this repo.

#### 1: Post and fund a bounty that is intended to do damage to a project
* __Example:__ Bounty to remove all members' access to social media accounts
* __Example:__ Bounty to add inaccurate or harmful code/content to the project
* __Solution:__ Incentivize other project members to be on the lookout for malicious bounties. If caught and proven through fair arbitration, offending parties are stripped of reputation, lose any staked tokens, and are blacklisted from the project.

#### 2: Post a fake bounty in order to extract funds from the shared pool
* __Example:__ Member posts very easy bounty and self-funds with tokens from the shared pool
* __Solution:__ Incentivize other members to be on the lookout for cheaters. If caught and proven through fair arbitration, offending member loses staked tokens and receives a permanent flag on reputation.
* __Solution:__ Any funds contributed to any bounty by the winner are returned to the shared pool (e.g. members cannot send shared tokens to themselves).

## Uses for Project Tokens
The tokens collected from bounties belong to the holder just like any other ERC-20 token. Although they could be worth something one day, we shouldn't expect them to be.

Even if they have $0 real-world value, there are still other options for them to provide utility, such as:

* Fund bounties beyond individual shares of the bounty pool
* Require users to stake a bond in order to be eligible to work on a task
* Use tokens as weight for various functions within a governance model
* Pay dividends to holders (in new tokens and/or ETH if generating a profit)

All projects should include some sort of utility for their tokens so users can get value out of them even if they can't sell them for another form of currency.

### Path to Liquidity
Early believers in a project should rightfully assume that one day the project might be worth something, and in turn, its tokens worth something. In order for this to happen, liquidity needs to develop. It could develop within the project's micro-economy or it could develop in secondary markets.

With the existence of decentralized exchanges, it is very possible that project bounties would emerge for growing token awareness. From this awareness, a secondary market, and in turn liquidity, could be created. Without one person governing, there is no one to stop that from happening.

If any project does actually provide real value to the world, it wouldn't be so crazy for its tokens to also have real value.

### Preserving Token Value by Decreasing Velocity
This is something I was made aware of recently by a few of the articles in [the resources document](https://github.com/DappSociety/token_reward_system/blob/wip/master/brainstorming/resources.md), and something that should be considered before finalizing the system. The premise is that there should be a reason to hold tokens rather than to simply sell them immediately.

>Velocity is one of the key levers that will influence long-term, non-speculative value.
>
>Most utility tokens don't provide a compelling reason for token holders to hold the token for more than a few seconds. Absent speculation, assets with high velocity will struggle to maintain long-term price appreciation.
>
>Hence, protocol designers will be well served to incorporate mechanisms into their protocols that encourage holding, not just usage.
>
>[Kyle Samani via CoinDesk](https://www.coindesk.com/blockchain-token-velocity-problem/)

Refer to the _'Uses for Project Tokens'_ section for some honest ways in which velocity could be decreased.

## Front End
This section is very minimal because the back-end concepts are still being fleshed out. Front-end elements have been partially discussed in other sections, but for the most part, we will trust the guidance of experienced UX designers in our community to develop this portion.

In its most basic form, the front-end will need to:

* Create and managing bounties
* Display all bounties and individual bounties
* Allow users to add and remove their tokens on bounties
* Submit bids to work on bounties
* Submit completed work for voting
* Provide an interface for the voting process
* Allow winners to claim funds from bounties

## FAQ
Please submit your questions within the [DappSociety Slack](https://dappsociety.slack.com/). Common questions will be added here.

#### Why would anyone pay transaction fees to earn with worthless tokens?

That will be a personal choice and will be based on how much the individual believes in the project. We should look to the future for a scaling solution where transaction fees are near zero. Or we could do similar to [Lunyr and refund transaction fees](https://medium.com/lunyr/gas-payment-will-be-free-in-the-lunyr-open-beta-8b1c77276e0b) (via an ETH donation pool from members).

## To Do
* Study more on mechanism design and game theory
* Evaluate how we can utilize [OpenZeppelin](https://openzeppelin.org/) and other libraries
* Research if/how [Aragon](https://aragon.one/) complements bounties

## Credits / Resources
* A list of all resources used in this project is being maintained [here](https://github.com/DappSociety/token_reward_system/blob/wip/master/brainstorming/resources.md).
* ... if you contribute, add yourself here

## License
```
Copyright (C) 2018 DappSociety

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
```
