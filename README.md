# greyhound

A Chrome/Firefox/Safari browser extension for [Domain](https://www.domain.com.au) and [Realestate](https://www.realestate.com.au) that auto-magically checks the [Statutory Infrastructure Provider](https://www.acma.gov.au/statutory-infrastructure-provider-sip-register) (SIP) for listing addresses displayed using data from [data.gov.au](https://data.gov.au). Some addresses do not have a SIP assigned currently, and further data sets are used to fill in the gaps. Oh, and it also reports what technology type is available.

## Contents
- [Background](#background)
- [Usage](#usage)
- [Contributing](#contributing)
- [Why internet "down under" sucks](#why-internet-down-under-sucks)
  - [Introduction](#introduction)
  - [What different options are there?](#what-different-options-are-there)
  - [Why does it matter how I connect?](#why-does-it-matter-how-i-connnect)
  - [So why don't we have fibre everywhere?](#so-why-dont-we-have-fibre-everywhere)
  - [Why don't carriers build over each other then?](#why-dont-carriers-build-over-each-other-then)
  - [Conclusion](#conclusion)
- [References](#references)

## Background

Looking for a new place is never simple. You make a list of scaling priorities to ensure that you are getting exactly what you need. The more stakeholders, the bigger the list can grow. As a Gen Z, I see internet connectivity as a basic need and a stable, fast connection saves me time and stress. Having Gen Z roommates that feel the same way just adds to this.

> Are we going fast? Can anyone tell if we're going fast? - Jake Peralta

![Yep. Yep. Yep. Yep. Yep.](https://media.giphy.com/media/FZhZ878xC8iQzkxd4J/source.gif)

NBN Co's website can be finicky, and most other carriers don't give consumers an easy way to view their data. So this project is the result of getting sick of constantly referencing SIP data, as well as [Aussie Broadband](https://www.aussiebroadband.com.au/)'s [PoI checker](https://www.aussiebroadband.com.au/nbn-poi/) whilst looking at listings.

As for the name 'greyhound', dogs are "man's best friend". Internet should be fast, and the greyhound is the fastest dog. [Monty Python's deductive reasoning](https://www.youtube.com/watch?v=X2xlQaimsGg) strikes again.

## Usage

WIP.

## Contributing

Yes. WIP.

## Why internet "down under" sucks

### Introduction

Is this specifically relevant to the extension? No. However, if connectivity in Australia was simple, reliable and fast in more places then I would never have built this extension.

Sadly, internet here can be abysmal. As a nation, we rank 60th globally for fixed broadband download speeds at 60.54Mbps, which is heavily lacking behind the average of 91.96Mbps¹.

Every country has their own set of local "buzz words". Ours include 'national', 'government' and 'infrastructure'. Combine the three, add a sprinkle of the [Telecommunications Act 1997](https://www.legislation.gov.au/Series/C2004A05145) Parts 7 and 8, and out comes this mess.

In summary, any fixed-line network built or modified after 1st January 2011 that serves residential/small business customers must be sold as a wholesale Layer 2 bitstream product. A local bitstream access service (LBAS) cannot be sold directly to consumers, instead a retail service provider (RSP) needs to purchase the product from the carrier and connect the customer to the greater internet. There is a small set of exemptions for smaller networks that were established before the first day of 2011, and these networks can be sold directly to customers.

Further information on the Telecommunications Act 1997 Parts 7 and 8 is available [here](https://www.communications.gov.au/policy/policy-listing/telecommunications-act-parts-7-and-8-requirements-and-exemptions).

### What different options are there?

The most important factor for a reliable and fast connection is always the "last mile" connection. This describes what technology is used to connect a premises to a network, with many different options that are available for use.

Name | Abbreviation | Technology | Speed | Reliability | Overall Rating |
---- | ------------ | ---------- | ----- | ----------- | -------------- |
Fibre to the Premises | FTTP | Fibre optic | ★★★★★ | ★★★★★ | 1 |
Hybrid Fibre Coaxial | HFC | Pay TV coaxial | ★★★★ | ★★★★ | 2 |
Fibre to the Curb | FTTC | Copper line | ★★★ | ★★★ | 3 |
Fibre to the Basement | FTTB | Copper line | ★★ | ★★★ | 4 |
Fibre to the Node | FTTN | Copper line | ★★ | ★★ | 5 |
nbn™ Fixed Wireless | FW | 4G cell service | ★★ | ★★ | 6 |
Sky Muster™ | - | Satellite | ★ | ★ | 7 |

For more information on what each technology type involves, [this Ausdroid article](https://ausdroid.net/2019/05/16/get-to-know-the-nbn-different-connection-types-and-what-they-mean/) gives a lot more detail.

### Why does it matter how I connect?

Put simply, the closer that you can get to a fibre cable, the faster and more relaible your connection _generally_ is. Not every carriers' network is built the same, so having Fibre to the Premises doesn't guarantee that your experience will be magical, however it is definitely a step in the right direction.

Copper telephone lines heavily influence how fast your internet can operate, as well as _generally_ being less reliable. A poor copper line that becomes exposed to the elements can cause your modem to "drop out" due to interference, and this isn't uncommon.

Coaxial networks have their own set of issues too, being that it is a shared medium. You, your neighbour, and even your neighbours' neighbour on a HFC network will all share physical connectivity back to the node. This just adds another place where things can slow down and cause issues.

### So why don't we have fibre everywhere?

Well, that was almost the original plan. Roll fibre to 93% of Australia's population, with the final 7% being served by satellite or fixed wireless as these premises were rural and extremely expensive to deploy fibre to. However, a change of Federal Government in 2013 resulted in the move to a Multi Technology Mix (MTM) model for the fixed line component, and we are now left with "Telstra’s dilapidated twisted pair and HFC access networks under new management"².

![Don't blame me, I voted for Kodos](https://media.giphy.com/media/3o6MbpHSxVAPUQQNws/source.gif)

### Why don't carriers build over each other then?

They do, just not in _residential_ areas. Parts 7 and 8 of the Telecommunications Act 1997 mean that they would have to wholesale that network out, which makes the investment much less appealing. Some carriers use wireless technologies to connect a complex to their network, which isn't covered under the legislation and allows them to sell directly to customers, however wireless can have many drawbacks including interference and slower link speeds.

### Conclusion

Despite former NBN Co CEO Bill Morrow stating that "Even if we offered it for free, we see the evidence around the world that they wouldn't use it anyway" when referencing Gigabit speeds, offering high speeds at affordable prices drives innovation and creates a better experience for consumers. It's not like [Deloitte was commissioned by the Australian Government](https://www2.deloitte.com/content/dam/Deloitte/au/Documents/finance/deloitte-au-fas-benefits-highspeed-broadband-v2-240914.pdf) to show these benefits.

More fibre is good, and trying to get it all the way into your premises is always a good idea for speed and reliability.

## References

¹ Speedtest® Global Index November 2020. Retrieved 2021-01-02 AEST. Archived copy available at https://web.archive.org/web/20201231063310/https://www.speedtest.net/global-index

² How to fix the NBN. https://theqlder.com/2020/03/06/how-to-fix-the-nbn/
