## ESA EarthCODE experiments as GeoDCAT and STAC profile 

This building block shows a possible profile of GeoDCAT supporting semantic annotation and inclusion of the three STAC extensions used by EarthCODE:

- themes
- osc
- cf

When provenance is included, the record `properties` describe the workflow run as a PROV Activity (`ogc.ogc-utils.prov-activity`).

### wf4ever (deprecated)

OSPD 2025 identified the wf4ever vocabularies (`wfprov`, `wfdesc`, `wf4ever`) as a useful level of abstraction for workflow provenance, between generic PROV and platform-specific records. wf4ever is no longer maintained, so it is deprecated here: these building blocks no longer depend on the wf4ever building blocks, and the focus has moved to the simpler task of defining activity types in a governed register (the activity-type register), which are used to type PROV activities. wf4ever terms already used in the examples are kept, with their prefixes declared, but are not required.

The SHACL shapes in this block check wf4ever traces (such as the Kind Grove example) for consistency; they only apply to data typed with `wfprov` classes.
