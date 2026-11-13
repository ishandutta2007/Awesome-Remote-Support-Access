# Awesome-Remote-Support-Access

# Awesome Remote Support & Access

> A curated list of top Remote Support and Access platforms — both SaaS/Hosted commercial solutions and open-source alternatives for troubleshooting, controlling, and collaborating on remote desktops and devices.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [TeamViewer](#teamviewer)
  - [AnyDesk](#anydesk)
  - [Zoho Assist](#zoho-assist)
  - [Splashtop](#splashtop)
  - [BeyondTrust Remote Support](#beyondtrust-remote-support)
  - [ConnectWise Control](#connectwise-control)
- [Open-Source Software](#-open-source-software)
  - [RustDesk](#rustdesk)
  - [Apache Guacamole](#apache-guacamole)
  - [MeshCentral](#meshcentral)
  - [ScottiBYTE Assist](#scottibyte-assist)
  - [Remmina](#remmina)
  - [FreeRDP](#freerdp)
  - [xrdp](#xrdp)
  - [noVNC](#novnc)
  - [mRemoteNG](#mremoteng)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Remote Support and Access platforms. These are not open-source but are included as reference points for feature comparison.

### TeamViewer
**Type:** Industry-standard remote access and support
TeamViewer is one of the most widely recognized remote support tools, offering cross-platform remote control, file transfer, VPN, and meeting capabilities. It is the benchmark against which open-source alternatives like RustDesk are measured [citation:2][citation:3]. Pricing is per-seat with tiered plans, and commercial use requires a license.

### AnyDesk
**Type:** Fast remote desktop with low latency
AnyDesk is known for its proprietary video codec (DeskRT) designed for low-bandwidth, high-latency connections. It offers remote control, file transfer, and session recording. Like TeamViewer, it is frequently cited as the proprietary standard that open-source tools aim to replace [citation:2][citation:11].

### Zoho Assist
**Type:** Remote support within Zoho ecosystem
Zoho Assist provides remote support and unattended access capabilities as part of the broader Zoho suite. It includes screen sharing, file transfer, multi-session support, and integration with Zoho Desk for ticketing. Suited for organizations already using Zoho products.

### Splashtop
**Type:** High-performance remote access
Splashtop provides remote desktop and support with a focus on performance for creative and technical workloads. It offers attended and unattended access, file transfer, and multi-monitor support. Pricing is per-user with tiered plans.

### BeyondTrust Remote Support
**Type:** Enterprise privileged remote access
BeyondTrust Remote Support provides secure, audited remote access for help desks and privileged users, with features like session recording, credential injection, and granular access controls. It is positioned for enterprises with strict compliance requirements.

### ConnectWise Control
**Type:** Remote support for IT service providers
ConnectWise Control (formerly ScreenConnect) provides remote support, unattended access, and meeting capabilities, with a focus on MSPs and IT service providers. It offers self-hosted and cloud options, with extensive customization and integration capabilities.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Remote Support and Access tools. The open-source ecosystem spans **full remote desktop applications**, **clientless gateways**, **web-based management platforms**, **attended-only assistance tools**, and **protocol implementations**.

### RustDesk
**Stack:** Rust / Flutter | **License:** AGPL-3.0
RustDesk is the leading open-source remote desktop alternative to TeamViewer and AnyDesk, with **126,000+ GitHub stars** and a mature, actively developed codebase [citation:2][citation:3]. Key features include:
- **Full self-hosting** of relay and signaling servers, giving complete control over data and eliminating dependency on third-party SaaS [citation:3][citation:14]
- **P2P connections with end-to-end encryption** based on NaCl, ensuring session privacy even when relayed [citation:3]
- **Cross-platform support**: Windows, macOS, Linux, iOS, Android, and Web [citation:3][citation:14]
- **Modern codec support**: VP8/VP9/AV1 software codecs and H264/H265 hardware codecs [citation:3]
- **Wayland multi-scaled display support** (nightly), addressing a gap where commercial rivals like TeamViewer and AnyDesk have been slow to adapt [citation:11]
- **No administrative privileges required** on Windows, with on-demand elevation locally or remotely [citation:3]

A free open-source server (RustDesk Server OSS) is available for self-hosting, while a Pro version adds web console, SSO, and enterprise controls [citation:3][citation:14].  
**Best for:** Teams and organizations wanting a full-featured, self-hostable TeamViewer/AnyDesk replacement with strong performance and active development, accepting the operational overhead of running relay servers.

### Apache Guacamole
**Stack:** Java / JavaScript (HTML5) | **License:** Apache-2.0
Apache Guacamole is a **clientless remote desktop gateway** supporting VNC, RDP, and SSH—no plugins or client software required, only a web browser [citation:5][citation:10]. It is the ideal solution for providing browser-based access to desktops without installing anything on the user's device. Version 1.6.0 (June 2025) improved rendering performance, Docker support, and added Duo v4 integration [citation:10]. The platform is built on documented APIs, allowing tight integration into other applications, and is actively maintained by a community of developers [citation:5].  
**Best for:** Organizations wanting clientless, browser-based remote access to desktops with no software installation required, particularly for BYOD or third-party access scenarios.

### MeshCentral
**Stack:** Node.js | **License:** Apache-2.0
MeshCentral is a **full computer management web site** that runs on your own server, allowing you to remotely manage and control computers on a local network or anywhere on the internet [citation:9][citation:13]. After installing an agent on each device, it provides **web-based remote desktop, terminal, and file management** capabilities [citation:9]. It is positioned as a comprehensive remote monitoring and management (RMM) solution rather than a simple remote support tool, with device grouping and agent deployment workflows.  
**Best for:** IT teams wanting a self-hosted, web-based platform for both remote support and ongoing device management, accepting the broader RMM scope.

### ScottiBYTE Assist
**Stack:** Node.js / Docker / WebRTC | **License:** Open Source
ScottiBYTE Assist is an open-source, self-hosted **attended remote-assistance platform** for Windows and Ubuntu Linux, explicitly designed as an alternative to TeamViewer, Chrome Remote Desktop, AnyDesk, and RustDesk [citation:6]. Its key differentiator is a deliberate focus on **customer-approved support sessions** rather than persistent unattended access. Features include:
- **Six-digit support codes** instead of permanent remote-access IDs
- **Explicit customer approval** before desktop access
- **No unattended-access mode** by design
- Two-way voice and text chat, clipboard sharing, file transfer, and an interactive customer terminal
- Provider administration and session auditing
- Self-hosted server with a public portal for client downloads [citation:6]

It supports X11 and Wayland on Linux, with a Docker Compose deployment model.  
**Best for:** Support teams wanting an attended-only, consent-first remote assistance tool that prioritizes customer approval and auditability over persistent access, accepting a narrower feature set than full remote desktop platforms.

### Remmina
**Stack:** C / GTK | **License:** GPL-2.0
Remmina is a remote desktop client for Linux and other Unix-like systems, supporting RDP, VNC, SSH, SFTP, SPICE, and other protocols in a single interface [citation:2][citation:7]. It provides tabbed sessions, automatic session management, and granular configuration. It is a **client** rather than a server, making it useful for technicians who need to connect to multiple remote systems from a Linux workstation.  
**Best for:** Linux users needing a versatile open-source remote desktop client with support for many protocols and session organization.

### FreeRDP
**Stack:** C | **License:** Apache-2.0
FreeRDP is a free remote desktop protocol library and client implementation, with **13,900+ GitHub stars** [citation:2][citation:7]. It provides the foundational RDP protocol stack used by many other tools, including Remmina. It is positioned for developers building RDP-based solutions or users needing a lightweight, protocol-level RDP client.  
**Best for:** Developers and advanced users wanting a robust, open-source RDP protocol library and client foundation.

### xrdp
**Stack:** C | **License:** GPL-2.0
xrdp is an open-source **RDP server** for Linux, allowing Windows Remote Desktop clients to connect to Linux desktops [citation:2][citation:7]. It is a key building block for making Linux systems accessible via RDP, often paired with a VNC server or X11 session. With 6,700+ GitHub stars and active maintenance, it is a mature solution for RDP-based access to Linux.  
**Best for:** Linux administrators wanting to enable RDP access to Linux desktops for Windows clients, often in conjunction with a VNC backend.

### noVNC
**Stack:** JavaScript | **License:** MPL-2.0
noVNC is an open-source **VNC client web application**, with 14,100+ GitHub stars [citation:2][citation:7]. It allows VNC sessions to be accessed through any modern web browser, making it a key component for building clientless remote access solutions. It is often used alongside a VNC server (like TigerVNC) to provide browser-based access.  
**Best for:** Developers building browser-based remote access solutions, or users wanting to access VNC servers through a web interface without installing a client.

### mRemoteNG
**Stack:** C# / .NET | **License:** GPL-2.0
mRemoteNG is a **tabbed, multi-protocol remote connections manager**, with 11,100+ GitHub stars [citation:2][citation:7]. It allows technicians to manage connections to RDP, VNC, SSH, Telnet, and other remote systems from a single interface, with tabbed sessions and credential management. It is a productivity tool for administrators who manage many remote connections.  
**Best for:** IT administrators and support technicians wanting a single, tabbed interface for managing multiple remote connections across protocols.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Self-Hosted Server | Clientless (Browser) | Attended-Only | Best For |
|----------|---------|-------|---------------------|----------------------|---------------|----------|
| **TeamViewer** | Proprietary | Cloud | ❌ | (Web client) | ❌ | Industry-standard support |
| **AnyDesk** | Proprietary | Cloud | ❌ | (Web client) | ❌ | Low-latency remote control |
| **RustDesk** | AGPL-3.0 | Rust | ✅ | ✅ (Web) | ❌ | Full TeamViewer alternative |
| **Apache Guacamole** | Apache-2.0 | Java/JS | ✅ | ✅ | ❌ | Browser-based access |
| **MeshCentral** | Apache-2.0 | Node.js | ✅ | ✅ | ❌ | RMM + remote support |
| **ScottiBYTE Assist** | Open Source | Node.js | ✅ | (Portal) | ✅ | Consent-first assistance |
| **Remmina** | GPL-2.0 | C/GTK | ❌ (Client) | ❌ | ❌ | Linux multi-protocol client |
| **FreeRDP** | Apache-2.0 | C | ❌ (Library) | ❌ | ❌ | RDP protocol foundation |
| **xrdp** | GPL-2.0 | C | ✅ (RDP server) | ❌ | ❌ | Linux RDP server |
| **noVNC** | MPL-2.0 | JavaScript | ❌ (Client) | ✅ | ❌ | Browser VNC client |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Remote Support or Access tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits** between **full remote desktop applications** (RustDesk, the clear leader with 126k+ stars and active development [citation:2][citation:3]), **clientless gateways** (Apache Guacamole for browser-only access [citation:5]), **web-based management platforms** (MeshCentral for RMM plus support [citation:9]), and **consent-first attended tools** (ScottiBYTE Assist [citation:6]). **RustDesk** is the most direct open-source replacement for TeamViewer and AnyDesk, with self-hosted servers, P2P encryption, and even Wayland multi-scaled display support that commercial rivals lack [citation:11]. **Apache Guacamole** remains unmatched for zero-install browser access.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
