# k8s-helm-charts

This repo provides some Helm charts.

## Usage

NOTE! ~/.kube/config needs to be configured correctly.

``` helm install <name> ./charts/<chart_folder> ```

## Helm Repository

With the following instructions we can deploy the charts via github pages in a helm repo.

```
helm lint charts/\*
helm package charts/\*
helm repo index . --url https://amir-heinisch.de/k8s-helm-charts/
git add . && git commit -m "Update helm repo." && git push
```

To use this repo you just have to add it to your local helm client:

```
helm repo add <customName> https://amir-heinisch.de/k8s-helm-charts
```

Then simply search for charts in the repo to test it:

```
helm search repo
```
