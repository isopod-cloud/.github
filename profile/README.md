## Isopod
The network should not be a barrier to cloud adoption and expansion.

  ## Problem Overview
Isopod is an open source project tackling the challenge of cloud networking. It’s no secret that cloud computing is, or is becoming, a central part of everyone’s IT infrastructure. In some cases, they start with a single provider and single region, then evolve to multiple regions for availability, then evolve to multiple clouds to either use 3rd party services or various other reasons.

Networking in a single provider is hard enough, but across multiple providers is an even bigger challenge. There are several reasons for this.

-   There are many networking services and connectivity options in each cloud provider. These individually can have some complexity, but importantly, while each provider offers similar services, there are slight differences in capabilities and configuration between each that must be mastered.
    
-   Cloud pricing model and overall infrastructure is complex. - getting something to work is hard enough, getting something to work well (performance, reliability, cost) is even more difficult.
    
-   Expertise - Cloud networking is a cross between network expertise and cloud expertise. Some may fill these roles separately, some may have cloud generalists. Separate teams means higher impedance to development efforts, generalists means less depth in expertise across areas and clouds.

Looking for solutions, there were some commercially available ones that are really expensive and require you to provision a lot of extra cloud resources. In talking to many enterprises, there were some homegrown solutions to some of the problems, and in their own words, hacked together scripts to do one-off things. We have developed our own, and felt like it was important to start helping each other out and create an open source project and community.

## Project Overview

Isopod aims to provide tools to help automate cloud networking. We have identified, based on our own experiences, and in talking with many other companies, four areas to focus on and we have on our roadmap to bring an open source solution for.

-   Encrypted communication - When communicating between VPCs, particularly when they are in different cloud providers, we want traffic to be encrypted. Providers offer IPsec gateways under different names.
    
-   Optimized connectivity - cloud networks are complex enough that optimizing the connectivity, whether for cost, performance, or reliability, is in itself a challenge. We envision a tool, as a first step, that can monitor egress traffic between cloud providers, and then suggest ways to improve (e.g., cost improvements).
    
-   3rd party service private connectivity - the cloud encourages an ecosystem approach to software development, where 3rd party services are becoming more frequently used. The base way to access is via a public API, but private connectivity options are available (e.g., AWS Private Link). The nuances of this connectivity, such as it only supporting connections within the same region, presents complexity. We envision a tool to help automate the connection, including extending to other regions and providers (in combination with other tools, perhaps).
    
-   Authentication - Each provider, and each third party service has its own authentication. Managing keys and providing access controls to different people or services requires care. We envision a tool to help manage these keys and broker the various authentication methods.

The first tool being released is Chasm, which (i) can inspect each of the specified accounts and it will output a list of subnets it finds, and (ii) can create IPsec tunnels between selected VPCs. The analyze step is optional, but would output in a format that can be edited to then run through the deploy step.

## About Stateless and Why We’re Going Open Source

The company behind Isopod is Stateless. It was founded by two academics, Eric Keller and Murad Kaplan at the University of Colorado, Boulder with a goal to make networking simple. We saw the movement towards a hybrid-multi cloud infrastructure, but saw software being offered by the major vendors largely not changing - so, you’d have cloud infrastructure which is dynamic and scalable, but on-prem infrastructure which was still rigid. The telcos and co-location providers needed new solutions which matched the design of the clouds. Enter Stateless.

In this journey, we were able to make great use of open source software to build a complete solution. We contributed back to many projects, including identifying and fixing some really complex bugs. When we embarked on a new project to push deeper into the cloud to solve cloud networking challenges, we knew the individual tools that we’re building would help others. This would apply to both those that are cloud-only as well as those that have a hybrid infrastructure, and applies to both those using only a single cloud provider and those that have embraced multiple providers.

Over the past 15 years or so, the networking ecosystem has shifted from a closed ecosystem of vendors selling appliances, to an open ecosystem where communities are building software together. We were right there in the middle of that transformation, and in the field of cloud networking, filling an unmet need.

What we hope to get out of it:

-   Community feedback - what challenges are you facing that we, as a community, can help each other out.
    
-   Software Improvements - there are many experts out there that can provide more features and better solutions. And with more use, the software is more well tested and refined to better support its users.
    

-   Goodwill for Stateless - And just to get it in the open, ultimately, Stateless is a for-profit company. Perhaps one day, this will take a life of its own and a community will emerge around it. But, we’re starting with ourselves contributing and so we do hope that brings good will towards Stateless and those that find value in the open source tools we’re providing will consider Stateless for networking solutions.

We’re committed to developing in the open, creating a welcoming environment for feedback and contribution, and doing our best to respond to requests for improvements.
  
## The Name Isopod

For some reason, an Isopod has become the unofficial mascot of Stateless. When we had an office (we’re fully remote), we had a stuffed Isopod named Deborah, that we put to work in different departments - she seemed to settle in accounting.

But, Isopod also is a technical sounding name. Isolation is one of the core tenets of cloud computing, and pod is a collection of instances (used in a datacenter networking context to represent a cluster of servers, used in a kubernetes context to represent a grouping of containers). So, a networking project for interconnecting groupings of instances, an Isopod seemed fitting.
