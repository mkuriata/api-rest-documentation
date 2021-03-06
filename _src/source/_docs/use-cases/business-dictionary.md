---
title: TransAPI Business dictionary
is_use_case: true
side_menu:
  - title: Authorization use cases
    url: /use-cases/authorization-use-cases/
  - title: TransAPI Business use cases
    url: /use-cases/transapi-business-use-cases/
  - title: TransAPI Business dictionary
    url: /use-cases/transapi-business-dictionary/
    active: true

---

## Offer types ##

* **Public** - offer is visible and available for all Trans.eu platform users immediately. Regardless of whether they are employees of the same company, corporation, or whether they belong to a common cluster.
* **Private** - offer is visible and available only for the employees of the same company as the oferrer.
* **Cluster** - offer is visible and available to employees of companies that are members of the cluster. The offer becomes visible in cluster right after being added.
**Note:** a company can be a member of many clusters, and each of them has a separate identifier to be specified during offer adding. 
For ex.
 
```json
{
"type":  "cluster",
"clusters" : [
    { "id": 123}
 ]
}
```

## Special identifiers

Some APIs introduce special type of identifiers referred to as **special identifiers**. Special identifiers can be used
instead of numerical identifiers (check respective API specifications where you can use them).

Examples:

- `@me` get resource in context of current user
- `@company` get resource in context of current users company
- `@company-contractor` get resource in context of current users company, where that company is in a role of contractor
