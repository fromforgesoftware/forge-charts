# forge-charts — forge platform umbrella Helm chart

`helm install` deploys the console + selected services. `console.install` /
`console.enable` values render the `forge-apps` ConfigMap the console reads for
runtime plugin loading + `/apps`.

## Commands
- Lint: `helm lint .`
- Build deps: `helm dependency build` (subcharts are file:// to each service's `deploy/helm`)
- Install: `helm install forge . -f values.yaml`

## Boundaries
- One-line conventional commits. NEVER put real secrets in values — reference
  existing Kubernetes secrets. No dependabot.
