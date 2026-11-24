# ESA EarthCODE Building Blocks

OGC Building Blocks for the metadata published by [ESA EarthCODE](https://earthcode.esa.int/) in the
[Open Science Catalog](https://opensciencedata.esa.int/): GeoDCAT / STAC / OGC API Records profiles for
EarthCODE experiments, products and workflows, and the workflow provenance they carry.

| Block | Identifier | Describes |
|---|---|---|
| [common](_sources/common) | `ogc.esa.earthcode.common` | the shared EarthCODE STAC / Records profile and common definitions |
| [experiments](_sources/experiments) | `ogc.esa.earthcode.experiments` | an experiment record: one workflow run |
| [products](_sources/products) | `ogc.esa.earthcode.products` | a product collection, optionally a PROV entity |
| [workflows](_sources/workflows) | `ogc.esa.earthcode.workflows` | a workflow record: the reusable workflow description |

## Dependencies

This register imports the
[Open Science Workflows Building Blocks](https://github.com/ogcincubator/bblocks-openscience) register
(`ogc.osc.*`), which holds the shared workflow-provenance profiles, together with the OGC default
register, OGC API Records and Processes, and STAC.

These blocks were previously published in the Open Science register as
`ogc.osc.prov-examples.geodcat-stac-earthcode.*`.

## wf4ever (deprecated)

OSPD 2025 identified the wf4ever vocabularies (`wfprov`, `wfdesc`, `wf4ever`) as a useful level of abstraction for workflow provenance, between generic PROV and platform-specific records. wf4ever is no longer maintained, so it is deprecated here: these building blocks no longer depend on the wf4ever building blocks, and the focus has moved to the simpler task of defining activity types in a governed register (the activity-type register), which are used to type PROV activities. wf4ever terms already used in the examples are kept, with their prefixes declared, but are not required.

The `experiments` block keeps SHACL shapes (`shapes.shacl`) that check wf4ever traces for consistency; they only apply to data typed with `wfprov` classes.

## Building locally

```shell
./build.sh   # run the postprocessor (output in build-local/)
./view.sh    # browse the result at http://localhost:9090/
```
