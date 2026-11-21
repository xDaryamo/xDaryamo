# Dario Mazza

Junior cloud and DevSecOps engineer at [Seacom](https://www.seacom.it), based in Italy. Computer science graduate from the University of Salerno.

Outside work I run a three-node Kubernetes cluster at home, and my site [dariomazza.net](https://dariomazza.net) is served from it.

## Homelab

[homelab](https://github.com/xDaryamo/homelab) is three Dell Optiplex mini PCs running K3s on Debian, with no hypervisor. Flux deploys everything from Git. Terraform and Ansible set up the Azure side and the nodes.

- Secrets live in Azure Key Vault and reach the cluster through External Secrets. No secret values in Git.
- Public services go through a Cloudflare Tunnel, so no ports are open on the router. Admin tools are reachable only from the LAN or Tailscale, some behind OAuth2 Proxy with Entra ID.
- Renovate opens dependency PRs, and CI builds every kustomization before merge.
- Longhorn volumes back up to Azure Blob Storage.

The repo README also lists what doesn't work yet: a single control plane, backups that aren't 3-2-1, and Ingress NGINX that still needs replacing.

## Other work

- **[go-puccini](https://github.com/tliron/go-puccini):** I contributed TOSCA 2.0 support to the Go version of the Puccini compiler. [PR #149](https://github.com/tliron/go-puccini/pull/149), merged.
- **ReTOSCA:** my thesis, a proof of concept for a conversion tool that turns AWS Terraform into TOSCA 2.0 models. Written in Go, with an LLM helping on the mapping.
- **[aws-cloud-solutions-portfolio](https://github.com/xDaryamo/aws-cloud-solutions-portfolio):** a small library of AWS exercises in Terraform. Each one tries out a set of services (Lambda, RDS, DynamoDB, EC2 and others) inside a realistic scenario.

## Tools

Kubernetes, Flux, Helm, Cilium, Terraform, Ansible, Docker, GitHub Actions, Prometheus, Grafana, Azure, AWS. Go, Python and Bash.

## Contact

[LinkedIn](https://linkedin.com/in/dario-mazza) · [dariomazza24@gmail.com](mailto:dariomazza24@gmail.com)
