Deploy a security and compliance system
When you deploy an image you may also deploy a security threat, and images can become quickly insecure as new threats are discovered and disclosed. To continuously monitor and detect threats, you can deploy a tool like Falco.

Create a Kubernetes cluster.
Go to Create > Kubernetes
Select a k8s version.
Choose a datacenter region.
Cluster capacity default is fine for this.


Two ways to connect to your cluster -> doctl or manual with kubectl file. I chose kubectl file as I manage multiple k8s clusters with kctx.

Skip auto install apps - we're doing it ourselves!

We're going to install Falco using the official Helm charts: https://github.com/falcosecurity/charts/tree/master/falco

---Descr its not the best way

helm install falco --set falcosidekick.enabled=true falcosecurity/falco 