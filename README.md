# dg-helm-repo
## Add new Charts
Create new helm chart in **main** branch under /charts with for example:
    helm create app-name
Push this to main branch and **Release** action is running to create a package and updating index.yaml file.

See [Helm chart releaser documentation](https://helm.sh/docs/howto/chart_releaser_action/) for more info.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add <alias> https://dennisvg.github.io/dg-helm-repo/

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  
You can then run `helm search repo <alias>` to see the charts.

To install the <chart-name> chart:

    helm install my-<chart-name> <alias>/<chart-name>

To uninstall the chart:

    helm delete my-<chart-name>
