[![Follow @ericthecurious.bsky.social](https://img.shields.io/badge/follow-@ericthecurious.bsky.social-whitesmoke?style=social&logo=bluesky)](https://bsky.app/profile/ericthecurious.bsky.social)
[![Contact me hello@ericthecurious.com](https://img.shields.io/badge/contact_me-hello@ericthecurious.com-whitesmoke?style=social&logo=gmail)](mailto:hello@ericthecurious.com)

# Welcome to Neurodevs 🧠🤖💜👋🏻

Neurodevs is an ecosystem of portable, open-source tools for real-time biosignal systems (and a few related domains) with a simple goal: make biosignal systems behave exactly as they say they do. Think boring reliability for real-time biosensors and biosignals.

The work toward that reliability is ongoing, and major version changes should be expected as the ecosystem matures.

## Problem situation

Neurodevs addresses a recurring problem seen across deployed biosignal systems:

Reliability most often breaks down at the point of runtime coordination between software and hardware, especially in long-running processes subject to unpredictable real-world conditions. Subtle failures in timing, state, buffering, or lifecycle management can accumulate over time, quietly undermining otherwise sound experiments.

A closely related problem is that when these systems drift or degrade, it is often difficult to tell what actually happened. Runtime behavior is often either opaque or only observable after the fact, once data has already been recorded or lost. Runtime issues such as timestamp jitter, clock drift, or dropped samples may only surface indirectly, if at all, and usually too late to intervene.

In practice, these systems may appear to function correctly while gradually deviating from their intended behavior. Data continues to flow, even as timing assumptions are violated or state transitions behave differently than expected. By the time a problem is visible, it is often no longer possible to distinguish between a genuine experimental effect and an artifact introduced by the system itself.

While some problems can be corrected during analysis, others result in irrecoverable loss of timing or state information.

## Approach

Neurodevs addresses these problems through **real-time systems orchestration**.

The guiding approach is to make runtime behavior explicit and observable, so that reliability is demonstrated continuously rather than reconstructed, validated, or inferred after the fact. This emphasis treats timing, state, buffering, and lifecycle behavior as first-class properties of the system rather than incidental implementation details.

The ecosystem is built on Node.js and TypeScript for their strengths in long-running, event-driven, and cross-platform systems. This allows the same code to run consistently across desktops, servers, embedded systems, and constrained environments, while integrating cleanly with native libraries and external tools written in languages such as C++ and Python.

The tools focus on reliability in the data acquisition and transport layers, supporting basic real-time signal processing while delegating heavier analysis to external applications via Lab Streaming Layer (LSL) or WebSockets. Typical workflows include applications written in Python, MATLAB, or C++, running either locally on the same network via LSL or remotely over HTTP(S) via WebSockets.

Wherever possible, this reliability is abstracted into the system itself rather than imposed on its users.

## Entry points and usage

Coming soon...

## Background

Many Neurodevs projects originated in applied R&D efforts supported by SBIR, STTR, and TACFI grants through my former employer, [Lumena](https://lumenalabs.com). Earlier versions were deployed on more than twenty U.S. Air Force bases worldwide in wellness and mindfulness training contexts, where real-world use hardened the system against failure modes that emerge in long-running biosignal deployments.

Neurodevs continues this lineage now as an independent, open-source ecosystem shaped by lessons learned from repeated deployment, maintenance, and long-term operation.

## Contributing

Contributions are welcome and reviewed carefully. Pull requests must follow test-driven development (TDD) by [the three laws](http://www.butunclebob.com/ArticleS.UncleBob.TheThreeRulesOfTdd): 

1. Do not write production code unless it is to make a failing test pass
2. Do not write any more of a test than is sufficient to fail
3. Do not write any more production code than is sufficient to pass the failing test

Collaboration beyond code is also welcome. If you are interested in ideas, research directions, or partnerships, you can reach me on Bluesky at [@ericthecurious](https://bsky.app/profile/ericthecurious.bsky.social) or by email at hello@ericthecurious.com.

Contract work is available at a professional rate.
