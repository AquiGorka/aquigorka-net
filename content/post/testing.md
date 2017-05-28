+++
date = "2017-05-28T11:39:51+02:00"
title = "Testing"
thumbnail = "/images/testing.jpg"
+++

Lately I've been learning about this awesome practice referred to as "testing" - in a nutshell, it verifies specific functionality with automated scripts (tests) so that whenever you add new features or fix some bugs, the prior features/functionalities still work.

> You create a system, you add features to a system, you realize you broke some stuff the system was doing correctly, you go and fix it and then you publish the new features.

Then came the layers of tests: *unit, integration/functional, smoke, regression, acceptance, system & pre flight*. Personally, I have a little bit of experience with some of the layers and will describe here the way I interpret the ones I use and how they help out.

Lets use as an example a website that consumes and api for items.

## Unit tests

The simplest type of tests (very powerful too), these will verify the smallest of functionalities (atomic). In our website example, the api we will surely have a handler function for a given endpoint. This type of tests will ensure the handlers return the correct headers and content every time they receive the same parameters.

## Integration/Functional tests

Following up on the layers, this type of tests will integrate the different atomic functions and ensure a greater system has defined functionalities to a given set of inputs. In our example, we should have a running server that will accept requests to the endpoints that in turn integrate the different handlers, hence this types of tests will have a server up and running and will test the server's api endpoint to behave and return data as expected when the given parameters stay the same.

## Acceptance tests

At the next level of interaction to a system, users come into play. This is where tests have to maintain the system specifications - at the user level. In our example this level comes to us at a browser: let's say the user visists a certain page and the list of items gets rendered after a request to the api endpoint. This tests will ensure that the system will deal properly with all the possible outcomes of such flow (from a fully working flow where the request is a success and the items are rendered in a specific fashion in the webpage, to scenarios where the request fails with different error codes).

This type of tests require help from other systems that simulate/control browsers in an automated fashion. There are some options out there and I have been working with browserstack and selenium + chrome and firefox drivers.

There you go. It is my intention to keep learning and keep understanding the differences in every layer (and possible layers to come) and how to apply and benefit from them - and when I do, I will share such knowledge.

Cheers,<br />
Gorka


### References

https://stackoverflow.com/questions/520064/what-is-unit-test-integration-test-smoke-test-regression-test
