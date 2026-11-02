# Access to electricity: production

The production version of the electricity access app. Posit Connect deploys it from this repository.

- `electricity-app/`: the app, its data, and `manifest.json`, which records the R version and packages Connect installs.

To deploy it, on Connect click **Publish** > **Import from Git**, then choose branch `main` and folder `electricity-app`.

When the app starts using a new package, regenerate the manifest from the repository root and commit it with the change:

```r
rsconnect::writeManifest("electricity-app")
```
