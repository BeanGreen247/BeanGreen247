👋 Hi, I’m Thomas — an **Analytics & Data Platforms Specialist @ ČEZ Distribuce a.s.**
Linux & Windows power‑user. DevOps mindset. Open‑source advocate with a growing focus on **Ansible automation** and infrastructure analytics.

```python
from dataclasses import dataclass, asdict
import json
import argparse

@dataclass
class About:
    name: str = "Thomas (Tomáš Mozdřeň)"
    company: str = "ČEZ Distribuce a.s."
    position: str = "Analytics & Data Platforms Specialist"
    core_expertise: list = None
    professional_goal: str = "To advance infrastructure automation with Ansible and enhance data-driven operations across platforms."
    links: dict = None
    contact: dict = None
    documents: dict = None

    def __post_init__(self):
        if self.core_expertise is None:
            self.core_expertise = [
                "Linux", "Windows", "Git", "Ansible", "Python", "SQL",
                "Automation", "Infrastructure Analytics", "Data Engineering"
            ]
        if self.links is None:
            self.links = {
                "Website": "https://beangreen247.xyz/",
                "LinkedIn": "https://www.linkedin.com/in/tom%C3%A1%C5%A1-mozd%C5%99e%C5%88-3382b71a6/"
            }
        if self.contact is None:
            self.contact = {
                "Linktree": "https://linktr.ee/BeanGreen247",
                "Email": "mozdrent@gmail.com"
            }
        if self.documents is None:
            self.documents = {
                "CV": "http://beangreen247.xyz/documents/cv.pdf",
                "Resume": "http://beangreen247.xyz/documents/resume.pdf"
            }

    def to_markdown(self) -> str:
        md = f"# {self.name}\n\n"
        md += f"**{self.position} @ {self.company}**\n\n"
        md += "## Core expertise\n"
        for item in self.core_expertise:
            md += f"- {item}\n"
        md += f"\n## Professional goal\n{self.professional_goal}\n\n"
        md += "## Links\n"
        for k, v in self.links.items():
            md += f"- **{k}:** {v}\n"
        md += "\n## Contact\n"
        for k, v in self.contact.items():
            md += f"- {k}: {v}\n"
        md += "\n## Documents\n"
        for k, v in self.documents.items():
            md += f"- **{k}:** {v}\n"
        return md

    def to_json(self) -> str:
        return json.dumps(asdict(self), indent=2, ensure_ascii=False)

    def headline(self) -> str:
        return f"{self.name} — {self.position} @ {self.company} — Ansible automation & data platforms"


def main():
    parser = argparse.ArgumentParser(description="Print Thomas's About profile in different formats")
    parser.add_argument('--json', action='store_true', help='Print JSON output')
    parser.add_argument('--brief', '--headline', action='store_true', help='Print a one-line headline')
    args = parser.parse_args()

    about = About()

    if args.brief:
        print(about.headline())
        return

    if args.json:
        print(about.to_json())
        return

    # default: markdown
    print(about.to_markdown())

if __name__ == '__main__':
    main()
```

📫 How to reach me:
* [Linktree](https://linktr.ee/BeanGreen247)
* [Email](mailto:mozdrent@gmail.com)

📚 Documents:
* [CV](http://beangreen247.xyz/documents/cv.pdf)
* [Résumé](http://beangreen247.xyz/documents/resume.pdf)

💡 Open‑Source & Projects Highlights:
* Backed and contributed to multiple open‑source projects
* Focused on building automation solutions and monitoring tools for Proxmox, Linux, and hybrid infrastructure environments

  Other docs...
* [nvs-5400m-arch-linux](https://github.com/BeanGreen247/nvs-5400m-arch-linux)
* [Modded GTA ViceCity README](http://beangreen247.xyz/moddedGamesDocs/README_MODDED_GTA_VC.txt)
* [Pushing Windows 11/10 Pro to its limits](https://docs.google.com/document/d/1CjGxVwnLESVqdD1OwZjAxAjxO6Fh6J_VXPo3jTe8WnA/edit?usp=sharing)
* [Ultimate Windows 10 Performance optimization guide](https://beangreen247.xyz/ultimatewindowsperformanceoptimization.html)
* [WINE Performance optimization](https://beangreen247.xyz/wineperformanceoptimization.html)

---
### What Projects I've Backed

[![Projects Backed](https://img.shields.io/badge/dynamic/json?url=https://gist.githubusercontent.com/BeanGreen247/9d4390c70565eeda217a4a2e72d33fec/raw/e883d1dd286cd10459b6d1da8644fbf8eed55f66/sponsored_projects.json&label=projects%20backed&query=$.totals.count)](#)
[![One-Time Donations](https://img.shields.io/badge/dynamic/json?url=https://gist.githubusercontent.com/BeanGreen247/9d4390c70565eeda217a4a2e72d33fec/raw/e883d1dd286cd10459b6d1da8644fbf8eed55f66/sponsored_projects.json&label=one-time%20donations&query=$.totals.oneTimeUsd&prefix=$)](#)

<details>
<summary>Projects supported via GitHub Sponsors</summary>
  
* Armbian → [https://github.com/sponsors/armbian?frequency=one-time\&sponsor=BeanGreen247](https://github.com/sponsors/armbian?frequency=one-time&sponsor=BeanGreen247)
* Thomas Adam (fvwm maintainer) → [https://github.com/sponsors/ThomasAdam?frequency=one-time\&sponsor=BeanGreen247](https://github.com/sponsors/ThomasAdam?frequency=one-time&sponsor=BeanGreen247)
* coletdjnz (yt-dlp maintainer) → [https://github.com/sponsors/coletdjnz?frequency=one-time\&sponsor=BeanGreen247](https://github.com/sponsors/coletdjnz?frequency=one-time&sponsor=BeanGreen247)
* Rem0o (FanControl maintainer) → [https://github.com/sponsors/Rem0o?frequency=one-time\&sponsor=BeanGreen247](https://github.com/sponsors/Rem0o?frequency=one-time\&sponsor=BeanGreen247)

</details>

<details>
<summary>Projects supported via SPI</summary>

* SPI General Donation  
* Arch Linux  
* Debian Project Donation  
* FFmpeg  
* LibreOffice  
* MinGW  
* OpenSSL Foundation  
* OpenZFS  
* PostgreSQL General Contribution  
* systemd  

[Donate via SPI](https://co.clickandpledge.com/advanced/default.aspx?wid=34115)

</details>

<details>
<summary>Proof of support</summary>

<img width="815" height="598" alt="Snímek obrazovky 2025-09-19 093335" src="https://github.com/user-attachments/assets/a634e78f-f245-43b0-8299-0a54b9efa561" />
<img width="1088" height="993" alt="Snímek obrazovky 2025-09-19 093058" src="https://github.com/user-attachments/assets/88e414ee-4c7a-422d-9a04-bd1b6c61d9a7" />


</details>

