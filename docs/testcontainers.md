# Test Containers

## Testing 

Testing our code is super important. Over the years I've used various test libraries/tools including:

* [SpecFlow](https://specflow.org/) with C# and ASP.NET
* [Selenium](https://www.selenium.dev/) with C# and ASP.NET
* [Cucumber](https://cucumber.io/) with Java
* [RSpec](https://rspec.info/) with Ruby
* [Cypress](https://www.cypress.io/) with TypeScript and Node
* [WebApplicationFactory](https://learn.microsoft.com/en-us/aspnet/core/test/integration-tests?view=aspnetcore-7.0#basic-tests-with-the-default-webapplicationfactory) with .NET Core
* [In-MemoryDatabase](https://learn.microsoft.com/en-us/ef/core/providers/in-memory/) with Entity Framework and .NET Core

You'll notice the last link here actually displays on the site as "In-memory (not recommended)", which came as a huge disappointment to earlier in 2023 when I found out Microsoft would no longer maintain the In-Memory Databases that had been in multiple previous versions of .NET Core.

## Enter Test Containers

As a super charged replacement for the much-maligned In-Memory databases, [Testcontainers](https://testcontainers.com/) provides much more than the ability to persist state as part of your test suite. Building on Docker containers, Testcontainers allows you to write tests for your applications locally and run them in the cloud (CI/CD) using real services wrapped in Docker containers.

## Basic Example

Recently a lot of the code I have written has been integrating with Azure and Testcontainers has great support commonly used Azure Services on their [modules](https://testcontainers.com/modules/?language=dotnet) page. 

The documentation provided by Testcontainers is great and I've followed this to setup a [basic](https://github.com/gbrown31/TestContainers.Basic) set of tests using Azurite for Blob Storage and SQL Edge with Entity Framework.