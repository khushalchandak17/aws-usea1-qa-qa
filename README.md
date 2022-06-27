# PROVIDER-REGION-ENVIRONMENT-TEAM

## Customize repository

You can follow the full instructions on the [operational manual](https://gitlab.industrysoftware.automation.siemens.com/caas-ops/operational-manual.git), or alternatively you can run these commands in the repository's root directory:

```bash
export REPO_NAME=$(basename `git rev-parse --show-toplevel`)
sed -i "s/PROVIDER-REGION-ENVIRONMENT-TEAM/$REPO_NAME/g" .chglog/config.yml Chart.yaml deploy.yaml

export TEAM='shared'
echo "defaultNamespace: fleet-$TEAM" > fleet.yaml
```