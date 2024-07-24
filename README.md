# Attribution Extension Specification

- **Title:** Attribution
- **Identifier:** <https://stac-extensions.github.io/attribution/v0.1.0/schema.json>
- **Field Name Prefix:** -
- **Scope:** Item, Collection
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @m-mohr

This document explains the Attribution Extension to the
[SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.
Allows to provide an attribution, which is compliant with OGC API Collections.
This is commonly seen in web maps to give credit to e.g. the basemap provider.

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
  - [Collection example](examples/collection.json): Shows the basic usage of the extension in a STAC Collection
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:

- [x] Catalogs
- [x] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [x] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [x] Links (especially [Web Map Links](https://github.com/stac-extensions/web-map-links))

| Field Name  | Type   | Description                                  |
| ----------- | ------ | -------------------------------------------- |
| attribution | string | **REQUIRED**. A short text intended for presentation to a user, for example, in a corner of a map. |

The attribution is a short text intended for presentation to a user, for example, in a corner of a map.
Parts of the text can be links to other resources if additional information is needed.

The attribution element can contain HTML markup.
It allows a text string to import images and format text.
The capabilities are only limited by the markup language used.
It is RECOMMENDED to keep the attributions simple so that clients can render them properly,
ideally just plain text and potentially a link that points to additional information.
Additionally, clients may decide to restrict the HTML capabilities for security reasons.

## Contributing

See the [Contributor documentation](CONTRIBUTING.md) for details.
