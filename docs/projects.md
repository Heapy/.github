# Explore Heapy

A directory of tools, libraries, applications, and experiments. Start with the problem you want to solve, then open a project's README for setup and compatibility details.

[Organization home](https://github.com/Heapy) · [AI and agent workflows](#ai-and-agent-workflows) · [Kotlin libraries and UI](#kotlin-libraries-and-ui) · [Build tools](#kotlin-toolchain-and-build-tools) · [Everyday software](#everyday-software) · [Infrastructure](#infrastructure-and-home) · [Community](#community-and-learning) · [Experiments](#benchmarks-and-early-projects) · [Earlier work](#earlier-work)

## AI and agent workflows

Keep coding sessions available, give agents useful context, and connect them to the systems you use.

| Project | What it helps you do | Notes |
| :--- | :--- | :--- |
| [kotgent](https://github.com/Heapy/kotgent) | Run and supervise Claude, Codex, Junie, and shell sessions from a terminal, browser, or PWA; keep a local project backlog. | Agent processes run in tmux on your host. |
| [kortex](https://github.com/Heapy/kortex) | Add Kotlin and JVM skills, review agents, and task workflows to coding assistants. | Plugins/extensions for Junie, Codex, and Claude Code. |
| [keemun](https://github.com/Heapy/keemun) | Model architecture decisions, constraints, options, and rationale as a graph that agents can query and update. | Experimental; includes a CLI and agent skill. |
| [kotlm](https://github.com/Heapy/kotlm) | Connect projects to a Codex subscription through an OpenAI-compatible proxy with separate project keys, limits, and metrics. | Uses the Codex subscription backend. |
| [argo-workflows-mcp](https://github.com/Heapy/argo-workflows-mcp) | Let MCP clients inspect and operate Argo workflows, templates, schedules, and logs. | HTTP/SSE server with connection management and configurable operation permissions. |
| [snowflake-mcp](https://github.com/Heapy/snowflake-mcp) | Query Snowflake through MCP and manage multiple connections in a web UI. | Includes query history and a read-only mode. |

## Kotlin libraries and UI

Building blocks for shared code, user interfaces, terminals, and bots.

| Project | What it helps you do | Notes |
| :--- | :--- | :--- |
| [kinetica](https://github.com/Heapy/kinetica) | Build Kotlin UIs as immutable node trees, with browser rendering, server rendering, and headless tests. | Native macOS support is in development; see the platform status in its docs. |
| [kinetica-terminal](https://github.com/Heapy/kinetica-terminal) | Use a shared Kotlin terminal engine with browser rendering and a native macOS terminal app. | Preview; native builds target Apple Silicon, and the browser demo uses local echo. |
| [krogu-time](https://github.com/Heapy/krogu-time) | Move code using the Java 25 `java.time` API to Kotlin Multiplatform. | Targets JVM, Android, and iOS; migration notes document differences. |
| [kotaml](https://github.com/Heapy/kotaml) | Read and write YAML with kotlinx.serialization. | Supported fork of [Charles Korn's kaml](https://github.com/charleskorn/kaml); JVM supported, JS/Wasm highly experimental. |
| [kwasm](https://github.com/Heapy/kwasm) | Explore a WebAssembly runtime whose guest execution can suspend with Kotlin coroutines. | Experimental; not a stable release or a claim of complete WebAssembly conformance. |
| [kotbot](https://github.com/Heapy/kotbot) | Build Telegram bots in Kotlin and see a bot used by the Kotlin community. | Contains the core Bot API library and the community bot implementation. |

## Kotlin Toolchain and build tools

Independent integrations for JetBrains Kotlin Toolchain, plus supporting tools for Kotlin builds. Start with **[ktc-plugins](https://github.com/Heapy/ktc-plugins)** for source plugin installation and **[setup-ktc](https://github.com/Heapy/setup-ktc)** for GitHub Actions. Check each README for its supported toolchain version and targets.

### GitHub Actions

| Project | What it helps you do |
| :--- | :--- |
| [setup-ktc](https://github.com/Heapy/setup-ktc) | Install and cache the Kotlin Toolchain and its dependencies in CI. |
| [ktc-check](https://github.com/Heapy/ktc-check) | Build and run registered checks, with job summaries, failure annotations, and report artifacts. |
| [ktc-publish](https://github.com/Heapy/ktc-publish) | Run checks, prepare signed Maven Central bundles, and publish libraries. |
| [update-ktc](https://github.com/Heapy/update-ktc) | Update toolchain wrappers, validate the build, and open an upgrade pull request. |
| [setup-main-kts](https://github.com/Heapy/setup-main-kts) | Set up Java and Kotlin for scripts, with compiler, dependency, and compiled-script caches. |

### Plugins and integrations

| Project | What it helps you do |
| :--- | :--- |
| [ktc-plugins](https://github.com/Heapy/ktc-plugins) | Install source plugins from GitHub, register them in a project, and track pinned sources in a lockfile. |
| [ktc-ktlint](https://github.com/Heapy/ktc-ktlint) | Check Kotlin style with ktlint and explicitly format sources. |
| [ktc-ktfmt](https://github.com/Heapy/ktc-ktfmt) | Check formatting with ktfmt and explicitly format sources. |
| [ktc-bcv](https://github.com/Heapy/ktc-bcv) | Review public JVM API changes against committed API snapshots. |
| [ktc-kover](https://github.com/Heapy/ktc-kover) | Generate JVM coverage reports and enforce coverage thresholds. |
| [ktc-dokka](https://github.com/Heapy/ktc-dokka) | Generate JVM, Android and Kotlin Multiplatform API documentation and Javadoc archives with Dokka 2.3.0. |
| [ktc-jib](https://github.com/Heapy/ktc-jib) | Build JVM container images and publish them without a Docker daemon. |
| [ktc-sqldelight](https://github.com/Heapy/ktc-sqldelight) | Generate SQLDelight database code and import matching runtime dependency aliases. |
| [ktc-quarkus](https://github.com/Heapy/ktc-quarkus) | Develop and package Quarkus applications, including JVM, native, and container outputs. |
| [ktc-benchmark](https://github.com/Heapy/ktc-benchmark) | Run multiplatform benchmarks on JVM, Native, JavaScript, and WebAssembly. |
| [detekt-config](https://github.com/Heapy/detekt-config) | Share Kotlin analysis rules across Gradle and Kotlin Toolchain builds. Includes a toolchain plugin. |

### Migration and publishing utilities

| Project | What it helps you do |
| :--- | :--- |
| [ktc-to-gradle](https://github.com/Heapy/ktc-to-gradle) | Convert a Kotlin Toolchain project into a Gradle Kotlin DSL build when you need a migration path. |
| [sign-checksum-upload](https://github.com/Heapy/sign-checksum-upload) | Calculate checksums, sign JAR/KLIB artifacts, and upload releases to Maven Central. |
| [repo.kotlin.link](https://github.com/Heapy/repo.kotlin.link) | Proxy Maven artifact requests to configured project repositories through one endpoint. |

## Everyday software

Read more, make information easier to use, and understand what your computer is doing.

| Project | What it helps you do | Notes |
| :--- | :--- | :--- |
| [kotbusta](https://github.com/Heapy/kotbusta) | Browse a personal INPX/FB2 book library, search metadata and content annotations, convert to EPUB, and send books to Kindle. | Web app with optional local semantic search. |
| [kotomka](https://github.com/Heapy/kotomka) | Turn video URLs into readable summaries and notes with key frames, timestamps, transcripts, and PDF export. | Local web service; live processing needs transcription and generation providers. |
| [komok](https://github.com/Heapy/komok) | Explore a life and collaboration assistant aiming to connect information, tasks, and personal workflows. | In development; the README includes goals and planned capabilities. |
| [harmon](https://github.com/Heapy/harmon) | Monitor macOS workloads, group helper processes by app, and understand memory and storage pressure. | Kotlin/Native; Apple Silicon macOS, local process UI, and configurable notifications. |
| [ptkw](https://github.com/Heapy/ptkw) | Explore Portuguese pronunciation learning from typed text and photographed words. | iOS scaffold/prototype using Azure services; setup is required to try it on a device. |

## Infrastructure and home

Small services for containers, local development, home devices, and distribution.

| Project | What it helps you do | Notes |
| :--- | :--- | :--- |
| [kodkod](https://github.com/Heapy/kodkod) | Restart unhealthy Docker containers and recreate selected containers when their image updates. | Opt-in per container through labels. |
| [ddns-fullstack](https://github.com/Heapy/ddns-fullstack) | Keep DNS records in sync with a changing home IP address. | Client/server setup supporting DigitalOcean and Cloudflare DNS. |
| [honeywell-iaq-mqtt](https://github.com/Heapy/honeywell-iaq-mqtt) | Publish Honeywell indoor air quality readings to MQTT for home integrations. | Relies on Honeywell cloud access. |
| [kotlin-dev-proxy](https://github.com/Heapy/kotlin-dev-proxy) | Proxy API requests and serve static files during local web development. | Kotlin and Undertow; an earlier utility. |
| [homebrew-tap](https://github.com/Heapy/homebrew-tap) | Install available Heapy tools through Homebrew. | Formulae and casks; consult each tool's installation instructions. |
| [trmnl-aeropress](https://github.com/Heapy/trmnl-aeropress) | Bring everyday AeroPress recipes to a TRMNL display. | Small display project with minimal documentation. |
| [trmnl-thirty-six-views-of-mount-fuji](https://github.com/Heapy/trmnl-thirty-six-views-of-mount-fuji) | Bring Thirty-six Views of Mount Fuji to a TRMNL display. | Small display project with minimal documentation. |

## Community and learning

| Project | What it helps you do |
| :--- | :--- |
| [awesome-kotlin](https://github.com/Heapy/awesome-kotlin) | Discover Kotlin libraries, tools, articles, and resources through the curated collection at [kotlin.link](https://kotlin.link). |
| [kotlin-telegram](https://github.com/Heapy/kotlin-telegram) | Find information about Kotlin community chats on Telegram. |

## Benchmarks and early projects

Comparisons, focused experiments, and ideas that are still taking shape.

| Project | Purpose | Notes |
| :--- | :--- | :--- |
| [di-comparison](https://github.com/Heapy/di-comparison) | Compare variants of an application using different dependency injection containers. | Benchmark code and recorded results; results depend on the workload and machine. |
| [kotlin-jmh](https://github.com/Heapy/kotlin-jmh) | Collect Kotlin performance experiments using JMH. | Build and source code are present; no top-level README at the directory review date. |
| [java-json-benchmark](https://github.com/Heapy/java-json-benchmark) | Compare JSON serialization and deserialization performance. | Fork of [fabienrenaud/java-json-benchmark](https://github.com/fabienrenaud/java-json-benchmark). |
| [jansi-test](https://github.com/Heapy/jansi-test) | Test Jansi behavior across JDK versions and terminals. | Focused compatibility experiment. |
| [kpress](https://github.com/Heapy/kpress) | Explore a static site generator written in Kotlin. | Early project; its README describes goals and an incomplete example. |
| [koday](https://github.com/Heapy/koday) | Proposed activity tracker for 2026. | Placeholder: only a license file at the review date. |
| [spring-boot-starter-ktor](https://github.com/Heapy/spring-boot-starter-ktor) | Proposed integration of Ktor server and client with Spring Boot. | Proposal only: README and license, no implementation at the review date. |
| [ktor-client-netty](https://github.com/Heapy/ktor-client-netty) | Proposed Netty engine for the Ktor client. | Placeholder: README and license, no implementation at the review date. |

## Earlier work

| Project | Purpose | Status |
| :--- | :--- | :--- |
| [kotlin_jobs](https://github.com/Heapy/kotlin_jobs) | Kotlin job description builder. | No longer maintained according to its README; the repository itself is not marked archived. |
| [heapy.io](https://github.com/Heapy/heapy.io) | Sources for the Heapy website. | Archived on GitHub. |

---

This directory covers all **55 public project repositories** available on **October 8, 2026**. Descriptions were checked against repository metadata and available READMEs; placeholder notes were checked against repository contents. Status notes are a dated snapshot, not a support commitment. Each project defines its own license and compatibility requirements.

The organization profile itself lives in **[Heapy/.github](https://github.com/Heapy/.github)**. [Suggest a correction or add a project](https://github.com/Heapy/.github/issues).
