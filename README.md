# Awesome-Enterprise-Cloud-Platform-Hosting

# Top Enterprise Cloud Platform & Hosting Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Hyperscale IaaS, Budget VPS & Self-Hosted Cloud Platforms*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Cloud Platform & Hosting**. These tools provide the foundational compute, storage, and networking infrastructure for running applications—covering everything from hyperscale public clouds to budget-friendly VPS providers and open-source platforms you can deploy on your own hardware.

**Examples** include AWS, Microsoft Azure, Google Cloud Platform, Oracle Cloud Infrastructure, DigitalOcean, Hetzner, OVHcloud, Alibaba Cloud, OpenStack, and Proxmox VE (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted cloud infrastructure, open-source IaaS platforms, and community-driven virtualization management—ideal for organizations seeking data sovereignty and avoiding vendor lock-in. The open-source landscape splits into **full IaaS platforms** (OpenStack, CloudStack) for building public-cloud-like environments, and **virtualization managers** (Proxmox VE) for private infrastructure without the complexity of a full cloud control plane [citation:7][citation:13].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[AWS](https://aws.amazon.com/)** | The largest public cloud provider with the broadest service catalog and deepest compliance certifications. Holds ~31% of the global cloud infrastructure market. **Highest maximum committed-use discount (69%)** but also the highest on-demand compute pricing among the big three. Egress costs are the most expensive [citation:1][citation:8]. | On-demand Linux VPS from ~$3.50–$5/month (Lightsail); EC2 from ~$0.0104/hr | **12-month free tier**: 750 hours t2.micro/t3.micro, 5 GB S3; new accounts get up to **$200 credits** (6-month validity) |
| **[Microsoft Azure](https://azure.microsoft.com/)** | Enterprise cloud with the **widest regional footprint (60+ regions)** and tightest Microsoft-stack integration. Hybrid Benefit licensing can dramatically cut costs for Windows/SQL Server workloads. Market share ~23–25% [citation:1][citation:8]. | On-demand Linux VMs from ~$0.0116/hr (B1s) | **12-month free tier**: 750 hours B1s VM, 5 GB Blob Storage; **$200 credit** for 30 days; 55+ always-free services |
| **[Google Cloud Platform](https://cloud.google.com/)** | **Lowest on-demand compute pricing among the big three** (5–10% cheaper than AWS/Azure) with automatic sustained-use discounts (no commitment required). Strongest native AI/ML tooling with TPU access. **Cheapest egress rates** [citation:1][citation:8]. | Compute Engine from ~$0.0104/hr (e2-micro); Cloud Storage from $0.020/GB/month | **$300 credit for 90 days**; always-free: 1 e2-micro VM (US regions), 5 GB Cloud Storage, 1 GB BigQuery queries/month |
| **[Oracle Cloud Infrastructure](https://www.oracle.com/cloud/)** | Enterprise cloud with the **most generous Always Free tier**. **4 Arm Ampere A1 cores + 24 GB RAM free forever**, plus 2 AMD VMs. Autonomous Database Always Free includes 20 GB storage (no backups/restore) [citation:3][citation:10]. | Pay-as-you-go beyond Always Free limits | **Always Free**: 2 AMD VMs (1/8 OCPU, 1 GB RAM each), **4 Arm A1 cores + 24 GB RAM**, 200 GB Block Volume, 20 GB Object Storage, 2 Autonomous Databases (20 GB each) [citation:3][citation:10] |
| **[DigitalOcean](https://www.digitalocean.com/)** | Developer-friendly cloud with the **most polished API and CLI (doctl)**. Simple pricing and strong documentation. Small VPS from **$6/month** (1 vCPU/1 GB); Medium from $24/month [citation:2][citation:9]. | Droplets from **$6/month** (1 GB RAM); Spaces from $5/month (250 GB) | **$200 credit for 60 days**; no permanent free tier for Droplets |
| **[Hetzner](https://www.hetzner.com/)** | **Cheapest price-per-core in the market** after its August 2026 price increase. Small VPS at **$3.79/month**, Medium (4 vCPU/8 GB) at **$7.49/month**—roughly a third of DigitalOcean's cost for comparable specs [citation:2][citation:9]. EU-first with strong GDPR posture. Only 4 region clusters; no managed database ecosystem [citation:2]. | CX22: ~**$3.79/month** (1 vCPU/2 GB); CX32: ~$7.49/month | No permanent free tier; trial via sales |
| **[OVHcloud](https://www.ovhcloud.com/)** | European cloud with strong data sovereignty positioning. **October 2026 pricing change**: local storage and public IPv4 are now **billed separately**—existing bills increase **1.4%–21.9%** depending on instance size. Compute hourly prices unchanged [citation:5][citation:12]. | VPS from ~$3.50/month; Public Cloud instances from ~$0.0087/hr | No permanent free tier; trial credits occasionally available via promotions |
| **[Alibaba Cloud](https://www.alibabacloud.com/)** | China's largest cloud with global regions and competitive Asia-Pacific pricing. **New individual users get a 300 CNY ECS trial credit valid for 3 months**—low-spec instances (2 vCPU/2 GB) can run the full 90 days. **Product new user** requirement (not just account new) [citation:4]. | ECS from ~$0.012/hr (t5-lc1m1.small); OSS from $0.018/GB/month | **300 CNY credit for 3 months** (individual new users); free tier varies by region [citation:4] |
| **[Zoho Cloud](https://www.zoho.com/)** | Application platform (not IaaS) providing customer engagement, ITSM, and CRM software. Underlying infrastructure managed by Zoho. | Freshdesk from $19/agent/month; Freshservice from $23/agent/month | Freshdesk free for 1–2 agents (6 months); Freshsales free for 3 users |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[OpenStack](https://github.com/openstack/openstack)** | [![Stars](https://img.shields.io/github/stars/openstack/openstack?style=social&color=white)](https://github.com/openstack/openstack/stargazers) | **The oldest and most battle-tested open-source IaaS platform.** Covers compute (Nova), object storage (Swift), networking (Neutron), block storage (Cinder), and identity (Keystone). Runs in production at telecoms, national research networks, and large enterprises. **Operational complexity is real**—requires a dedicated team and substantial expertise. Has its own API surface; AWS CLI/Terraform workflows do not carry over [citation:7]. **Best for large organizations with dedicated infrastructure teams** needing maximum flexibility and no AWS tooling dependency. |
| **[Apache CloudStack](https://github.com/apache/cloudstack)** | [![Stars](https://img.shields.io/github/stars/apache/cloudstack?style=social&color=white)](https://github.com/apache/cloudstack/stargazers) | **Mature IaaS platform, simpler to deploy and operate than OpenStack.** Used by several commercial cloud providers. Has its own API with partial AWS EC2 compatibility (basic instance management only). Community smaller than OpenStack's; development pace has slowed but platform is stable [citation:7]. **Best for mid-size organizations building an internal cloud** who want something more operationally accessible than OpenStack. |
| **[OpenNebula](https://github.com/OpenNebula/one)** | [![Stars](https://img.shields.io/github/stars/OpenNebula/one?style=social&color=white)](https://github.com/OpenNebula/one/stargazers) | **Lightweight IaaS for private, public, and hybrid clouds.** Apache-2.0. Manages KVM, LXC, and Firecracker workloads on a lean footprint—viable on smaller hardware clusters where OpenStack would be overkill. Simpler web interface than OpenStack's Horizon. Strong in HPC, research, and edge deployments [citation:7][citation:13]. **Best for research institutions, HPC environments, and edge deployments** needing a lightweight IaaS layer. |
| **[Proxmox VE](https://github.com/proxmox)** | [![Stars](https://img.shields.io/github/stars/proxmox?style=social&color=white)](https://github.com/proxmox/stargazers) | **Virtualization management platform (KVM + LXC), not a full IaaS cloud.** Web interface for managing VMs and containers across a cluster, with Ceph integration for shared storage. **Most common destination for VMware refugees** after Broadcom's 800–1,500% price increases. No programmatic infrastructure provisioning API like AWS/OpenStack [citation:7][citation:13]. **Best for teams replacing VMware** who manage VMs through a web interface rather than programmatically. |
| **[Ubicloud](https://github.com/ubicloud/ubicloud)** | [![Stars](https://img.shields.io/github/stars/ubicloud/ubicloud?style=social&color=white)](https://github.com/ubicloud/ubicloud/stargazers) | **Open-source managed cloud service running on Hetzner and Leaseweb hardware.** AGPL-3.0, Ruby, **12,300 GitHub stars**. Offers elastic compute, block storage, managed Postgres, Kubernetes, firewall, load balancer, and AI inference endpoints. **Pricing runs 3–10x lower than equivalent AWS services** [citation:7]. **Best for teams looking to cut cloud bills without changing their operational model significantly**—note this is a hosted service, not software you deploy on hardware you own. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Cozystack](https://github.com/aenix-io/cozystack)** | — | **Free PaaS and private cloud platform.** TCO comparison shows **5-year cost of $342,915 for 200 VMs**—saving 36% vs Proxmox VE ($533,514) and 27% vs self-managed OpenStack ($467,569) [citation:6]. **Best for organizations wanting a lower-TCO alternative** to traditional private cloud platforms. |
| **[Coolify](https://github.com/coollabsio/coolify)** | [![Stars](https://img.shields.io/github/stars/coollabsio/coolify?style=social&color=white)](https://github.com/coollabsio/coolify/stargazers) | **Self-hosted Heroku/Vercel/Netlify alternative.** Apache-2.0, **61,430 GitHub stars**. Deploy static sites, Node.js, PHP, and databases on your own VPS with Git integration and automatic SSL. ToolVitals score 98 (Excellent) [citation:14]. **Best for developers wanting PaaS-like deployment** on their own infrastructure. |

**Frameworks for building custom systems**: Choose **OpenStack** for full IaaS with broad service coverage if you have a dedicated team [citation:7], **Proxmox VE** for VMware replacement with straightforward VM management [citation:13], or **Ubicloud** for a hosted cloud service at 3–10x lower cost than AWS [citation:7]. **For budget VPS hosting**, **Hetzner** delivers the lowest price-per-core ($3.79/month for small, $7.49 for 4 vCPU/8 GB) [citation:2][citation:9], while **Oracle Cloud's Always Free tier** (4 Arm cores + 24 GB RAM forever) is unmatched for small workloads [citation:3].

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud platforms handle sensitive workloads and data; enforce least-privilege IAM policies, network segmentation, and encryption at rest and in transit.
- **Pricing models vary dramatically and hidden costs compound.** **Egress fees** are the most overlooked cost—GCP recently reduced them and is the cheapest of the big three, while AWS remains the most expensive [citation:1]. **Hetzner's low headline prices** exclude the operational trade-off of only 4 region clusters and no managed database ecosystem [citation:2]. **OVHcloud unbundled local storage and IPv4 in October 2026**, increasing existing bills by 1.4%–21.9% [citation:5][citation:12]. **Oracle's Always Free Autonomous Database has no backups or restore**—upgrade to paid for production use [citation:10]. **Alibaba's 300 CNY trial is for product new users only** (not just account new)—if you've ever opened an ECS instance, you're ineligible [citation:4]. Validate total cost of ownership including egress, support, and operational overhead before committing.

---

**Made for platform engineers, cloud architects, and organizations building infrastructure.**  
Let's make enterprise cloud platform and hosting more open, transparent, and cost-predictable.
