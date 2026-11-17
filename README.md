# RDP VPS: What RackNerd's Six Windows Plans Cost, How Many People Can Share One Server, and What the Windows Licence Adds (Full Price Table)

RackNerd's Windows VPS line starts at **$27.59 a month** for one AMD Ryzen core, 2 GB of RAM, 35 GB of NVMe storage and 2 TB of monthly transfer, with Remote Desktop enabled, full administrator access and one dedicated IPv4 address. These are monthly prices, and every plan in the line is a Windows machine you sign into over RDP. Which one you need depends more on headcount than on core count. Two people can share any of these plans at no extra cost. A third simultaneous user changes the licensing picture completely, and that is the part most "rdp vps" pages skip.

## The short answer

> Most buyers should take **Windows VPS 4GB at $30.59/month**: 2 Ryzen cores, 4 GB RAM, 60 GB NVMe, 2 TB transfer. It costs $3 more than the entry plan and doubles both cores and memory. Stay on the 2 GB plan only if you are one person running a browser, Office and a single line-of-business app. If three or more people need to be signed in at the same time, read the licensing section below before you order anything.
>
> 👉 Check RackNerd's current Windows VPS and RDP plan prices

## RackNerd Windows VPS plans and prices

All six plans run on AMD Ryzen cores with NVMe storage and are listed in Los Angeles.

