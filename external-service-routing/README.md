# custom routing to external services

This example contains [default networking](./default-networking) for setting up shared resources, used for routing
requests to your custom domains to an external service.

In this example we want to have a domain to route to an specific folder on a GCP Bucket. For this we create 
* IngressRoute
* Middleware for adding path for no requestPath
* Middleware for adding path for wildcardRequestPath

These routes have a shared ExternalService on the default namespace.

The examples are using [Traefik Custom CRD for K8s](https://doc.traefik.io/traefik/reference/dynamic-configuration/kubernetes-crd/#definitions)

Each new routing based on the host is deployed by using [Pages Routing](./pages-routing) helm deployments to a dedicated namespace.