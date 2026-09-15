# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.1](https://github.com/cordanaLLM/nucleus/compare/v0.1.0...v0.1.1) (2026-09-15)


### Features

* **governance:** declare the praetor os-image profile ([#13](https://github.com/cordanaLLM/nucleus/issues/13)) ([b7a0ef1](https://github.com/cordanaLLM/nucleus/commit/b7a0ef198d7fe7bb8e4feea33bf5268f581b9c38))
* **init:** bootstrap lusoris-kernel-forge repository ([e527cd3](https://github.com/cordanaLLM/nucleus/commit/e527cd3400c76dac9aa2812f50e732a8fdfafbfb))
* **onboarding:** establish full ecosystem and repository parity with lusoris-cloud-images ([#7](https://github.com/cordanaLLM/nucleus/issues/7)) ([c3397fc](https://github.com/cordanaLLM/nucleus/commit/c3397fcec25c8b71776f4d58b4cd61f00b5a8423))
* **packaging:** implement multi-arch builder container, dual packaging pipeline, and qemu boot verification ([#9](https://github.com/cordanaLLM/nucleus/issues/9)) ([494ea58](https://github.com/cordanaLLM/nucleus/commit/494ea58dcd7032e19fc82691398f06a14749ece1))

## [Unreleased]

### Added
- Extended Renovate configuration (`renovate.json`) with automated GitHub Actions digest pinning, Monday batch scheduling, and SSOT regex managers for `versions.json`.
- Root-level governance policies and community contracts (`CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `GOVERNANCE.md`, `MAINTAINERS.md`, `SECURITY.md`, `SUPPORT.md`).
- Static code hygiene tooling configs (`.editorconfig`, `.gitleaks.toml`, `.markdownlint.json`, `.codespellrc`, `.pre-commit-config.yaml`, `.semgrepignore`).
- Google Release Please automated release management (`release-please-config.json`, `.release-please-manifest.json`).
- Python test harness dependencies (`requirements-test.txt`) and unified pytest/coverage/ruff configurations in `pyproject.toml`.

## [0.1.0] - 2026-09-10

### Added
- Initial repository bootstrap for `lusoris-kernel-forge`.
- Multi-stream kernel compilation matrix across 4 streams:
  - `bleeding` (Linux 7.3-rc2) for Blackwell RTX 5090/B200, CXL 3.0, and sched-ext.
  - `mainstream` (Linux 7.2.4) for Intel Battlemage Xe2, AMD ROCm 10, and NVIDIA 565/610.
  - `lts` (Linux 6.18.50) for enterprise Kubernetes nodes, OpenZFS 2.3, and CloudNativePG.
  - `realtime` (Linux 7.2-rt) for full PREEMPT_RT deterministic low-latency edge workloads.
- Multi-architecture native compilation and cross-compilation support for `x86_64`, `arm64`, and `riscv64`.
- Modular, security-hardened KConfig fragment framework meeting Kernel Self-Protection Project (KSPP) and CIS Linux Benchmark Level 2 baselines.
- Single Source of Truth `versions.json` declarative manifest backed by JSON Schema validation `versions.schema.json`.
- NASA/JPL Power of 10 compliant shell build pipelines (`scripts/build-kernel.sh`, `scripts/kconfig/merge_config.sh`) with strict ShellCheck compliance.
- Automated downstream dispatch contracts for integration into `lusoris-cloud-images`.
