# forge-charts

Umbrella Helm chart for the forge platform. `helm install` deploys the console +
selected services; the `console.install`/`console.enable` values render the
`forge-apps` ConfigMap the console reads for runtime plugin loading + `/apps`.

```sh
helm dependency build
helm install forge . -f values.yaml
```

Subcharts are sourced from each service repo's `deploy/helm` (file:// deps for
local dev; switch to a chart registry for published installs).
