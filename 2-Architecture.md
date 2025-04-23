# 2\. Updated Architecture

The EUCAIM architecture focuses on a federated model in which nodes connect to the central core services but which also keep a reasonable degree of independence and autonomy. The technical requirements for the integration in the federated infrastructure relies on the model of tiers:

- Tier 1: Compliance with the metadata model for the datasets.
- Tier 2: Compliance with the data model for searching purposes, considering the use of a mediator component that translates the queries to the specific format of the data holder.
- Tier 3: Direct (through adoption) or indirect (through a mediator component) compliance with the data model for processing purposes.

[Figure 1](#fig_architecture_EUCAIM) shows a simplified diagram of the architecture explaining the interactions among the components according to the tier model.

![image](figures/image2-1.avif)

[Figure 1](#figur_architecture_EUCAIM). Simplified architecture diagram of EUCAIM.

The core services for the federation are shown in the upper part of the figure. The lower part represents a node that connects to the federation. The three tier levels described above are related to the following federation concepts:

- Tier 1: The datasets hosted by the federated node are registered in the central catalogue. Ideally, this is done through the exposure of FAIR Data Points that are used by the central catalogue to harvest the dataset’s metadata, although manual registration is also feasible for tier 1. Users can explore the metadata of the datasets registered in EUCAIM’s platform.
- Tier 2: The data of the federated node is searchable through its local searching service, which is queried by the federated search system through a Query Mediator component that transforms the query from EUCAIM’s model to the local model and vice-versa for the results. In case the local model already complies with EUCAIM’s one, the mediator component is still necessary for transforming the results and utilising the network communication middleware. The users can explore the actual number of studies fulfilling the search criteria defined by the user.
- Tier 3: The federated node has a materialisation component that makes the data available to the federated processing, according to EUCAIM’s model. The user will be able to run processing actions on the actual data, if the access to them is granted.

Components in grey relate to the node local services and components. Components in purple are tier-independent components of EUCAIM core services, and the LS-AAI component is an external entity that manages the common authentication model.

The following URLs forward to the EUCAIM Platform services

- Dashboard ([dashboard.eucaim.cancerimage.eu](http://dashboard.eucaim.cancerimage.eu))
- Catalogue ([catalogue.eucaim.cancerimage.eu](http://catalogue.eucaim.cancerimage.eu))
- Federated Search ([explorer.eucaim.cancerimage.eu](http://explorer.eucaim.cancerimage.eu))
- Negotiator ([negotiator.eucaim.cancerimage.eu](http://negotiator.eucaim.cancerimage.eu))
- Helpdesk ([helpdesk.eucaim.cancerimage.eu](http://helpdesk.eucaim.cancerimage.eu))
- Reference Node at UPV ([eucaim-node.i3m.upv.es](http://eucaim-node.i3m.upv.es))
