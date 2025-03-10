# Requirements

When new software comes to life, there are usually certain requirements that need to be met. This can be anything from a simple task, such as downloading or converting files, to visualizing data, to a complex problem that needs to be solved in a time that a human would not be capable of.  

Normally, a complete [requirements analysis](https://en.wikipedia.org/wiki/Requirements_analysis), as a separate sub-area of [software engineering](https://en.wikipedia.org/wiki/Software_engineering), would cover numerous topics. Here, we want to focus primarily on the use case or functional/behavioral requirements from the user's perspective.  
We will largely ignore questions relating to stakeholders, measurable goals, a contract-like list of requirements or the various types of requirements besides the functional requirements. Let's assume that these questions have already been clarified at this point so that we can concentrate fully on the implementation of the software.  

## One simple use case

As already mentioned, the primary use case should be as follows:  
> A tool that visualizes the money spent over time by knowing the resources used and the time elapsed.  

Or to put it simply: in the end, the user will always have a tool that is started like a stopwatch, but instead of time, money is ticking away.  

### Minimum requirements

#### Functional

- **MF 01.1** Possibility to define multiple different resources as input
- **MF 01.2** Possibility to define the costs per time intervals for each resource as input
- **MF 02.1** Possibility to start a stopwatch
- **MF 02.2** Possibility to stop the stopwatch
- **MF 03.1** The costs must be calculated by multiplying the costs per resource by the number of resources by the elapsed time of the stopwatch
- **MF 03.2** Output of the costs calculated
- **MF 03.3** Output of the time elapsed
- **MF 03.4** Ability to persist the results of the time/money recording job as outlined in MF 02.1, MF 02.2 and MF 03.1

#### Behavioral 

- **MB 01.1** While stopwatch is running, the to that point in time calculated money should be displayed every second instead of a stopwatch
- **MB 01.2** When stopwatch is stopped, a summary should be displayed, showing resources, time and money invested
- **MB 02.1** The application should correspond to the expected standard behavior of its respective implementation type. For example, if it is an implementation of a console application, it is to be expected that configuration values are passed via parameters and an interactive dialog guides you through the application. If it is a desktop application, it is expected to be operated using buttons in the window.

### Optional requirements

#### Functional

- **OF 01.1** Possibility to distinguish between multiple time/money recording jobs as unique data records
- **OF 01.2** Possibility to pause time/money recording jobs
- **OF 02.1** Possibility to abstract the costs in roles that are bound to the specific resource
- **OF 02.2** Possibility to group resources as teams, that can be assigned like single resources to a single time/money recording job
- **OF 02.3** Possibility to categorize resources into different resource types
- **OF 02.4** Have proper metadata (like name, status, ID, etc.) on each record as it is plausible
- **OF 02.5** Have automatically generated metadata like create/modified date on time/money recording job records
- **OF 03.1** Entered configuration data such as resources, teams, categories should be remembered and must be saved (at the latest when the application is closed)
- **OF 03.2** Entered as well as recorded time/money jobs should be remembered and must be saved (at the latest when the application is closed) including all data

#### Behavioral 

- **OB 01.1** Ability to start, stop, resume and stop again a time/money recording job
- **OB 02.1** Ability to easily reuse and select from already defined teams and single resources when starting a new time/money recording job
- **OB 03.1** Recorded time/money jobs should contain a short summary in which the costs are broken down by resource type
- **OB 03.2** A history should display the entered and recorded time/money orders with their most important metadata

## User Stories

In order to have a more contemporary and tangible representation of the requirements, we translate the stated requirements into user stories.

### Minimum requirements

- **Story M1** "As a user I want to define resources with hourly costs so I can use them as input values to a time/money recording job. The job should calculate the costs by multiplying the costs per resource by the number of resources by a given time."  
==> Requirements **MF 01.1**, **MF 01.2**, **MF 03.1**
- **Story M2** "As a user I want to be able to start and stop a stopwatch whenever I want so that I can measure the time for a time/money recording job."  
==> Requirements **MF 02.1**, **MF 02.2**
- **Story M3** "As a user I want to see the results of the calculation while the stopwatch is running (at every elapsed second) and when the stopwatch is finished so that I can see the development of costs over time and to refer to it later on."  
==> Requirements **MF 03.2**, **MF 03.3**, **MB 01.1**
- **Story M4** "As a user, when the stopwatch is stopped, I want to have a summary of the job displayed, showing resources, time and money invested. Also I want to have an option to save the results of the job."  
==> Requirements **MB 01.2**, **MF 03.4**
- **Story M5** "As a user, I expect a user experience that corresponds to the type of implementation, so that I can work with the application in the same manner as I am used to with similar types of applications."  
==> Requirements **MB 02.1**

### Optional requirements

- **Story O1** "As a user I want to be able to distinguish between and handle more than one named time/money recording job so that I'm able to prepare, review, pause and resume jobs attached to different sets of resources."  
==> Requirements **OF 01.1**, **OF 01.2**, **OB 01.1**
- **Story O2** "As a user, I want **(A)** to use roles to address costs to a specific resource, **(B)** group resources as teams that can be addressed to time/money recording jobs likewise to single resources, and **(C)** be able to categorize resources so that I have a better overview of available resources and can choose from predefined teams as well as individual resources when I start new time/money recording jobs."  
==> Requirements **OF 02.1**, **OF 02.1**, **OF 02.3**, **OB 02.1**
- **Story O3** "As a user, I want to collect and store plausible metadata with configuration and progress data as well so that I can see a short summary in which the costs are broken down by resource type for each job and to have a history of all time/money recording jobs."  
==> Requirements **OF 02.4**, **OF 02.5**, **OB 03.1**, **OB 03.2**
- **Story O4** "As a user, I want entered and processed data to be stored automatically so that I can reuse data of former sessions and resume paused jobs later on."  
==> Requirements **OF 03.1**, **OF 03.2**
