# Security Recovery Core (SRC)

**Hardware-Assisted, Unbrickable Recovery System**

## Overview

SRC is a production-ready firmware recovery system that runs before BIOS/UEFI, providing automatic firmware backup and recovery capabilities. It protects against permanent bricking while preserving user data.

## Architecture

- **Recovery Core Firmware**: Runs on EC/MCU or reserved SPI flash region (pre-UEFI)
- **Boot Failure Detection**: Multiple redundant methods (GPIO, watchdog, POST codes)
- **USB Recovery System**: Structured backup rotation (exactly 2 backups)
- **Cross-Platform CLI**: Terminal control tool for all major operating systems

## Quick Start

See [INSTALL.md](docs/INSTALL.md) for installation instructions.

## Project Structure

```
SRC/
├── firmware/          # Recovery Core firmware source
├── cli/              # Host-side CLI tool
├── docs/             # Documentation
├── tools/            # Build tools and utilities
└── tests/            # Test suites
```

## Security

- Cryptographic signature verification
- Tamper-resistant logging
- Multi-step uninstall confirmation
- Hardware-level protection

## License

Open-source friendly (see LICENSE file)
