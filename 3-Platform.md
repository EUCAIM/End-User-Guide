# 3. Components of the platform
This section briefly describes the components of the platform, updating the descriptions provided in deliverables D5.1 Early release of the Data Federation Framework and D4.3: First rules for participation report. The deliverable is not an extensive description of the architecture, which is kept continuously updated in an online document [https://eucaim.gitbook.io/architecture-of-eucaim/](https://eucaim.gitbook.io/architecture-of-eucaim/).

## 3.1. The Dashboard
The Dashboard is the entrypoint to the platform and contains the general information about the available datasets and the links to the different services of EUCAIM’s architecture. The Dashboard includes the main information and the links to the different services and applications, although it does not exchange information from the rest of the services. A detailed description of the functionality of the Dashboard is provided in D4.7 First EUCAIM Dashboard.

## 3.2. The Catalogue
The catalogue contains the metadata of the datasets within EUCAIM. Through the filtering of and the browsing through the public catalogue entries, a user can freely look for datasets that are relevant to their research. Only after they have found a suitable dataset, a request can be made to access the actual data through the Negotiator.

## 3.3. The AAI
Some services in EUCAIM allow anonymous access (Dashboard and the Catalogue). Those services provide access to general information, onboarding processes and aggregated data. Finer-grain searching and data access require authentication and authorisation.

Authentication and Authorisation in EUCAIM relies on the Life Sciences AAI[1]. LS AAI is the commonly agreed AAI framework for Life Sciences Research Infrastructures. It relies on the AARC blueprint[2] and supports the EDUGain Federation (which serves most academic and research organisations in Europe), as well as other public Identity Providers. The process of registering in EUCAIM involves two steps:

Creating an account on the LS-AAI environment. This enables linking your institutional or public credentials to an LS-AAI account so you can use your institutional IdP for authenticating.

Enrolling in the EUCAIM VO Group. Federated search and negotiator services of the EUCAIM platform are available only to the members of the EUCAIM VO group.

The instructions for the sign up and enrollment of users are described in Annex I of this document.

## 3.4. The Federated Search
Federated search enables users to retrieve the number of subjects that fulfil a specific criteria. The federated search provides a user interface that interacts with a broker that distributes the query to the different providers registered. The federated search results are linked to the catalogue through hyperlinks. Figure 2 shows a schema of the interaction among the three above components.

![image](figures/image3-1.avif)

Figure 2. Schema of interactions among the components of the Federated Search. The Federated Search cores services sends the queries to the registered data holders and retrieve the aggregated results from them. The results are shown in the federated search GUI which links the results to the additional information on the datasets available in the catalogue.
The federated search will incorporate progressively more providers and datasets, as well as more searching criteria.

## 3.5. The Access Request
Access request is initiated from the catalogue and it is managed by the negotiator component. Information about the datasets that a user would like to access is transferred from the catalogue to the negotiator tool, where the data requester can submit an application, which is processed by the EUCAIM manager and the dataset responsible, on behalf of the access committee who is the body that effectively performs the evaluation of the application. Information is exchanged through the negotiator communication system, including the access link to the dataset. Figure 3 shows the interactions among the components.

![image](figures/image3-2.avif)

Figure 3: Interactions in the access request process. Access request starts from the catalogue, which triggers the connection to the negotiator passing all the information needed through. Interactions between the dataset responsible (on behalf of the Access Committee) and the data requester are performed through the negotiator, ending up with the transfer of the access link to the dataset in the data holder.
