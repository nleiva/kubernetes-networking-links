<p align="center">
  <img width="512" height="91" title="Kubernetes Logo" src="static/Kubernetes_logo.svg"><br>
  <b>Networking Links</b><br>
</p>

---

Kubernetes Networking recommended reading list.

## Linux Networking
- [Linux Networking Explained](https://events.static.linuxfound.org/sites/events/files/slides/2016%20-%20Linux%20Networking%20explained_0.pdf) by [tgraf](https://github.com/tgraf)
- [An In-Depth Guide to iptables, the Linux Firewall](https://www.booleanworld.com/depth-guide-iptables-linux-firewall/) by [supriyo-biswas](https://github.com/supriyo-biswas)
- Monitoring and Tuning the Linux Networking Stack:
  - [Receiving Data](https://blog.packagecloud.io/eng/2016/06/22/monitoring-tuning-linux-networking-stack-receiving-data/)
  - [Sending Data](https://blog.packagecloud.io/eng/2017/02/06/monitoring-tuning-linux-networking-stack-sending-data/)

### Linux Namespaces
- [Introducing Linux Network Namespaces](https://blog.scottlowe.org/2013/09/04/introducing-linux-network-namespaces/) by [scottslowe](https://github.com/scottslowe)
- [Making sense Of Linux namespaces](https://prefetch.net/blog/2018/02/22/making-sense-of-linux-namespaces/) by [Matty9191](https://github.com/Matty9191)
- [Namespaces in operation](https://lwn.net/Articles/531114/) by [mkerrisk](https://github.com/mkerrisk)
- [Containers from Scratch](https://speakerdeck.com/ericchiang/coreos-fest-2017-containers-from-scratch), [recording](https://www.youtube.com/watch?v=wyqoi52k5jM) by [ericchiang](https://github.com/ericchiang)
- Containers from scratch: The sequel, [recording](https://www.youtube.com/watch?v=_TsSmSu57Zo) by [lizrice](https://github.com/lizrice)
- [Linux Namespaces](https://medium.com/@teddyking/linux-namespaces-850489d3ccf) by [teddyking](https://github.com/teddyking)
- [Namespaces, Threads, and Go](https://github.com/containernetworking/plugins/tree/master/pkg/ns) by [squeed](https://github.com/squeed)
  - [Linux Namespaces and Go Don't Mix](https://www.weave.works/blog/linux-namespaces-and-go-don-t-mix) by [brb](https://github.com/brb)

## Kubernetes Networking
- [The Almighty Pause Container](https://www.ianlewis.org/en/almighty-pause-container) by [ianlewis](https://github.com/ianlewis)
- There is No Such Thing as Container Networking, [recording](https://www.youtube.com/watch?v=t98CX8Tberc) by [kelseyhightower](https://github.com/kelseyhightower)
- [Kubernetes Networking: Behind the scenes](https://medium.com/@nleiva/kubernetes-networking-behind-the-scenes-39a1ab1792bb) by [nleiva](https://github.com/nleiva)
- [Kubernetes Container Networking (Cisco Live 2018)](https://clnv.s3.amazonaws.com/2018/eur/pdf/BRKDCN-2390.pdf)
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
- [Operating a Kubernetes network](https://jvns.ca/blog/2017/10/10/operating-a-kubernetes-network/) by [jvns](https://github.com/jvns)
- [Understanding the Kubernetes Networking Model](https://sookocheff.com/post/kubernetes/understanding-kubernetes-networking-model/) by [soofaloofa](https://github.com/soofaloofa)
- [Kubernetes Networking Master Class](https://rancher.com/events/2018/kubernetes-networking-masterclass-june-online-meetup/)

### IPVS
- [IPVS-Based In-Cluster Load Balancing Deep Dive](https://kubernetes.io/blog/2018/07/09/ipvs-based-in-cluster-load-balancing-deep-dive/)

### eBPF
- [eBPF, Microservices, Docker, and Cilium: From Novice to Seasoned](http://www.adelzaalouk.me/2017/security-bpf-docker-cillium/) by [zanetworker](https://github.com/zanetworker)
- [Why is the kernel community replacing iptables with BPF?](https://cilium.io/blog/2018/04/17/why-is-the-kernel-community-replacing-iptables/) by [cilium](https://github.com/cilium)
- [Using eBPF in Kubernetes](https://kubernetes.io/blog/2017/12/using-ebpf-in-kubernetes/)
- [BPF and XDP Reference Guide](https://cilium.readthedocs.io/en/v1.1/bpf/) by [cilium](https://github.com/cilium)

## CNI
- [Container Network Interface Specification](https://github.com/containernetworking/cni/blob/master/SPEC.md)
- [Understanding CNI (Container Networking Interface)](https://www.dasblinkenlichten.com/understanding-cni-container-networking-interface/)
- CNI, the Container Network Interface, [recording](https://skillsmatter.com/skillscasts/10811-cni-the-container-network-interface) by [bboreham](https://github.com/bboreham)
- The Container Network Interface (CNI), [recording](https://www.youtube.com/watch?v=_-9kItVUUCw) by [eyakubovich](https://github.com/eyakubovich)
- KubeCon "Container Network Interface: Network Plugins", [recording](https://www.youtube.com/watch?v=-DB1nxrUwbA) by [eyakubovich](https://github.com/eyakubovich)
- [Kubernetes and the CNI Where We Are and What's Next](https://github.com/sbueringer/kubecon-slides/blob/master/slides/2018-kubecon-eu/Kubernetes%20and%20the%20CNI%20Where%20We%20Are%20and%20What's%20Next%20-%20Casey%20Callendrello%2C%20CoreOS%20(Intermediate%20Skill%20Level)%20-%20Kubernetes-and-the-CNI-Kubecon-218.pdf), [recording](https://www.youtube.com/watch?v=Vn6KYkNevBQ) by [squeed](https://github.com/squeed)
- [Comparative Kubernetes networks solutions](https://www.objectif-libre.com/en/blog/2018/07/05/k8s-network-solutions-comparison/)
- [Comparison of Networking Solutions for Kubernetes](http://machinezone.github.io/research/networking-solutions-for-kubernetes/)

## DNS
- [5 – 15s DNS lookups on Kubernetes?](https://blog.quentin-machu.fr/2018/06/24/5-15s-dns-lookups-on-kubernetes/) by [Quentin-M](https://github.com/Quentin-M)

## Routing
- [Kubernetes Traffic Engineering with BGP](https://www.asykim.com/blog/kubernetes-traffic-engineering-with-bgp) by [andrewsykim](https://github.com/andrewsykim)

## Service Mesh

- The Service Mesh: Past, Present, and Future, [recording](https://www.youtube.com/watch?v=2trOvMUuLkk) by [wmorgan](https://github.com/wmorgan)
