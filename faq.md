---
layout: base-fullwidthcontent
title: FAQ
subtitle: Get answers to some of your common Microlam questions.
permalink: /faq/
---

## What is your license?

Microlam is an Open Source project licensed under the [MIT License](https://github.com/microlam-io/microlam/blob/master/LICENSE.txt).

## Where can I get it?

Microlam is published in Maven Central you need to just to add a dependency our core artifacts in your `pom.xml` to get Microlam. We recommend you start your Microlam experience via our [Getting Started guides](/get-started).

## Microlam is stable?

Our API is not 100% stable but will be officially stable when reaching v1.0. Anyway our code is very small and it should be very easy to use new releases.

## What is GraalVM?

[GraalVM](https://www.graalvm.org) is a universal virtual machine for running applications written in various different languages, as well as providing the ability to compile JVM bytecode to a native executable (this native executable runs a special virtual machine called SubstrateVM). These native executables start much faster and can use a lot less memory than a traditional JVM, however not every JVM feature is supported, and some are more limited than normal.

For example by default reflection in GraalVM will not work, unless a class/member has been explicitly registered for reflection. This is normally achieved by listing every class, method, field and constructor in a JSON file, and passing this as a parameter into the native image build. This obviously gets quite cumbersome for all but the most trivial projects.  Microlam provides a way to automatically generate the configurations while running tests.

## What's the difference with other Java frameworks like [Quarkus](https://quarkus.io) and [Micronaut](https://micronaut.io) ?

These 2 frameworks are great frameworks doing 1,000,000 things Microlam cannot do... but Microlam scope is much more reduced and dedicated to AWS Serverless which gives him the advantage of being simpler and more focus on this small domain.
