# LocalStack on Openshift Dev Spaces

Sample repo for running LocalStack in Redhat Openshift Dev Spaces.

## Changes made to the original repo

* add new serviceAccount `localstack-sa` with `anyuid` SCC

After deploying LocalStack, run the command below to add the `anyuid` SCC to the `localstack-sa` service account:

```bash
oc adm policy add-scc-to-user anyuid -z localstack-sa
```
