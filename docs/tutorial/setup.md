# CHKN Tutorial: Setup

Adobe provides documentation about local environment setup [here](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/overview.html?lang=en) and [here](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=en). I find the documentation somewhat scattered and confusing. Hopefully the walkthrough below will be helpful.

## Note on AEM Versions
The most current AEM versions at the time of this writing are AEM 6.5 and AEM as a Cloud Service (AEMaaCS). Adobe has been promoting AEMaaCS as the preferred arrangement.

A local AEMaaCS environment can be set up without any proprietary downloads or licenses, so that is what we will be using for CHKN development.

## Dependency Overview
To build and run an AEM project, we will need the following dependencies:
- Java 11 Java Development Kit (JDK)
- Apache Maven
- Node.js
- npm
- AEM author instance
- (Optional for now) AEM publish and dispatcher instances
- (Optional for now) If using an AEM dispatcher instances, Docker will be helpful to have

## Java 11
- Java 11 JDK [footnote: Java 8 is used in AEM versions prior to 6.5. Java 11 is used in the more current versions: 6.5 and AEM as a Cloud Service.]
    - TODO

## Apache Maven
Download Maven from the [Apache Maven Project website](https://maven.apache.org/download.cgi). Install Maven per Apache's [installation instructions](https://maven.apache.org/install.html).

## Node.js
TODO

## npm
TODO

## AEM instances
AEM architecture includes the notions of "author", "publish", and "dispatcher" instances. For the most complete testing of our code and to run an AEM project in production, all three are needed. However, to keep things simple and easy to understand, I am going to defer discussion of the publish and dispatcher instances until later in the tutorial. An author instance is adequate to begin learning AEM.

### Author Instance
TODO

### Publish Instance
Optional for now. If you do wish to set this up now, here are the steps:
- TODO

### Dispatcher Instance
Optional for now. If you do wish to set this up now, here are the steps:
- TODO

## CHKN Project Setup
- Clone https://github.com/adobe/aem-project-archetype
