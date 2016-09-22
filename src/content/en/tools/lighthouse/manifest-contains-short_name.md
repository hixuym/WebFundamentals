project_path: /web/_project.yaml
book_path: /web/tools/_book.yaml
description: Reference documentation for the "Manifest Contains short_name" Lighthouse audit.

{# wf_updated_on: 2016-09-21 #}
{# wf_published_on: 2016-09-21 #}

# Manifest Contains short_name  {: .page-title }

## Why the audit is important {: #why }

After a user adds your app to the homescreen, the `short_name` is the text that
is displayed on the homescreen next to your app icon. In general, it is used
wherever there is insufficient space to display the full name of your app.

## How to pass the audit {: #how }

Add a `short_name` property in your Web App Manifest.

    {
      ...
      "short_name": "Air Horner",
      ...
    }

Chrome's [maximum recommended
length](https://developer.chrome.com/apps/manifest/name#short_name) is 12
characters.

Check out the [How to pass the audit section](manifest-exists#how) of the
"Manifest Exists" audit for a list of guides that teach you how to properly
implement and test "Add to Homescreen" support in your app.

## What the audit tests for {: #what }

*Use this information to determine if the audit is relevant to your needs
or is returning incorrect results.*

Audit passes if the manifest contains either `short_name` or `name` property.
The manifest that Lighthouse fetches is separate from the one that Chrome is
using on the page, which can possibly cause inaccurate results.