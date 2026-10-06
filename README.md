# Faseeh Ullah Jafar

Senior .NET engineer with six years on ASP.NET Core, SQL Server and Azure, and Angular or React on the front end. I'm a Senior Software Engineer at Horizon IT Solutions. Before that I was at Devsinc and Zentech Solutions. Most of my work has been fixing performance on live systems and moving older .NET code onto services that can deploy independently.

## Work

**Horizon IT Solutions** (2025–now), billing and invoicing for a US retail group

- During an outage, cut the worst-case billing run from over 3 minutes to 40 seconds. The cause was missing indexes on hot tables and a stored procedure whose plan regressed once the table passed 4.2 million rows.
- Shipped the platform's first Azure OpenAI feature, which summarises documents and extracts fields from them. Responses are schema-validated before they're saved, and each document type has its own token budget.
- Cut build-and-deploy time from 27 to 15 minutes by rebuilding the Azure DevOps pipelines.

**Devsinc** (2023–2025), healthcare and fintech clients

- For a US healthcare client, cut a clinical worklist from 4 seconds to 300 ms for 120 concurrent providers, using Redis caching, server-side paging and query rewrites based on the execution plans. I also put four EMR systems (Redox, Athena, Epic, eCW) behind one gateway, with the HIPAA-protected data behind role-based access.
- At Dev Vaults (fintech), led the backend move from legacy Java to .NET 8 with CQRS, DDD and Saga orchestration. Our tests mocked the message broker, so they passed while production failed. I moved them onto a real broker under Testcontainers.
- Split a .NET monolith into four independently deployable services, and moved the slow cross-service calls onto AWS SQS.

## Projects

| Project | |
|---|---|
| [saga-in-production](https://github.com/FaseehUllahJafar/saga-in-production) | A checkout saga in .NET 10 with six services, Wolverine and RabbitMQ, and a SQL Server database per service. Each failure case has an integration test against real containers: a lost payment response, a timeout where you don't know whether the step ran, a compensation that arrives before its command, and a saga that stops without an error. |
| [InstructorSharp](https://github.com/FaseehUllahJafar/InstructorSharp) | A C# port of the Instructor library. It returns typed objects from an LLM and retries with the validation errors when the output doesn't validate. Source only for now, not yet on NuGet. |
| [dotnet-firefighting-skills](https://github.com/FaseehUllahJafar/dotnet-firefighting-skills) | Runbooks for ten common .NET production problems, including thread-pool starvation, connection-pool exhaustion, EF Core N+1 queries and SQL Server plan regressions. They're written as Agent Skills, so a coding agent can follow them during an incident. |

I'm also writing a [series on sagas](https://www.linkedin.com/in/faseeh-ullah-jafar/recent-activity/all/) on LinkedIn, and saga-in-production is the code that goes with it.

## Stack

- **Daily:** C#, .NET 10 and 8, ASP.NET Core, EF Core, SQL Server / T-SQL, Redis, Azure (App Service, Functions, Service Bus, Key Vault, AD B2C), Azure DevOps, Angular, React, TypeScript, xUnit
- **Architecture:** microservices, Clean Architecture, CQRS, DDD, sagas, event-driven design
- **Also used:** PostgreSQL, RabbitMQ / MassTransit, AWS, Docker, Kubernetes, Azure OpenAI, Python, Node.js

## Contact

[Portfolio](https://faseehullahjafar.vercel.app) · [LinkedIn](https://linkedin.com/in/faseeh-ullah-jafar) · faseehullahdev@gmail.com

Open to senior .NET roles. I can start on a remote contract or EOR without needing a visa, or relocate to the UK, EU or Gulf. My notice period is 14 days. I'm based in Lahore and currently work US hours.
