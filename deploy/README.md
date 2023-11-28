# Summary

To hold the manifest.yaml and directions for uploading mermaid frontend to cloud foundry

## Build mermaid website

Note, the process for this may change, so be sure to check the mermaid GitHub directions for the latest.

1. Clone: https://github.com/mermaid-js/mermaid-live-editor
1. set MERMAID_RENDERER_URL=https://mermaid-live.apps1-fm-htz.icloud.intel.com
1. npm install
1. npm run build

The `docs` directory has the resulting build.

1. In recent builds I had to manually update this build by:
- make a `view` and `edit` directory
- move the `view.html` and `edit.html` in to the corresponding directory
- rename each to `index.html` and update the refs to use `../app` instead of `./_app`

1. copy manifset.yml from this repo in to the docs directory
1. copy Staticfile from this repo in to the docs directory

`cf push`

