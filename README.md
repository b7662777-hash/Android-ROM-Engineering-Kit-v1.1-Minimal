# Android ROM Engineering Kit

A proposed lightweight toolkit for reproducible Android ROM engineering, device bring-up, recovery development, and build automation.

> **Documentation-only starting point:** this repository currently contains a README, not a published collection of working scripts. There is no installation command, executable toolkit, or verified toolkit release yet. The repository name's version suffix should not be interpreted as proof of a downloadable release.

## Intended audience

Android platform developers, custom ROM maintainers, recovery developers, and learners who want transparent, reproducible tooling rather than opaque one-click modification scripts.

## Current versus planned scope

| Area | Status |
| --- | --- |
| Project outline | Available in this README |
| ROM engineering scripts | Planned; not present in the current repository |
| Device/kernel helpers | Planned |
| Image/recovery tooling | Planned |
| Build/package helpers | Planned |
| ADB/Fastboot automation | Planned |
| Automated tests and CI | Planned |
| Installation and releases | Not yet provided |

There are no runnable quick-start instructions until an implementation is committed.

## Suggested first milestone

Start with a read-only environment and workspace checker rather than flashing, deleting, or rewriting device partitions.

| Deliverable | Acceptance criterion |
| --- | --- |
| Environment report | Reports detected tools and missing prerequisites without installing anything automatically |
| Workspace validation | Checks user-specified paths without modifying source files |
| Dry-run output | Shows proposed commands without executing device-changing operations |
| Tests | Covers valid paths, missing tools, invalid inputs, and failure handling |
| Documentation | Includes tested platforms, exact commands, limitations, and sample output |

These are proposed requirements, not implemented features. Future behavior should be tested and documented before being advertised.

## Related repositories

These are separate projects in the same GitHub account, not components bundled by this toolkit. Check their individual branches, credits, licenses, and compatibility before use.

| Repository | Role |
| --- | --- |
| [Action-TWRP-Builder](https://github.com/b7662777-hash/Action-TWRP-Builder) | Recovery build automation |
| [Action-OFRP-Builder](https://github.com/b7662777-hash/Action-OFRP-Builder) | OrangeFox build workflow |
| [device_xiaomi_raphael](https://github.com/b7662777-hash/device_xiaomi_raphael) | Xiaomi Raphael ROM device configuration |
| [kernel_xiaomi_raphael](https://github.com/b7662777-hash/kernel_xiaomi_raphael) | Xiaomi Raphael kernel source |
| [android_device_xiaomi_raphael-orangefox](https://github.com/b7662777-hash/android_device_xiaomi_raphael-orangefox) | Recovery device configuration |

## Safety principles

| Principle | Requirement for future tooling |
| --- | --- |
| Preserve originals | Never overwrite original ROM packages or extracted source without explicit approval |
| Validate devices | Check exact device, partition layout, and compatibility before device-changing operations |
| Make actions visible | Explain commands, prerequisites, and expected outputs |
| Prefer reversible work | Use isolated work directories and maintain recovery instructions |
| Protect sensitive data | Do not commit credentials, signing keys, private device data, or confidential logs |

Flashing or modifying Android system images can cause data loss or make a device unbootable. This README is not a flashing guide or a compatibility guarantee.

## Contributing

Begin with a focused proposal or a small, tested read-only utility. State the supported host OS, required tools, input/output contract, and failure behavior. Include reproducible tests before expanding to destructive or device-changing operations.

For bug reports once code exists, provide the relevant device codename, Android/ROM version, host environment, exact command, expected result, and sanitized logs.

## License

No explicit repository-wide license file is currently published with this documentation-only project. Public availability does not imply unrestricted redistribution. The maintainer must choose an appropriate license before presenting future code as licensed open source; preserve all third-party licenses separately.
