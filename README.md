## Kağan Çapar

Vulnerability researcher. I find memory-corruption bugs in native code and build the exploits that prove they matter. Windows and Linux userland, image and colour-profile parsers, avionics software.

Offensive Security Lead at TurkNet. Independent researcher with the Trend Zero Day Initiative since 2022. Doing this since 2006.

### Published vulnerabilities

| CVE | Target | Class | Severity |
| --- | --- | --- | --- |
| [CVE-2026-96054](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2026-96054) | Microsoft Color Management (Windows) | Heap-based buffer overflow, remote code execution | CVSS 7.0, Microsoft Important |
| [CVE-2026-54984](https://www.zerodayinitiative.com/advisories/ZDI-26-543/) | Windows ICC profile parsing (`Mscms.dll`) | Out-of-bounds write, remote code execution | CVSS 7.8 |
| [CVE-2026-5201](https://nvd.nist.gov/vuln/detail/CVE-2026-5201) | GNOME gdk-pixbuf JPEG loader | Heap buffer overflow | CVSS 7.5, Red Hat Important |
| [CVE-2022-29072](https://nvd.nist.gov/vuln/detail/CVE-2022-29072) | 7-Zip 21.07 (`7z.dll`) | Command execution via the Help>Contents handler | CVSS 7.8 |
| [CVE-2021-47881](https://nvd.nist.gov/vuln/detail/CVE-2021-47881) | dataSIMS Avionics ARINC 664-1 | Stack overflow, full instruction-pointer control | Code execution, [PoC published](https://www.exploit-db.com/exploits/49577) |

Image and colour-profile parsers are a recurring target of mine. The gdk-pixbuf bug reached essentially every Linux desktop, including RHEL, Ubuntu, Debian, Fedora and Arch.


On CVE-2022-29072, NVD records that third parties contest whether privilege escalation is achievable. The command execution and the heap overflow itself are not contested. The write-up and proof of concept are still up at [the repository](https://github.com/kagancapar/CVE-2022-29072), 670+ stars and 100+ forks, so the mechanism can be judged directly.

### Talks

**DEF CON 34**, main stage, Las Vegas 2026
[From Fuzzer Noise to a Weaponized PHP Exploit: Exploiting a PHP Use-After-Free Vulnerability](https://www.youtube.com/watch?v=ngcr8T6vrXw)

### How I work

Fuzzing harness design with AFL++, WinAFL and libFuzzer, then crash triage, root-cause analysis and weaponization. The forks on this profile are the targets and the infrastructure I fuzz against, not abandoned projects.

I also build the capability, not just the findings: fuzzing infrastructure, hardware test labs and isolated malware analysis environments, at Turkish Aerospace and again at TurkNet.

### Shellcode and primitives

Small, self-contained pieces published over the years: Windows persistence, Event Viewer disabling, Linux reverse TCP, Linux enumeration, ASLR disabling, sudo version enumeration. Written to be read, not just run.

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/kagancapar) · [kagancapar.github.io](https://kagancapar.github.io) · OSCP, OSCE, CISM
