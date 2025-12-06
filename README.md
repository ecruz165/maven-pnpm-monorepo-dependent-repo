# Dependent Service

This service depends on `demo-module-a` from the [maven-pnpm-monorepo](https://github.com/ecruz165/maven-pnpm-monorepo) project.

## Dependencies

- **demo-module-a** (0.0.1-SNAPSHOT) - From GitHub Packages
- Spring Boot 3.5.8
- Spring WebFlux

## Setup

### 1. Configure Maven Settings

Add GitHub authentication to `~/.m2/settings.xml`:

```xml
<settings>
  <servers>
    <server>
      <id>github</id>
      <username>YOUR_GITHUB_USERNAME</username>
      <password>YOUR_GITHUB_TOKEN</password>
    </server>
  </servers>
</settings>
```

**GitHub Token Scopes Required:**
- `read:packages` - Download packages from GitHub Packages

### 2. Build

```bash
mvn clean install
```

## Dependency Information

The `demo-module-a` dependency is resolved from:
```
https://maven.pkg.github.com/ecruz165/maven-pnpm-monorepo
```

**Current Version:** 0.0.1-SNAPSHOT

This version is automatically updated when new versions are published to the maven-pnpm-monorepo.
