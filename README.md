<p align="center">
  <img width="512" height="91" title="Kubernetes Logo" src="static/Kubernetes_logo.svg"><br>
  <b>Networking Links</b><br>
</p>

---

Kubernetes Networking recommended reading list.

## Linux Networking
- [Linux Kernel Networking Walkthrough](https://www.slideshare.net/ThomasGraf5/linuxcon-2015-linux-kernel-networking-walkthrough): Getting packets from/to the NIC, Packet processing (TCP/IP Processing, Queuing from/to userspace (Socket Buffers, Flow Control) by [tgraf](https://github.com/tgraf)
- [Linux Networking Explained](https://events.static.linuxfound.org/sites/events/files/slides/2016%20-%20Linux%20Networking%20explained_0.pdf): Network devices, Namespaces, Routing, Veth, VLAN, IPVLAN, MACVLAN, MACVTAP, Bonding, Team, OVS, Bridge, BPF, IPSec by [tgraf](https://github.com/tgraf)
- Monitoring and Tuning the Linux Networking Stack:
  - [Receiving Data](https://blog.packagecloud.io/eng/2016/06/22/monitoring-tuning-linux-networking-stack-receiving-data/)
  - [Sending Data](https://blog.packagecloud.io/eng/2017/02/06/monitoring-tuning-linux-networking-stack-sending-data/)
### Netfilter 
- [An In-Depth Guide to iptables, the Linux Firewall](https://www.booleanworld.com/depth-guide-iptables-linux-firewall/) by [supriyo-biswas](https://github.com/supriyo-biswas)
- [Benchmarking nftables](https://developers.redhat.com/blog/2017/04/11/benchmarking-nftables): Regarding scalability, `ipset` is a blessing to any `iptables` set up. `Nftables` follow the path with their native implementation of sets and take the concept to a higher level by extending the list of supported data types and allowing it to be used in further applications using (verdict) maps.
- [Nftables ruleset debug/tracing](https://wiki.nftables.org/wiki-nftables/index.php/Ruleset_debug/tracing): This is an equivalent of the old iptables method -J TRACE, but with some great improvements.
- - [kube-proxy nftables and iptables vs a Service with 100k endpoints](https://gist.github.com/aojea/f9ca1a51e2afd03621744c95bfdab5b8): Iptables performance is limited mainly by two reasons; Latency on the first packet of a connection caused by the linear search rule matching, Latency on the programming latency caused by the need to save and restore all the lines to the kernel in each transaction. The kernel community moved to `nftables` as replacement of `iptables`, with the goal of removing the existing performance bottlenecks by [Antonio Ojea](https://github.com/aojea)
- [Iptables the end of an era](https://www.youtube.com/watch?v=h7Y2eaBwCqc): Kubernetes has decided to implement a new nftables proxy by [Antonio Ojea](https://github.com/aojea)
- [Add an nftables-based kube-proxy backend](https://github.com/kubernetes/enhancements/tree/master/keps/sig-network/3866-nftables-proxy): The default kube-proxy implementation on Linux is currently based on iptables. IPTables was the preferred packet filtering and processing system in the Linux kernel for many years (starting with the 2.4 kernel in 2001). However, problems with iptables led to the development of a successor, nftables, first made available in the 3.13 kernel in 2014, and growing increasingly featureful and usable as a replacement for iptables since then. Development on iptables has mostly stopped, with new features and performance improvements primarily going into nftables instead by [Dan Winship](https://github.com/danwinship).
### Sockets
- [High-Speed Packet Transmission in Go: From net.Dial to AF_XDP](https://toonk.io/sending-network-packets-in-go/index.html): Sending as many packets per second from a Linux machine by [Andree Toonk](https://github.com/atoonk)

### Linux Namespaces
- [Introducing Linux Network Namespaces](https://blog.scottlowe.org/2013/09/04/introducing-linux-network-namespaces/) by [scottslowe](https://github.com/scottslowe)
- [Making sense Of Linux namespaces](https://prefetch.net/blog/2018/02/22/making-sense-of-linux-namespaces/) by [Matty9191](https://github.com/Matty9191)
- [A deep dive into Linux namespaces](http://ifeanyi.co/posts/linux-namespaces-part-1/) by [iffyio](https://github.com/iffyio)
- [Namespaces in operation](https://lwn.net/Articles/531114/) by [mkerrisk](https://github.com/mkerrisk)
- [Containers from Scratch](https://speakerdeck.com/ericchiang/coreos-fest-2017-containers-from-scratch), [recording](https://www.youtube.com/watch?v=wyqoi52k5jM) by [ericchiang](https://github.com/ericchiang)
- Containers from scratch: The sequel, [recording](https://www.youtube.com/watch?v=_TsSmSu57Zo) by [lizrice](https://github.com/lizrice)
- [Linux Namespaces](https://medium.com/@teddyking/linux-namespaces-850489d3ccf) by [teddyking](https://github.com/teddyking)
- [Namespaces, Threads, and Go](https://github.com/containernetworking/plugins/tree/master/pkg/ns) by [squeed](https://github.com/squeed)
  - [Linux Namespaces and Go Don't Mix](https://www.weave.works/blog/linux-namespaces-and-go-don-t-mix) by [brb](https://github.com/brb)
- [Network Namespaces Basics Explained in 15 Minutes](https://www.youtube.com/watch?v=j_UUnlVC2Ss) by [Mumshad Mannambeth](https://github.com/mmumshad)

## Kubernetes Networking
- [The Almighty Pause Container](https://www.ianlewis.org/en/almighty-pause-container) by [ianlewis](https://github.com/ianlewis)
- There is No Such Thing as Container Networking, [recording](https://www.youtube.com/watch?v=t98CX8Tberc) by [kelseyhightower](https://github.com/kelseyhightower)
- [Kubernetes Networking: Behind the scenes](https://medium.com/@nleiva/kubernetes-networking-behind-the-scenes-39a1ab1792bb) by [nleiva](https://github.com/nleiva)
- [Kubernetes 101: Kubernetes Networking](https://dominik-tornow.medium.com/kubernetes-networking-22ea81af44d0)
- [The Kubernetes Networking Guide](https://k8s.networkop.co.uk/) by [Michael Kashin](https://github.com/networkop)
- [Kubernetes Networking Demystified: A Brief Guide](https://www.cncf.io/blog/2020/01/30/kubernetes-networking-demystified-a-brief-guide/)
- [Tracing the path of network traffic in Kubernetes](https://learnk8s.io/kubernetes-network-packets) by [Kristijan](https://github.com/k-mitevski)
- [Understanding kubernetes networking: pods](https://medium.com/google-cloud/understanding-kubernetes-networking-pods-7117dd28727) by [Markbnj](https://github.com/Markbnj)
- [An illustrated guide to Kubernetes Networking [Part 1]](https://medium.com/@ApsOps/an-illustrated-guide-to-kubernetes-networking-part-1-d1ede3322727) by [ApsOps](https://github.com/ApsOps)
- [A Hacker’s Guide to Kubernetes Networking](https://thenewstack.io/hackers-guide-kubernetes-networking/) by [yaronha](https://github.com/yaronha)
- [Kubernetes Cluster Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/)
- [Why Kubernetes doesn’t use libnetwork](https://kubernetes.io/blog/2016/01/why-kubernetes-doesnt-use-libnetwork/) by [thockin](https://github.com/thockin)
- [Understanding kubernetes networking: services](https://medium.com/google-cloud/understanding-kubernetes-networking-services-f0cb48e4cc82) by [Markbnj](https://github.com/Markbnj)
- [Kubernetes Networking](https://cloudnativelabs.github.io/post/2017-04-18-kubernetes-networking/) by [cloudnativelabs](https://github.com/cloudnativelabs)
- [Understand and Troubleshoot the “Magic” of k8s Networking](https://kccnceu18.sched.com/event/Dquy/blackholes-and-wormholes-understand-and-troubleshoot-the-magic-of-kubernetes-networking-minhan-xia-rohit-ramkumar-google-intermediate-skill-level-slides-attached), [recording](https://www.youtube.com/watch?v=knIJEzTd3kc) by [rramkumar1](https://github.com/rramkumar1) and [freehan](https://github.com/freehan)
- [An Illustrated Guide to Kubernetes Networking](https://speakerd.s3.amazonaws.com/presentations/005d36f0113d4773be8866496142485e/Illustrated_guid_to_kubernetes_networking.pdf) by [thockin](https://github.com/thockin)
- [The ins and outs of networking in Google Container Engine and Kubernetes](https://speakerdeck.com/thockin/the-ins-and-outs-of-networking-in-google-container-engine), [recording](https://www.youtube.com/watch?v=y2bhV81MfKQ) by [thockin](https://github.com/thockin) and [matchstick](https://github.com/matchstick)
- Introduction to Kubernetes Networking, [recording](https://www.youtube.com/watch?v=7OFw3lgSb1Q) by [bboreham](https://github.com/bboreham)
- [Life of a Packet](https://github.com/sbueringer/kubecon-slides/blob/master/slides/2017-kubecon-eu/Life%20of%20a%20Packet%20%5BI%5D%20-%20Michael%20Rubin%2C%20Google%20-%20KubeCon%20EU%20'17-%20Life%20of%20a%20Packet.pdf), [recording](https://www.youtube.com/watch?v=0Omvgd7Hg1I) by [matchstick](https://github.com/matchstick)
- [Google Kubernetes Engine networking](https://cloud.google.com/kubernetes-engine/docs/concepts/network-overview)
- [Operating a Kubernetes network](https://jvns.ca/blog/2017/10/10/operating-a-kubernetes-network/) by [jvns](https://github.com/jvns)
- [Understanding the Kubernetes Networking Model](https://sookocheff.com/post/kubernetes/understanding-kubernetes-networking-model/) by [soofaloofa](https://github.com/soofaloofa)
- [Kubernetes Networking Master Class](https://rancher.com/events/2018/kubernetes-networking-masterclass-june-online-meetup/)
- [Kubernetes and Networks - why is this so dang hard?](https://speakerdeck.com/thockin/kubernetes-and-networks-why-is-this-so-dang-hard) by [thockin](https://github.com/thockin)
- [Bringing Traffic Into Your Kubernetes Cluster](https://speakerdeck.com/thockin/bringing-traffic-into-your-kubernetes-cluster) by [thockin](https://github.com/thockin)
- [Deconstructing Kubernetes Networking](https://eevans.co/blog/deconstructing-kubernetes-networking/)
- [Certified Calico Operator: Level 1](https://academy.tigera.io/course/certified-calico-operator-level-1/)
- [Networking and Kubernetes: A Layered Approach](https://learning.oreilly.com/library/view/kubernetes-networking/9781492081647/) by [strongjz](https://twitter.com/strongjz) and [Vallery Lancey](https://twitter.com/vllry)
- [Let's talk about Kubernetes on the Internet](https://raesene.github.io/blog/2022/07/03/lets-talk-about-kubernetes-on-the-internet/): Talks about exposed Kubernetes clusters on the Internet by [Rory McCune](https://github.com/raesene)
- [Kubernetes Networking Explained – Guide for Beginners](https://spacelift.io/blog/kubernetes-networking)
- [How Container Networking Works: a Docker Bridge Network From Scratch](https://labs.iximiuz.com/tutorials/container-networking-from-scratch): Learn how to virtualize network environments, connect multiple Linux containers using veth pairs and Linux bridge devices, and even tried to configure IP routing and NAT to enable connectivity between the containers and the outside world by [Ivan Velichko](https://github.com/iximiuz)

### IPVS
- [IPVS-Based In-Cluster Load Balancing Deep Dive](https://kubernetes.io/blog/2018/07/09/ipvs-based-in-cluster-load-balancing-deep-dive/)

### eBPF
- [eBPF, Microservices, Docker, and Cilium: From Novice to Seasoned](http://www.adelzaalouk.me/2017/security-bpf-docker-cillium/) by [zanetworker](https://github.com/zanetworker)
- [Why is the kernel community replacing iptables with BPF?](https://cilium.io/blog/2018/04/17/why-is-the-kernel-community-replacing-iptables/) by [cilium](https://github.com/cilium)
- [Using eBPF in Kubernetes](https://kubernetes.io/blog/2017/12/using-ebpf-in-kubernetes/)
- [BPF and XDP Reference Guide](https://cilium.readthedocs.io/en/v1.1/bpf/) by [cilium](https://github.com/cilium)
- [pwru (packet, where are you?)](https://github.com/cilium/pwru)
- [Dive into BPF: a list of reading material](https://qmonnet.github.io/whirl-offload/2016/09/01/dive-into-bpf/)
- [The eXpress Data Path](https://blogs.igalia.com/dpino/2019/01/10/the-express-data-path/): Review of the eXpress Data Path, the new kernel component for fast packet processing.

### IPv6
- [IPv4/IPv6 dual-stack](https://kubernetes.io/docs/concepts/services-networking/dual-stack/)
- [Dual-stack Kubernetes with kubeadm-dind-cluster](http://blog.michali.net/2018/11/08/dual-stack-kubernetes-with-kubeadm-dind-cluster/) by [pmichali](https://github.com/pmichali)
- [kube-v6](https://github.com/leblancd/kube-v6) by [leblancd](https://github.com/leblancd)
- [Kubernetes in IPv6 only](https://opsnotice.xyz/kubernetes-ipv6-only/) by [valentin2105](https://github.com/valentin2105)
- [Add IPv4/IPv6 dual stack KEP](https://github.com/kubernetes/enhancements/pull/648)
* [How to run an IPv6 conformance cluster in AWS using kubeadm](https://github.com/aojea/k8s-aws-ipv6) by [aojea](https://github.com/aojea)

### Multi-cluster
- [Kubernetes multi-cluster networking made simple](https://medium.com/@nleiva/kubernetes-multi-cluster-networking-made-simple-c8f26827813) by [nleiva](https://github.com/nleiva)

## CNI
- [Container Network Interface Specification](https://github.com/containernetworking/cni/blob/master/SPEC.md)
- [Container Network Interface and Go](https://www.youtube.com/watch?v=0SXPsLvB0UI)
- [Understanding CNI (Container Networking Interface)](https://www.dasblinkenlichten.com/understanding-cni-container-networking-interface/)
- CNI, the Container Network Interface, [recording](https://skillsmatter.com/skillscasts/10811-cni-the-container-network-interface) by [bboreham](https://github.com/bboreham)
- The Container Network Interface (CNI), [recording](https://www.youtube.com/watch?v=_-9kItVUUCw) by [eyakubovich](https://github.com/eyakubovich)
- KubeCon "Container Network Interface: Network Plugins", [recording](https://www.youtube.com/watch?v=-DB1nxrUwbA) by [eyakubovich](https://github.com/eyakubovich)
- [Kubernetes and the CNI Where We Are and What's Next](https://github.com/sbueringer/kubecon-slides/blob/master/slides/2018-kubecon-eu/Kubernetes%20and%20the%20CNI%20Where%20We%20Are%20and%20What's%20Next%20-%20Casey%20Callendrello%2C%20CoreOS%20(Intermediate%20Skill%20Level)%20-%20Kubernetes-and-the-CNI-Kubecon-218.pdf), [recording](https://www.youtube.com/watch?v=Vn6KYkNevBQ) by [squeed](https://github.com/squeed)
- [Comparative Kubernetes networks solutions](https://www.objectif-libre.com/en/blog/2018/07/05/k8s-network-solutions-comparison/)
- [Comparison of Networking Solutions for Kubernetes](http://machinezone.github.io/research/networking-solutions-for-kubernetes/)
- [Comparative Kubernetes networks solutions](https://www.objectif-libre.com/en/blog/2018/07/05/k8s-network-solutions-comparison/)
- [Benchmark results of Kubernetes network plugins (CNI) over 10Gbit/s network](https://itnext.io/benchmark-results-of-kubernetes-network-plugins-cni-over-10gbit-s-network-36475925a560)
- [Large-scale network simulations in Kubernetes, Part 1 - Building a CNI plugin](https://networkop.co.uk/post/2018-11-k8s-topo-p1/)
- [Large-scale network simulations in Kubernetes, Part 2 - Network topology](https://networkop.co.uk/post/2018-11-k8s-topo-p2/)
- [How to Write Your Own CNI Plug-in with Bash](https://www.altoros.com/blog/kubernetes-networking-writing-your-own-simple-cni-plug-in-with-bash/)

### Calico
- [Calico for Kubernetes networking: the basics & examples](https://medium.com/flant-com/calico-for-kubernetes-networking-792b41e19d69)

## Ingress
- [Kubernetes Ingress for Beginners](https://thenewstack.io/kubernetes-ingress-for-beginners/)
- [Kubernetes Ingress with NGINX Ingress Controller Example](https://kubernetes.github.io/ingress-nginx/): Explores the Ingress object in Kubernetes (K8s). Step-by-step walk through setting up an NGINX Ingress controller with Azure Kubernetes Service (AKS).

## Network Solutions Details

## DNS
- [An Introduction to the Kubernetes DNS Service](https://www.digitalocean.com/community/tutorials/an-introduction-to-the-kubernetes-dns-service)
- [5 – 15s DNS lookups on Kubernetes?](https://blog.quentin-machu.fr/2018/06/24/5-15s-dns-lookups-on-kubernetes/) by [Quentin-M](https://github.com/Quentin-M)
- [Debugging and Monitoring DNS issues in Kubernetes](https://cilium.io/blog/2019/12/18/how-to-debug-dns-issues-in-k8s/)
- [Kubernetes DNS at scale](https://gist.github.com/aojea/32aeaa86aacebcdd93596ecb70fcba4f): Environments may operate at large scales (+10k nodes) and it seems that the DNS protocol has some limitations, mainly the number of records that fit into a DNS answer by [Antonio Ojea](https://github.com/aojea)

## Routing
- [Kubernetes Traffic Engineering with BGP](https://www.asykim.com/blog/kubernetes-traffic-engineering-with-bgp) by [andrewsykim](https://github.com/andrewsykim)

## Service Mesh

- The Service Mesh: Past, Present, and Future, [recording](https://www.youtube.com/watch?v=2trOvMUuLkk) by [wmorgan](https://github.com/wmorgan)
- [Using Istio Multicluster to "Burst" Workloads Between Clusters](https://codelabs.developers.google.com/codelabs/istio-multi-burst/#0)
