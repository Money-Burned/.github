# Contributing to "Money Burned"

Contributing to "Money Burned" means first of all submitting your own implementation of the generically formulated specifications (see [/doc/requirements.md](/doc/requirements.md)) in compliance with the rules listed here and the minimum information on how your project was created and how your approach corresponds to the specifications.  

To participate, you need an invitation to the organization. Please make sure that you agree to the organization's terms and conditions before requesting to become a contributing member.  

## Getting started

### Access to "Money Burned"

At the moment, there is no self-service. We are sure that it will be sufficient if you send us a brief request by email to `money-burned [at] gmx [dot] org` and give us a very rough outline of what you have in mind.  

### Repo creation 

#### Naming conventions

When creating your repository, please stick to the following naming pattern:  
`mb-frameworkname[-subframeworkname][-projecttype]`  

- always start with "mb-"
- please only use lowercase letters
- no spaces
- **framework** should be a basic reference to the technology stack or software development platform used - there is no need to be specific about versions or variants
- **sub framework** is optional if differentiation on nuances is necessary
- **project type** is optional and should help to differentiate between types of frontends or UI approaches

Examples:
```
mb-asm
mb-cpp-console
mb-cpp-qt
mb-java-spring
mb-java-qt
mb-javascript
mb-javascript-vue
mb-nodered
mb-python-console
mb-python-qt
mb-unity
```

It would be good to mention in the description of the repository that it is based on "Money Burned", as well as the project type and the chosen software development environment.  
It could be something like this: _A "Money Burned" PROJECT-TYPE-A implementation based on FRAMEWORK-B_.  

If you are in any doubt, please contact the [core team](https://github.com/orgs/Money-Burned/teams/core).  

#### Special cases

Just in case you plan to create multiple projects for a framework that have a single resource to be referenced by those projects (e.g. libraries, packages, etc.), this section is for you.  
Please create a separte repository whenever more than one of your project repositories are intended to use it. If you'd like to provide a library that only one of your projects are going to depend on, it is okay to include this dependency directly inside your project.  

##### Example #1 - Shared library:

```
. mb-yourimplementationframework-specialguitec1
├─ src
└─ doc
. mb-yourimplementationframework-specialguitec2
├─ src
└─ doc
. mb-yourimplementationframework-lib
├─ src
└─ doc
```

##### Example #2 - Included library:

```
. mb-yourimplementationframework-specialguitec
├─ src
|  ├─ gui
|  └─ lib
└─ doc
```

#### Template

In order to offer a similar user experience across all repos and to ensure a minimum level of content quality, we ask you to use our template. You can find it at [.template-project](https://github.com/Money-Burned/.template-project) and it is possible to use it when creating a new repository.  

In addition to a basic structure, you will also find a `README.md`. Please note the checklist at the end of the file and fill in the required minimum of information before you make your implementation of "Money Burned" available to the public.  

To share your knowledge with others, we suggest that you explain your software development approach to interested people by going into more detail in the included `dev-approach.md` file. We give you some key points there that we think you can probably cover.    

#### Folder structure

It's not that easy defining a complete framework or platform independend folder structure. There are so many different patterns and flavors: Some people prefer full names, some don't. Some people are keen on lots of folders, some are not.  
If the choosen approach of yours or the best practice guidelines given by the technology you selected are more suitable, please feel free to adapt whats best for you. We think scenario over hard rules will fit way better.  

With our template repo, we have taken up a currently common idea of a modern Open Source folder structure and propose to follow this idea.  

In case you're missing some of the usual suspects, a few words about them:

- folders _"build"_, _"packages"_ and/or _"artifacts"_ - without great benefit, because it's all about code
- folder _"test"_ - no need in the first place but feel free to add
- folder _"res"_ - would be a good place for resources like graphics, PDF, screenshots, etc.
- folder _"samples"_ - well, isn't the whole project a sample in a way?
- folder _"lib"_ - only relevant, if there is a 1-to-1 relation to your project (see [above](#special-cases))

Here are some more good ideas, put together [Soulaiman Ghanem](https://medium.com/code-factory-berlin/github-repository-structure-best-practices-248e6effc405) and [David Fowler](https://gist.github.com/davidfowl/ed7564297c61fe9ab814).  

#### Let useres know about our intentions

Please make sure that the application you are developing - _if it has a user interface_ - contains a reference to the organizational profile of "Money Burned" including a hyperlink.  
In addition to the the link back to "Money Burned" in your documention/README, you also should include the link to the profile page ([https://github.com/Money-Burned](https://github.com/Money-Burned)) into the application, where it is visible to the users of your implementation.  
You are free to place it where it fits best for you. This could also be done in the info dialog or in the credits.  

### The central implementation register

It is nothing other than the table with the examples that you have surely already seen on [profile page of "Money Burned"](./profile/README.md). It contains all completed implementation repositories. To be included in the list, please contact the [core team](https://github.com/orgs/Money-Burned/teams/core) for a quick review. If everything complies with our [code of conduct](./CODE_OF_CONDUCT.md) and you are willing to make your implementation of "Money Burned" available to the public, we will add this entry.  

### Licensing

Yes, please [attach a license to your project](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository). We use an open source license based on the [MIT license](https://en.wikipedia.org/wiki/MIT_License) and have already included it in the project template. If you are okay with that, we appreciate it. At the very least, it must be open source and a reference to "Money Burned" with a link to the GitHub organization must be provided.

## Maintaining your project

As you have already guessed, this is entirely up to you. We are happy if you take care of what you have created and hope that together we can help to make software development a little more transparent and easier to understand for beginners and interested parties in the long term.  

We hope you have a good time and enjoy working on this collection of examples. Please do not hesitate to contact us if you have any questions or ideas of your own.  

Thank you!  
