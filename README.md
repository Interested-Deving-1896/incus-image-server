[update-readmes]   Mode: rewrite — migrating to template structure...
# incus-image-server

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/incus-image-server)

<!-- AI:start:what-it-does -->
This project provides a unified simplestreams image server for managing and distributing container images for LXC, LXD, and Incus. It includes a multi-distribution build pipeline and supports ChromiumOS stage3 builds. It is designed for developers and system administrators who need to automate image creation, synchronization, and distribution across diverse environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of several key components designed to manage and serve simplestreams images for LXC/LXD/Incus environments. The architecture includes a unified image server, multi-distro build pipelines, and ChromiumOS stage3 support. Workflows automate tasks such as mirroring repositories, building and publishing images, syncing upstream sources, and managing tokens. The repository is organized into directories for scripts, server configurations, and documentation.

Directory structure:
```plaintext
.
├── .github                 # GitHub workflows and CI/CD configurations
├── demo-server             # Example server setup for testing and demonstration
├── dep-graph               # Dependency graph files for build pipelines
├── scripts                 # Shell scripts for automation and orchestration
├── unified-image-server    # Core server implementation for simplestreams images
├── LICENSE                 # Project license
├── README.md               # Project documentation
```
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/incus-image-server.git
cd incus-image-server
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
- **add-mirror-repo.yml**: Adds a new repository to the mirror list. Requires `MIRROR_TOKEN` secret.
- **build-and-publish.yml**: Builds images and publishes them to the simplestreams server. Requires `PUBLISH_TOKEN` and `BUILD_SECRET`.
- **check-gitlab-sync.yml**: Verifies synchronization status between GitHub and GitLab repositories. Requires `GITLAB_TOKEN`.
- **chromiumos-stage3-build.yml**: Builds ChromiumOS stage3 images. Requires `CHROMIUMOS_BUILD_KEY`.
- **cleanup-pollution.yml**: Removes temporary files and artifacts from the workspace. No secrets required.
- **clone-org.yml**: Clones all repositories from a specified organization. Requires `ORG_CLONE_TOKEN`.
- **create-readmes.yml**: Generates README files for repositories based on templates. No secrets required.
- **demo-server-ci.yml**: Runs CI tasks for the demo server. Requires `DEMO_SERVER_TOKEN`.
- **mirror-artifacts.yml**: Mirrors build artifacts to external storage. Requires `ARTIFACT_STORAGE_KEY`.
- **mirror-orgs-full.yml**: Performs a full synchronization of all repositories in an organization. Requires `ORG_MIRROR_TOKEN`.
- **sync-to-gitlab.yml**: Synchronizes repositories from GitHub to GitLab. Requires `GITLAB_SYNC_TOKEN`.
- **token-health.yml**: Checks the validity of API tokens used in workflows. Requires `API_TOKENS`.
- **update-readmes.yml**: Updates README files across repositories. No secrets required.
- **upstream-commits.yml**: Monitors upstream repositories for new commits. Requires `UPSTREAM_TOKEN`.
- **upstream-prs.yml**: Tracks upstream pull requests for changes. Requires `UPSTREAM_TOKEN`.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/incus-image-server`](https://github.com/Interested-Deving-1896/incus-image-server) and mirrored through:

```
Interested-Deving-1896/incus-image-server  ──►  OpenOS-Project-OSP/incus-image-server  ──►  OpenOS-Project-Ecosystem-OOC/incus-image-server
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896) - 232 commits

*Note: This repository is a mirror. For the upstream source, refer to the original project.*
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
<!-- License not detected — add a LICENSE file to this repo. -->
<!-- AI:end:license -->
