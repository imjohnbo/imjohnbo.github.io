---
layout: post
title: "Partner Engineering: The Missing Manual"
author: john
categories: [ Technology ]
tags: [ Work, Partner Engineering ]
comments: false
image: assets/images/2021-12-27-partner-engineer.jpg
---

# Partner Engineering: The Missing Manual

Over the last decade, a new developer discipline has emerged called Partner Engineering, found at companies large and small, including GitHub, Algolia, Meta, and Google. **Partner Engineering is a unique combination of software development, program management, community building, and communication, used to build rich ecosystems around a company’s products**. Whether you’re considering a new role, already work as a Partner Engineer, or are building out an integration ecosystem at your company, I hope my experience may be helpful to you.

In this article, I’ll tease apart the role and its responsibilities, contrast it with other roles, and discuss common practices and strategies. This article is based on *my own observations as a Partner Engineer* at GitHub and conversations with others – it does not necessarily reflect the views or opinions of my employer.

## Meet the Partner Engineers

**Partner Engineers are software developers who are experts at building from the outside in**. To meet the demands of today’s connected world, companies offer *developer platforms* with SDKs, APIs, and extensions, which other companies can *integrate* their services into for the benefit of mutual customers. Most developer platforms are open to the public and include comprehensive documentation and examples. A few are invitation-only and serve niche needs. You might have already used one of the public “developer dot” platforms ([`developer.twitter.com`](https://developer.twitter.com), [`developers.facebook.com`](https://developers.facebook.com), etc.) for fun or at work. Maybe you’ve met with a Partner Engineering team while building out an official integration.

As stewards of the integration ecosystem, Partner Engineers carry three main responsibilities:
1. **🔦 Enablement**: paving the path. Depending on the category of integration (see below), this can mean *de-risking* technical architecture, *specing out* specific integrations or generalized reference implementations, and *consulting* on the nuance inherent in the platform.
2. **🎓 Education**: connecting the dots. You’ll find Partner Engineers giving talks either *for* integrators or *with* integrators for mutual customers. Why integrate and how? What self-serve resources are available? And for customers – what is the use of the integration? 
3. **📣 Advocacy**: giving a voice to the integrator community. Partner Engineers should be *good listeners and communicators*. As they engage with a variety of integrators, they distill their feedback into an actionable form for the product teams. Does the platform need better docs? A well-defined roadmap? Are customers having a good experience? Are there successes to celebrate publicly?

Let’s make it concrete with some (semi-contrived) examples. A Partner Engineering team would take on initiatives like:
- Onboarding a set of ID providers (integrators) to a digital wallet (developer platform) in preparation for a launch announcement
- Providing reference implementations in three common programming languages so merchants (integrators) can connect to a ride sharing service (developer platform)
- Managing several collaboration SaaS products (integrators) migrating from one integration mechanism to another in a chat workspace product (developer platform)

In many cases, Partner Engineers are specialists embedded on the product teams that need integrations to succeed (see “complementary integrations” below). Between product release cycles, Partner Engineers contribute top features and fixes to the platform, prepare reference implementations and documentation for the next release, or support another product release. At other companies, Partner Engineers are platform generalists who sit outside of the product teams, which provides them more agility for supporting multiple supplementary integrations across verticals.

Partner Engineers enable, educate, and advocate for partner integrators – but *who is the integrator*? Who writes and maintains the integration?

## Working with integrators

All else equal, **the company that has more to gain acts as integrator** and will resource a team to develop and maintain the integration. Some companies maintain lots of external integrations, others few or none. Some companies dedicate a software engineering or developer relations team to integrations, others let it happen ad hoc. Many companies integrate with and buy from each other, so the integrator and customer roles can be fluid. **I find Partner Engineering interesting because of these changing roles, working with a variety of technologies, and tackling high impact projects with companies around the world**.

Partner Engineers work with other internal teams to ensure the success of the integrator, especially:
- **Product**: fit integrations with current and future product strategy
- **Engineering**: make the developer platform that integrators need
- **Business Development** **/ Strategic Alliances**: prioritize and initiate new areas of partnership
- **Sales**: plan co-sales activity, if applicable
- **Marketing**: plan co-marketing activity, if applicable
- **Support**: address inbound technical support questions around integrations

Companies with public developer platforms have a mix of inbound, reactive integration needs and outbound, proactive requests. Technical Support generally is responsible for inbound requests and Partner Engineering for outbound, along with one or more of the teams above. Partner Engineering depends on B2B partnership programs and other long term engagements to arrange initial contact with an integrator but is then responsible for their journey through launch.

All this talk about integrations – come to think of it, *what is an integration*?

## Understanding integrations
 
**An integration connects a host product to a target product via the target developer platform**. The integration can sit inside the host product, or outside, calling both the host and target platform.

In general, integrations fall into two main categories and in both cases serve to improve the product:
1. **🧩 Complementary**, where a product *requires* or is *made complete* by external integrations. Smart TVs need partnerships with streaming providers, app stores need apps, etc.
2. **💅 Supplementary**, where a product is *reinforced* or *enhanced* by external integrations. Video calling software might be better with external apps but works just fine without it.

Of course, what counts as “required” vs “optional” is subjective and is defined by the business. **Partner Engineering** **focuses on complementary integrations**, ensuring a product has launch partners or ongoing gap-filling integrations, but can also be found fostering communities of supplementary integrators. Working with complementary integrations – usually a 1:1 ratio for a period of time – means providing early access to features, presenting to technical audiences, writing reference implementations and documentation, capturing feedback, and supporting the feature launch or long-term integrator pipeline around the feature. Supplementary integrations – a 1:many ratio – augment a “power of the platform” message and need less individual attention but can still be critical to ecosystem vitality. Partner Engineers might arrange Platform Days or office hours for these integrators, or help cohorts with cross-cutting concerns, e.g migrate their integrations to newer authentication models.

**If your revenue model includes extensibility, you’ll want to define a specialized Partner Engineering function**. As a developer platform grows in breadth and complexity, this unique type of engineer will help the ecosystem thrive and allow product teams to focus on what they do best. From a business standpoint, not all integrations are alike – not even all complementary integrations. Start with impact and work backwards: where should this engineering team spend its time? The answer is: on partnerships with high-impact, strategic integrators, while simultaneously ensuring all integrators have a good experience on “developer dot” through scalable integration programs.

## Summary

By now, we have covered how Partner Engineering contributes to software ecosystems, using expertise in a developer platform to bring about integrations that delight customers. Though Partner Engineering is relatively new to the industry, it is an important role to understand and work with in an increasingly connected software landscape.

Give me a shout on Twitter or GitHub (@imjohnbo) if you have any callouts, thoughts, or questions. See you around the ecosystem!
