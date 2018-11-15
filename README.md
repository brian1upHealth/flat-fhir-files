# flat-fhir-files

This repository contains the data that we host on the demo FHIR servers exported in NDJSON format.
The data can be used for population-level analysis that would be very difficult to do using fhir API calls.
Once we add `bulk data` support to the fhir servers, you will be able to get that data directly. Until then,
you can use these files, as if they were downloaded from a bulk data server and experiment with them even
before we have working flat fhir implementation.

- The `r2` folder contains the data for the DSTU2 server at https://r2.smarthealthit.org.
- The `r3` folder contains the data for the STU3 server at https://r3.smarthealthit.org.
- There is one file per resource type. The file can be empty if there are no records of that type

There might be some differences between this data and the one that you would receive from the servers:

1. The servers are live. People can insert, delete or modify resources but then the servers are reset to their default state each night. Those "changes" are not represented here. Instead, you get a snapshot of that default state that we reset the data to.
2. The `meta.lastUpdated` may have different value than what you see online.
3. Resources that have numeric IDs will have their ID prefixed with "RES" on the live servers.
4. Resources that do not have IDs will have a generic ID on the live servers.
