<div align="center">
<a href="https://vald.vdaas.org/">
    <img src="./assets/image/readme.svg" width="50%" />
</a>
</div>

[![License: Apache 2.0](https://img.shields.io/github/license/vdaas/vald.svg?style=flat-square)](https://opensource.org/licenses/Apache-2.0)
[![release](https://img.shields.io/github/release/vdaas/vald.svg?style=flat-square)](https://github.com/vdaas/vald/releases/latest)
[![CNCF Landscape](https://img.shields.io/badge/CNCF%20Landscape-5699C6)](https://landscape.cncf.io/?item=app-definition-and-development--database--vald)
[![Go Reference](https://pkg.go.dev/badge/github.com/vdaas/vald.svg)](https://pkg.go.dev/github.com/vdaas/vald)
[![Codacy Badge](https://img.shields.io/codacy/grade/a6e544eee7bc49e08a000bb10ba3deed?style=flat-square)](https://www.codacy.com/app/i.can.feel.gravity/vald?utm_source=github.com&utm_medium=referral&utm_content=vdaas/vald&utm_campaign=Badge_Grade)
[![Go Report Card](https://goreportcard.com/badge/github.com/vdaas/vald?style=flat-square)](https://goreportcard.com/report/github.com/vdaas/vald)
[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B21465%2Fvald.svg?type=small)](https://app.fossa.com/projects/custom%2B21465%2Fvald?ref=badge_small)
[![DeepSource](https://static.deepsource.io/deepsource-badge-light-mini.svg)](https://deepsource.io/gh/vdaas/vald/?ref=repository-badge)
[![DeepSource](https://deepsource.io/gh/vdaas/vald.svg/?label=resolved+issues&show_trend=true&token=UpNEsc0zsAfGw-MPPa6O05Lb)](https://deepsource.io/gh/vdaas/vald/?ref=repository-badge)
[![CLA](https://cla-assistant.io/readme/badge/vdaas/vald?&style=flat-square)](https://cla-assistant.io/vdaas/vald)
[![Artifact Hub](https://img.shields.io/badge/chart-ArtifactHub-informational?logo=helm&style=flat-square)](https://artifacthub.io/packages/chart/vald/vald)
[![Slack](https://img.shields.io/badge/slack-join-brightgreen?logo=slack&style=flat-square)](https://join.slack.com/t/vald-community/shared_invite/zt-db2ky9o4-R_9p2sVp8xRwztVa8gfnPA)
[![Twitter](https://img.shields.io/badge/twitter-follow-blue?logo=twitter&style=flat-square)](https://twitter.com/vdaas_vald)

<!--[![codecov](https://img.shields.io/codecov/c/github/vdaas/vald.svg?style=flat-square&logo=codecov)](https://codecov.io/gh/vdaas/vald) -->

## What is Vald?

Vald is a highly scalable distributed fast approximate nearest neighbor (ANN) dense vector search engine.

Vald is designed and implemented based on Cloud-Native architecture.

Vald has automatic vector indexing and index backup, and horizontal scaling which made for searching from billions of feature vector data.

Vald is easy to use, feature-rich and highly customizable as you needed.

It uses the fastest ANN Algorithm [NGT](https://github.com/NGT-labs/NGT) to search neighbors.

(If you are interested in ANN benchmarks, please refer to [ann-benchmarks.com](https://ann-benchmarks.com/).)

For more information, please refer to [Official Web Site](https://vald.vdaas.org).

<div align="center">
  <img src="./assets/image/svg/vald_architecture_overview.svg" width="100%" />
</div>

Vald can handle any object data, image, audio processing, video, text, binary, or etc., if converting to the vector, and be used for:

- Recognition
- Recommendation
- Detecting
- Grammar checker
- Real-time translator
- anything you want to do!

## Requirements

- Kubernetes 1.19~
- AVX2 instructions (required by Vald Agent NGT)

## Get Started

Go to [Get Started](https://vald.vdaas.org/docs/tutorial/get-started) page to try out Vald !

## Installation

### Using Helm

```shell
helm repo add vald https://vald.vdaas.org/charts
helm install vald-cluster vald/vald
```

If you use the default values.yaml, the `nightly` images will be installed.

### Using Helm-operator

Please refer to [vald-helm-operator](https://github.com/vdaas/vald/blob/main/charts/operator/helm).

## Components

<table>
  <tr>
    <th>Component</th>
    <th>Docker image</th>
    <th>latest image</th>
    <th>nightly image</th>
  </tr>
  <tr>
    <td>Agent NGT</td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-agent-ngt">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-agent-ngt?label=vdaas%2Fvald-agent-ngt&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-agent-ngt">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--agent--ngt-brightgreen?logo=docker&style=flat-square"/>
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-agent-ngt/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-agent-ngt/latest?label=vald-agent-ngt" />
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-agent-ngt/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-agent-ngt/nightly?label=vald-agent-ngt" />
      </a>
    </td>
  </tr>
  <tr>
    <td>Agent Sidecar</td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-agent-sidecar">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-agent-sidecar?label=vdaas%2Fvald-agent-sidecar&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-agent-sidecar">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--agent--sidecar-brightgreen?logo=docker&style=flat-square"/>
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-agent-sidecar/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-agent-sidecar/latest?label=vald-agent-sidecar" />
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-agent-sidecar/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-agent-sidecar/nightly?label=vald-agent-sidecar" />
      </a>
    </td>
  </tr>
  <tr>
    <td>Discoverer</td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-discoverer-k8s">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-discoverer-k8s?label=vdaas%2Fvald-discoverer-k8s&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-discoverer-k8s">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--discoverer--k8s-brightgreen?logo=docker&style=flat-square"/>
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-discoverer-k8s/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-discoverer-k8s/latest?label=vald-discoverer-k8s" />
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-discoverer-k8s/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-discoverer-k8s/nightly?label=vald-discoverer-k8s" />
      </a>
    </td>
  </tr>
  <tr>
    <td>Gateways</td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-lb-gateway">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-lb-gateway?label=vdaas%2Fvald-lb-gateway&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-lb-gateway">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--lb--gateway-brightgreen?logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://hub.docker.com/r/vdaas/vald-filter-gateway">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-filter-gateway?label=vdaas%2Fvald-filter-gateway&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-filter-gateway">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--filter--gateway-brightgreen?logo=docker&style=flat-square"/>
      </a><br/>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-lb-gateway/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-lb-gateway/latest?label=vald-lb-gateway" />
      </a><br />
      <a href="https://hub.docker.com/r/vdaas/vald-filter-gateway/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-filter-gateway/latest?label=vald-filter-gateway" />
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-lb-gateway/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-lb-gateway/nightly?label=vald-lb-gateway" />
      </a><br>
      <a href="https://hub.docker.com/r/vdaas/vald-filter-gateway/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-filter-gateway/nightly?label=vald-filter-gateway" />
      </a><br />
    </td>
  </tr>
  <tr>
    <td>Index Manager</td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-manager-index">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-manager-index?label=vdaas%2Fvald-manager-index&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-manager-index">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--manager--index-brightgreen?logo=docker&style=flat-square"/>
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-manager-index/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-manager-index/latest?label=vald-index-manager" />
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-manager-index/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-manager-index/nightly?label=vald-index-manager" />
      </a>
    </td>
  </tr>
  <tr>
    <td>Helm Operator</td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-helm-operator">
        <img src="https://img.shields.io/docker/pulls/vdaas/vald-helm-operator?label=vdaas%2Fvald-helm-operator&logo=docker&style=flat-square"/>
      </a><br/>
      <a href="https://github.com/orgs/vdaas/packages/container/package/vald/vald-helm-operator">
        <img src="https://img.shields.io/badge/ghcr.io-vdaas%2Fvald%2Fvald--helm--operator-brightgreen?logo=docker&style=flat-square"/>
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-helm-operator/tags?page=1&name=latest">
        <img src="https://img.shields.io/docker/v/vdaas/vald-helm-operator/latest?label=vald-helm-operator" />
      </a>
    </td>
    <td>
      <a href="https://hub.docker.com/r/vdaas/vald-helm-operator/tags?page=1&name=nightly">
        <img src="https://img.shields.io/docker/v/vdaas/vald-helm-operator/nightly?label=vald-helm-operator" />
      </a>
    </td>
  </tr>
</table>

Docker images tagging policy:

- `nightly` ... latest build of main branch
- `vX.X.X` ... released versions
- `latest` ... latest build of release versions
- `stable` ... latest long-term supported version

## Tools

- [SDK](https://vald.vdaas.org/docs/user-guides/sdks/): Official client libraries
- [Demo](https://github.com/vdaas/vald-demo): Demo repository using sample data

## Vald Users

<p align="center">
  <a href="https://www.lycorp.co.jp/en/" target="_blank">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/image/vald-users/lycorp_white.png">
    <source media="(prefers-color-scheme: light)" srcset="./assets/image/vald-users/lycorp_black.png">
    <img alt="LY" src="./assets/image/vald-users/lycorp.png" width="150" height="120">
  </picture>
  </a>
  <a href="https://jpsearch.go.jp/" target="_blank">
    <img src="./assets/image/vald-users/japansearch_color.png" alt="jpsearch" width="150" height="120"/>
  </a>
</p>

## Contribution

Please read the [contribution guide](https://vald.vdaas.org/docs/contributing/contributing-guide).

Before your first commit to this repository, it is strongly recommended to run the commands below.

```shell
git clone https://github.com/MeAkash77/VectorScale-Distributed-Vector-Search-Indexing-Engine.git && cd vald
make init
```

## Contributors

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->

[![All Contributors](https://img.shields.io/badge/all_contributors-27-orange.svg?style=flat-square)](#contributors)

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

## LICENSE

Vald released under Apache 2.0 license, refer [LICENSE](https://github.com/MeAkash77/vald/blob/main/LICENSE) file.

[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B21465%2Fvald.svg?type=large)](https://app.fossa.com/projects/custom%2B21465%2Fvald?ref=badge_large)
