# Project MD
**9.20.2024**

## 1 ABSTRACT

_Project MD re-envisions how TIGA can provide documentation to clients. Leveraging pre-existing open-source tools, Project MD provides a more secure, accessible, and flexible documentation delivery system that can be adapted to the Industrial Internet of Things (IIoT)._

## 2 WHAT IS PROJECT MD

Project MD is a combined application of open-source tools pertaining to written documentation. The goal of Project MD was to provide a novel approach to documentation that can adapt to existing cybersecurity regulations and provide additional revenue sources for TIGA. 

## 3 CURRENT SYSTEM

Current client driven documentation efforts result in the production of either a word document or a SharePoint site. While both are equally feasible in providing satisfactory documentation, each format has shortcomings including but not limited to:

· Document Control

· Mass Revisions / Updates

· 3rd Party Handling / Access

· Server / Network Pre-requisites

· Formatting

## 4 HOW DOES PROJECT MD CHANGE THIS?

Project MD provides new possible documentation deliverable formats for clients, circumnavigating current document limitations. With Project MD, documentation can exist entirely on a GitHub repository owned and operated by TIGA and publish documentation to either a webhosted solution or a client server.

Webhosted solutions remove the need for clients to provide server access for documentation. With this solution, documentation can be written and pushed to the client without having to enter their network. Webhosted solutions are public but can be formatted with Documentation Authentication (private access) for a license cost which would be incurred onto the client.

Client server solutions require initial remote access but subsequently are hosted and ran locally, keeping documentation and sensitive materials safe. Locally hosted documentation still gains the benefit of a web-based platform but is only accessible via a local IP web address, allowing the site to be integrated as needed into systems and minimizing operator downtime.

The benefits of Project MD shine when it comes to updating documentation. With a pull request via the home repository, all documentation can be edited and changed remotely. This system eradicates the need to locate a word document or pull up multiple SharePoint sites for edits. Now, writers can make edits and push to **all** existing platforms at once.

**Use Case Example:** TIGA may provide standard documentation across several clients. As times change and systems update, all clients need the updated document. Traditionally this would require sending the clients a new copy or rewriting it in their current SharePoint. With Project MD, all we need to do is update the document in our local repo and push to main. The system will automatically update the document across all connected platforms.

![Image title](https://github.com/Mokrecho1/MkDocs_Test/blob/main/docs/images/testimage1.png?raw=true)

## 5 HOW DOES IT WORK?

Project MD works by leveraging a GitHub repository as the source of truth. From there, MKDocs, a static site generator, is installed into the repository. MKDocs takes all markdown documentation in the repository and generates a local site.

For hosting the site, we feed the GitHub repository, along with a MKDocs configuration file, into ReadTheDocs, a documentation deployment platform. ReadTheDocs will automatically build the front end leveraging the static site generation of MKDocs and provide a webhosted version.

After MKDocs and/or ReadTheDocs is established, any changes pushed to main via GitHub now automatically populate the static-site.

