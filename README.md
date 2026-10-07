# Faseeh Ullah Jafar

Senior .NET engineer, based in Lahore. I've spent six years on C# and SQL Server backends, the last three on US teams working US hours. I'm open to senior .NET roles, either as a remote contractor or Employer of Record (EOR) hire for a US or EU company, or relocating with sponsorship to the UK, EU or Gulf. My notice period is 14 days.

Most of my work is in private client codebases, usually on systems that are already live and have outgrown their original design:

- On a billing platform for a US retail group, worst-case invoice generation took over 3 minutes. During the outage I traced it to unindexed hot tables and a stored procedure whose plan collapsed past 4.2 million rows. Emergency indexing got it down to 40 seconds.
- A clinical worklist for a US healthcare client went from 4 seconds to 300 ms with 120 providers using it at once. That came from Redis caching, server-side paging and query rewrites based on the execution plans.
- At Dev Vaults, a fintech platform, I led the backend move from legacy Java to .NET 8, with CQRS, saga orchestration and idempotent command handlers. Our tests were passing against a mocked broker while production failed, so I moved them onto a real broker under Testcontainers.

## Public code

**[saga-in-production](https://github.com/FaseehUllahJafar/saga-in-production)**

A checkout saga across six .NET 10 services, using Wolverine and RabbitMQ, with a SQL Server database for each service. It's built for the failures tutorials skip: a payment response lost after the charge went through, a timeout that doesn't tell you whether the step ran, a compensation that overtakes its own command. It has 75 tests covering fault injection with Toxiproxy, crash recovery, concurrency and idempotency, plus choreography and not-a-saga versions for comparison. It's the companion code for my [saga series on LinkedIn](https://www.linkedin.com/in/faseeh-ullah-jafar/recent-activity/all/).

**[InstructorSharp](https://github.com/FaseehUllahJafar/InstructorSharp)**

Gets typed, validated objects out of an LLM in C#. When a response fails validation, the library sends the errors back to the model and retries. It's built on `IChatClient` from Microsoft.Extensions.AI, with strategies for each provider and support for streaming partial JSON. 145 tests pass on .NET 10, .NET 8 and .NET Framework 4.7.2. Not on NuGet yet.

**[dotnet-firefighting-skills](https://github.com/FaseehUllahJafar/dotnet-firefighting-skills)**

Ten runbooks for .NET production incidents, including thread-pool starvation, connection-pool exhaustion, EF Core N+1 queries, cache stampedes and SQL Server plan regressions. Each one shows how to prove the cause before you change anything, orders the fixes by risk, and says what the fix breaks. They're packaged as Agent Skills for Claude Code, Copilot or Cursor.

## Stack

C#, .NET 10 and 8, ASP.NET Core, EF Core, SQL Server, Azure (Service Bus, Functions, App Service, Key Vault), Redis, RabbitMQ, Docker, Azure DevOps, Angular, React, TypeScript

## Contact

faseehullahdev@gmail.com · [LinkedIn](https://linkedin.com/in/faseeh-ullah-jafar) · [Portfolio](https://faseehullahjafar.vercel.app)
