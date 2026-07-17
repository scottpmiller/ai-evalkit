# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/), and the project follows
[Semantic Versioning](https://semver.org/).

## [Unreleased]

### Changed
- **Breaking:** the import package and CLI are now `evalcore` (were `evalkit`).
  Update `import evalkit` to `import evalcore` and the `evalkit` command to
  `evalcore`. The distribution name (`evalcore`) is unchanged.
- Lowered the minimum Python to **3.11** (was 3.14).

### Added
- `evalcore.__version__`.
- Public `evalcore.adapters.expand_env` for `${VAR}` expansion in custom
  adapters (replaces the private `adapters._env` module).
- Exception hierarchy: `EvalcoreError` (base) and `ConfigError` (also a
  `ValueError`, so existing handlers keep working).
- Top-level convenience entry points: `load_suite`, `load_cases`, `run_suite`,
  `run_suite_sync`.
- HTML rendering for `sweep` and `pairwise` reports, and `--report` /
  `--report-out` on those CLI commands.

## [0.1.0] - 2026-07-16

- Initial public release: adapters (http/replay), graders (deterministic,
  numeric, classification, LLM judge + panel), runner (N-sampling, concurrency,
  retries, checkpoint/resume), compare/gate, sweep, pairwise, blind human
  rating + ranking with judge agreement, Markdown/HTML reporters, JSON +
  column-store outbox, and content-hash provenance.

[Unreleased]: https://github.com/scottpmiller/evalcore/compare/0.1.0...HEAD
[0.1.0]: https://github.com/scottpmiller/evalcore/releases/tag/0.1.0
