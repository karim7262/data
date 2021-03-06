# GSA Enterprise Architecture

> The Enterprise Architecture, Policy and Planning Division provides business-focused IT support for GSA customers at all levels of the organization.

The General Services Administration's [Enterprise Architecture](http://www.gsa.gov/portal/category/26815) team maintains a list of systems approved for use at GSA, called the [IT Standards Profile list](it-standards.csv). This list includes:

- Desktop software
- Server software
- Software as a Service (SaaS)

Make sure to **pay attention to the `Status` column**, as the list includes items that are `Approved`, `Pending`, and `Denied` (though there can be other values for the column).

The data is manually exported (for now) from [the official list in GEAR](https://ea.gsa.gov/#!/itstandards) on a regular (but best-effort) basis. See the Last Modified date on the CSV to see when it was last updated. Feel free to [open an issue](https://github.com/GSA/data/issues/new) to give us a nudge if we forget!

To see the latest-and-greatest list, [get on the GSA network](https://handbook.tts.gsa.gov/how-to-log-in/) and visit [GEAR](https://ea.gsa.gov/#!/itstandards).

## Updating the list

1. [Clone this repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository).
1. Connect to the GSA network ([VPN information](https://handbook.tts.gsa.gov/anyconnect/))
1. Follow either the scripted or manual steps below.

### Script

Requires:

- cURL
- Git
- Python 3

From this directory (`enterprise-architecture`), run the updating script:

```sh
./update.sh
```

### Manual

1. Visit [the canonical IT Standards list](https://ea.gsa.gov/#!/itstandards).
1. Only show the `Standard Name`, `Description`, `Category`, `Status`, `Deployment Type`, and `Approval Expiration Date` columns.

   ![column selection drop-down](columns.png)

1. Export the list as a CSV.

   ![export drop-down](export.png)

1. Save/rename the file as `it-standards.csv` in this directory.
1. [Commit the changes.](https://services.github.com/on-demand/github-desktop/add-commits-github-desktop)
1. [Send a pull request.](https://services.github.com/on-demand/github-desktop/pull-request-github-desktop)