| Plan | CPU / RAM | NVMe storage | Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Windows VPS 2GB | 1 Ryzen core / 2 GB | 35 GB | 2 TB | $27.59/mo | [ Order 2GB](https://bit.ly/RacKnerd) |
| Windows VPS 4GB | 2 Ryzen cores / 4 GB | 60 GB | 2 TB | $30.59/mo | [ Order 4GB](https://bit.ly/RacKnerd) |
| Windows VPS 6GB | 2 Ryzen cores / 6 GB | 85 GB | 3 TB | $35.59/mo | [ Order 6GB](https://bit.ly/RacKnerd) |
| Windows VPS 8GB | 3 Ryzen cores / 8 GB | 110 GB | 5 TB | $44.59/mo | [ Order 8GB](https://bit.ly/RacKnerd) |
| Windows VPS 12GB | 4 Ryzen cores / 12 GB | 160 GB | 6 TB | $64.59/mo | [ Order 12GB](https://bit.ly/RacKnerd) |
| Windows VPS 16GB | 6 Ryzen cores / 16 GB | 200 GB | 10 TB | $89.59/mo | [ Order 16GB](https://bit.ly/RacKnerd) |

Every plan includes RDP access, full administrator rights, one dedicated IPv4, a 1 Gbps public port, and the ctrl control panel for reboots, OS reinstalls, rDNS, firewall rules and an HTML5 VNC console. The servers are unmanaged: you create accounts, install software and run Windows Update yourself. Support is listed as 24/7.

RackNerd also sells cheaper KVM VPS specials, but the order form on those offers Linux distributions (CentOS, Rocky Linux, AlmaLinux, Fedora, Debian, Ubuntu), with custom ISO installs handled by support ticket. For a machine you log into over Remote Desktop, the Windows VPS plans above are the ones to look at.

## What the monthly price covers, and where the licence question hides

The RackNerd listings present one flat monthly number for a Windows machine and don't itemise a per-core Windows charge. Other hosts do the opposite, and that difference is worth more than a few dollars of sticker price. MassiveGRID advertises RDP VPS from $3.99/month, but its quotes are built on a 180-day Windows Server evaluation, and a real licence is billed at $6.31 per vCPU per month on top. Its 2 vCPU / 4 GB / 64 GB configuration at $9.58 becomes roughly $22/month once Windows is licensed, against $30.59 for RackNerd's 4 GB plan.

Read that comparison in both directions. If you are comfortable adding a licence line and keeping an eye on an evaluation clock, the cheaper route exists. If you want one number, no expiry date and no per-core maths, RackNerd's flat price is the easier buy. What matters is that you are comparing the same thing.

An expired evaluation is not a cosmetic problem. When the 180 days run out the installation needs licensing, and the machine you were using as a desktop stops being usable until it is sorted.

Before you pay, ask whether the Windows image is a licensed install or an evaluation. That single answer moves the real monthly cost more than any plan upgrade on this page.

## How many people can be logged in at once

Windows Server allows two administrative sessions at the same time. Two people can each have their own desktop on any RackNerd Windows plan, and that concurrency costs nothing extra.

The third user is where the budget moves. From three concurrent sessions you need the Remote Desktop Services role installed and RDS client access licences, which Windows Server does not include. Providers that sell this as a product price it per seat: MassiveGRID charges $8.90 per extra user per month on top of the server. RackNerd's plan listings don't itemise an RDS add-on, so if you need three or more seats, put the question to pre-sales rather than assuming a bigger plan covers it.

Desktop Windows behaves differently again. Windows 10 and 11 permit one interactive session, so a two-person team on desktop Windows isn't possible regardless of how much RAM you buy. Hosting companies also can't resell desktop Windows licences, which is why providers offering Windows 10/11 images sell them on your own key.

A five-person office therefore isn't a bigger version of the same purchase. It's RDS CALs per user plus a machine sized for the sessions, and the sizing guidance one host publishes is 2 GB of RAM per user plus 2 GB for Windows itself. Five users lands at 12 GB, which is RackNerd's $64.59 plan.

## Picking a size for your workload

RackNerd doesn't map plans to workloads, so here are thresholds drawn from the sizing guidance MassiveGRID publishes for the same job, matched to RackNerd's tiers.

- **One or two people on email, documents and browsing:** 4 GB. That's the $30.59 plan. The 2 GB entry plan boots Windows and a browser but leaves very little headroom, and $3 is a small price to stop thinking about RAM.
- **Multitasking, several apps open, spreadsheets, video calls:** 6 GB at $35.59.
- **Data analysis, design tools, large databases:** 8 GB and up. The 8 GB plan at $44.59, 12 GB at $64.59 and 16 GB at $89.59 sit in this bracket.
- **Three to eight people on Remote Desktop Services:** start at 12 GB and count 2 GB per user plus 2 GB of system overhead.

Treat these as vendor guidance, not a spec sheet. A single app with a large dataset can want more memory than five people typing in Word.

👉 Compare RackNerd's Windows VPS plans at current prices

## Getting in, and locking the door behind you

Microsoft has replaced its Remote Desktop apps with a client called Windows App, which is what you install on macOS, iOS, Android and Linux. Windows still ships Remote Desktop Connection (mstsc) built in, so a Windows laptop needs nothing extra.

Four things are worth doing on first login: leave Network Level Authentication enabled, set an account lockout policy, move RDP off port 3389 or put it behind a VPN, and leave Windows Update on. An RDP port exposed to the open internet collects password-guessing traffic within hours, and a default administrator password on 3389 is the most common way these servers get taken over.

The recovery path matters as much as the hardening. If a firewall rule locks RDP out, ctrl's HTML5 VNC console gets you back into the machine without waiting on a ticket.

Latency decides how the desktop feels more than the CPU does. Sessions under roughly 50 ms feel local, and above that typing and window dragging start to lag. RackNerd's Windows plans list Los Angeles, which is comfortable from North America and a long haul from Europe or Asia. Run a ping to a Los Angeles host from where you'll actually sit before you commit to a monthly plan.

## RDP VPS or a per-user managed desktop?

Windows 365 and Azure Virtual Desktop sell a managed desktop per user per month and require a Microsoft 365 subscription. An RDP VPS is the other trade: you hold the administrator account and pay for resources instead of seats.

|  | RDP VPS (RackNerd) | Windows 365 / AVD |
| --- | --- | --- |
| Billing basis | Per server, by CPU, RAM and storage | Per user, per month |
| Prerequisite | None beyond the plan | Microsoft 365 subscription |
| Who administers it | You | Microsoft or a partner |
| Multiple users | 2 admin sessions free, more via RDS CALs | Built around per-user assignment |

Other price anchors, all from the providers' own pages: MassiveGRID from $3.99/month with its 2 vCPU / 4 GB configuration at $9.58 before licensing, LightNode from $7.71/month or $0.012/hour with hourly billing, and RDP.NET advertising setup in under five minutes with 99% uptime and servers in Los Angeles, Chicago, London and Amsterdam. Each of those needs the licence question settled before you can compare it fairly with a RackNerd plan.

## Which plan to buy

- **One person, a few Windows-only apps:** 4 GB at $30.59. Take the 2 GB at $27.59 only if the workload really is light.
- **Two people sharing a desktop:** 4 GB or 6 GB, no licensing cost.
- **Three to five on RDS:** 12 GB at $64.59, plus RDS CALs purchased separately.
- **Six to eight, or a database or design workload:** 16 GB at $89.59.

Before paying, put three questions in a pre-sales ticket: whether the Windows image is a licensed install or an evaluation, what a third concurrent user costs, and what the renewal price and refund window are. Those answers change your real cost far more than the $3 gap between the two cheapest plans.

👉 See the current RackNerd Windows VPS plans and prices
