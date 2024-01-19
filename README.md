## About project

The final project for the Building AI course - Signaling messages analyzer for testing voice services in the telecom world

## Summary

In the telecom world, there is a need to do tests to verify the implemented changes, the goal is that a machine can replace a human in certain actions. To verify the changes in the voice network, we need to perform E2E tests and then check if everything is as expected from the user experience and a signaling perspective for each test. The user only needs to choose which test scenario he wants to test, and the rest is automated from the execution of the test scenario to the verification. We would use AI to do the verification part from a signaling point of view with pass or fail results for each executed test scenario within the system environment.


## Background

We want to have a solution that will analyze the traces of voice calls with signaling messages inside for different test scenarios and this will save us time and human resources as we don't need to do it manually anymore.


## How is it used?

We use automated systems for testing in the telecom world, these systems use attenuators, shielded boxes, base stations, SIM cards, and probes (mobile phones, IP phones, analog modems) that use 2G, 3G, 4G, 5G signals from the live/lab network. With certain open source software like Jenkins, Gitlab, Docker, Cucumber, ReportPortal, and programming languages like Python we create an environment for automation and testing end-2-end voice services. Such a system is integrated with a tool for collecting signaling traces from the network. Our AI solution will analyze the collected traces for certain tests and will offer a pass or fail result depending on the signaling messages within the trace. The test can pass functionally from the user's perspective, but it goes the wrong way through the network, so the signaling analysis would declare that test a failure. The user of the system would select the tests he wants to perform via web GUI and after a certain time the test result would wait for him and he could devote himself to doing other things during that time.


## Data sources and AI methods

We need to collect as many signaling traces in pcap format as possible for certain test scenarios that have been manually verified by humans, they form a database against which the program will make comparisons while executing the test that we ran through the automation system. For each performed test in the system, there is a signaling trace in the database. We are collecting traces for the database on our own and choosing the parameters that we will use for comparison.

## Challenges

We are limited in time because it takes an average of 5 minutes to perform one test scenario through the automation system, so we can perform and analyze 10-15 tests in one hour. If we increase the number of probes that perform tests, then we can speed up testing with simultaneous execution and increase the number of performed and analyzed tests in one hour.

## What next?

We could use the same automated solution for testing and analyzing data services within the live/lab network.


## Acknowledgments

Source of inspiration:
- Implementation of Automated Testing Solution for Voice Services (M.Ivancic, N.Stokic, T.Zilic (Hrvatski Telekom)) - Published in: 2023 46th MIPRO ICT and Electronics Convention (MIPRO) - https://ieeexplore.ieee.org/document/10159634
