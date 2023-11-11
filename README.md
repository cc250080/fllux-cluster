# flux-cluster
Welcome to my highly opinionated Repo for my GitOps home-lab. In this repo I install a basic Vanilla [Kubernetes](https://kubernetes.io/docs/home/) and I use [Flux](https://fluxcd.io/flux/) to manage its state.

## 👋 Introduction
My personal Goal with this project is to have an easy and elegant way to manage applications that I want to run in my kubernetes home-lab while at the same time use it to keep learning the intrinsicacies of Kubernetes. That is why I took some choices like for example installing Vanilla Kubernetes by hand. It is my goal to take out any abstraction on top of the basic Kubernetes components while at the same time enjoying a useful GitOps installation.

## ✨ Features

- Documented **manual** Installation of Kubernetes v1.28 mono-node cluster in Debian 12 *BookWorm*
- Opinionated implementation of Flux with [strong community support](https://github.com/onedr0p/flux-cluster-template#-support)
- Encrypted secrets thanks to [SOPS](https://github.com/getsops/sops) and [Age](https://github.com/FiloSottile/age)
- Web application firewall thanks to [Cloudflare Tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps)
- SSL certificates thanks to [Cloudflare](https://cloudflare.com) and [cert-manager](https://cert-manager.io)
- Next-gen networking thanks to [Cilium](https://cilium.io/)
- A [Renovate](https://www.mend.io/renovate)-ready repository
- Integrated [GitHub Actions](https://github.com/features/actions)

... and more!

## 📝 Pre-start checklist

Before we get started everything below must be taken into consideration, you must...

- [ ] bring a **positive attitude** and be ready to learn and fail a lot. _The more you fail, the more you can learn from._
- [ ] run the cluster on bare metal machines or VMs within your home network &mdash; **this is NOT designed for cloud environments**.
- [ ] have Debian 12 freshly installed on 1 or more AMD64/ARM64 bare metal machines or VMs. Each machine will be either a **control node** or a **worker node** in your cluster.
- [ ] give your nodes unrestricted internet access &mdash; **air-gapped environments won't work**.
- [ ] have a domain you can manage on Cloudflare.
- [ ] be willing to commit encrypted secrets to a public GitHub repository.
- [ ] have a DNS server that supports split DNS (e.g. Pi-Hole) deployed somewhere outside your cluster **ON** your home network.
