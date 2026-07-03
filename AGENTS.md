# AGENTS.md

## Cursor Cloud specific instructions

This repository is a minimal **Apache Maven** skeleton project (`org.example:mydata1:1.0-SNAPSHOT`). It currently contains only `pom.xml` files (root and `mydata1/`) with **no `src/` source code and no tests**, so builds produce an empty jar (`target/mydata1-1.0-SNAPSHOT.jar`) and emit a harmless `WARNING: JAR will be empty` message. There is no runnable/long-running application (no main class, no server) — the "application" is the Maven build lifecycle itself.

### Tooling
- Java: OpenJDK **21** (`/usr/bin/java`).
- Maven: **3.8.7** (`mvn`, installed system-wide). If `mvn` is ever missing, install it with `sudo apt-get install -y maven`.

### Common commands (run from repo root `/workspace`)
- Validate: `mvn validate`
- Lint/verify: `mvn verify` (no linter plugins are configured, so this only runs the standard lifecycle)
- Test: `mvn test` (prints `No tests to run.`)
- Build: `mvn package` (produces the jar under `target/`)

### Notes
- First build downloads Maven plugins/dependencies from Maven Central (network required). The update script pre-warms these via `mvn dependency:go-offline`.
- The empty-jar warning is expected until real source code is added under `src/main/java`.
