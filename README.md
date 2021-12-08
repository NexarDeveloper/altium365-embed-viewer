# Altium 365 Embed Viewer

- [Embedding Uploaded Data on a Website](https://www.altium.com/documentation/altium-365/personal-space#!embedding-uploaded-data-on-a-website)
- [Embed via URL with Altium 365](https://docs.google.com/document/d/1CooHtbmdMCez44K1UdDOZ4InWpR_MrrxITT4Y4chx_I/edit#)
- [Example](https://www.altium.com/viewer?token=akrWFsQWqEa6Qk7RJPmbCyNY)


## Common Step: Upload Files

Upload files to the personal space "Files", e.g. [sample-1/Kame_MB.zip](sample-1/Kame_MB.zip)

## Way 1: Embed with a Link

Click `...`, select `Share` and click `Copy Link`.
As a result, you get a link like:

<https://365.altium.com/files/43813802-47E4-4E9F-A52C-EAED1BDB57AB>

If the above link is opened from this page then the browser simply navigates to
another page with the interactive CAD files viewer.

But when a user posts such a link on one of our partner websites supporting
`oEmbed`, then a page displays the CAD viewer as embedded content.

- [oEmbed home](https://oembed.com/)
    - [providers](https://oembed.com/providers.json), one of them is "Altium LLC"

## Way 2: Embed HTML Snippet

Click `...`, select `Embed`, enable the "Allow embedding this design anywhere on the web", copy the HTML snippet.

```html
<iframe src="https://personal-viewer.365.altium.com/client/index.html?feature=embed&source=43813802-47E4-4E9F-A52C-EAED1BDB57AB&activeView=SCH" width="1280" height="720" style="overflow:hidden;border:none;width:100%;height:720px;" scrolling="no" allowfullscreen="true" onload="window.top.scrollTo(0,0);"></iframe>
```

Use the snippet on a web page, e.g. [sample-1/Kame_MB.html](sample-1/Kame_MB.html)

```html
<html>
<body>

<p>Embedding A365 viewer:</p>

<iframe src="https://personal-viewer.365.altium.com/client/index.html?feature=embed&source=43813802-47E4-4E9F-A52C-EAED1BDB57AB&activeView=SCH" width="1280" height="720" style="overflow:hidden;border:none;width:100%;height:720px;" scrolling="no" allowfullscreen="true" onload="window.top.scrollTo(0,0);"></iframe>

</body>
</html>
```

## Appendix

### oEmbed "Altium LLC"

<https://oembed.com/providers.json>

```json
    {
        "provider_name": "Altium LLC",
        "provider_url": "https://altium.com",
        "endpoints": [
            {
                "schemes": [
                    "https://altium.com/viewer/*"
                ],
                "url": "https://viewer.altium.com/shell/oembed",
                "formats": [
                    "json"
                ]
            }
        ]
    },
```
