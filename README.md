<div align="center">

<img src="snap/gui/rovar.png" alt="Rovar logo" width="128" />

# Rovar

**A native design editor for interfaces and interactive prototypes.**

[![rovar](https://snapcraft.io/rovar/badge.svg)](https://snapcraft.io/rovar)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Rovar](https://github.com/cradiy/rovar), a design editor with reusable components, media and AI-assisted editing.

</div>

---

## Getting Started

<a href="https://snapcraft.io/rovar"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install rovar
rovar
```

Launch from the terminal or your application menu.

## Configure

Manage preferences and workspace connections in the app. There are no `snap set` options.

| Optional access | Command |
| --- | --- |
| Designs and media on removable storage | `sudo snap connect rovar:removable-media` |

To enable a host AI agent that supports skills and local commands:

```bash
mkdir -p ~/.agents/skills/rovar-design
cp /snap/rovar/current/usr/share/rovar/skills/rovar-design/SKILL.md ~/.agents/skills/rovar-design/
```

Restart the agent session and open a design in Rovar. The skill uses the same `rovar` command to reach the editor.

## Limitations

- A working GPU and desktop session are required.
- Files outside your home and connected removable storage are restricted.
- The optional self-hosted workspace server and browser edition are not included; connect to an existing server from the app.
- Agents must be able to run `/snap/bin/rovar`; other confined applications may restrict this.

## Build

```bash
git clone https://github.com/sidalit/rovar-snap.git
cd rovar-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/rovar-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/cradiy/rovar/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/rovar-snap/blob/main/LICENSE).
