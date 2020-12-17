# Open sourcing guideline

## Why and what to open source?

### Why

Open sourcing software is a great tool for showcasing new innovation, building company or personal brand image or as a gesture of good will towards the software development community at large.

If software component or library is critical in terms of trust, continuity or support for upcoming years, it can be crucial for the success of said tool to open source parts of it. By doing so, the user can rest assured that they have the required knowledge and tools to build their solutions on top of something that can be maintained and fixed if a need arises in the future.

If your software has a large user base, it can be beneficial for the ongoing development of it to enable its users to develop the features they need on top of it or fix bugs independently. It's in vested interest to submit the fixes and new features upstream

### What

- Software that can be benefit for others or could benefit from external contributions
- Libraries and tools that help third parties to adopt or integrate with your product
- Software that is not intellectual property of Visma
- Critical components that rely heavily on public trust, such as cryptographic algorithms

## Requirements

### Documentation
Your project needs to have at least minimum amount of documentation available. The documentation can be in a single file or distributed over multiple different files, and the best practice is to write it in MarkDown format.

The standard way of structuring the documentation is:
 
 #### README.md 
 
 The documentation, and often project landing page, that's rendered by many SCM solutions like GitHub, GitLab and similar. If documentation is written in a single file, it should be this one. 
 
 The `README.md` should contain short description of the project, information about possible dependencies, installation instructions and preferably a short usage example.
 
 #### INSTALL.md
 
 In some cases, the installation instructions might be complex either by the nature of the application or by divergences between different platforms that it is designed to be used on. In such case the installation instructions should be separated to this file. If it is created, it should also be linked from the `README.md`.
  
 #### CONTRIBUTING.md
 
 Contribution guidelines for external contributors. Often contains instructions how to submit code and documentation contributions, and a short explanation of the steps that will be taken before the contributed code is merged to the project.
 
 #### LICENSE.md
 
You need to have a proper license. This should almost always be MIT.

### Security

The codebase should be scanned by SAST / SCA tools - where available - prior to the initial release, and at least the higher severity issues fixed. 

While open source software is transparent and able to be vetted independently as per its design, exposing your users to security vulnerabilities can be very harmful for reputation of your tool, brand and those of Visma.

## Recommendations

### Best practices

You should strive to follow the best practices of chosen techologies. These may be related to packaging, distribution, code quality and such. The best practices exist and have cultivated over time for a reason, and following them often makes it much easier to integrate and maintain your software by your userbase and yourself. It also sets the base quality expectations for external contributions.

### Code scanning / Code quality

If possible, you should deploy automated linters, code quality checkers and security scanners as part of your development pipeline. GitHub for example offers multiple tools that can be deployed really easily to perform scans even before the code gets merged. The scans often take place in Pull Request, and should be completed successfully before the code review is done.

These do not only guarantee a certain level integrity, but also help to guide your contributors through the forest of good coding and security practices.

### Maintenance

Open source is a living organism, and needs love and care throughout its life cycle. If you make the choice to release a project, you should make sure you have the time to maintain it too. This includes answering to issues opened by users, reviewing incoming pull requests from community, updating the documentation and code dependencies where needed.

Please note that you don't have to do it all yourself! It's prefectly OK to ask for help, and often users that open issues for a bug or feature request are willing to contribute the fixes or features themselves.

In the case you wish to stop maintaining your open source software, you should mention it clearly in the documentation, and potentially linking to a maintained fork in case someone from the community might take over the maintenance duty.

### Communication / Code of Conduct

Make sure that you follow good, inclusive communication practices - just like you do in your daily work life. Code of Conduct is here to help you with this too, it sets the expectations through requirements not only for the maintainers, but also the community opening issues or pull requests. 

Having CoC available makes it easy to remove / ban abusive users without leaving a suspection of censorship.
