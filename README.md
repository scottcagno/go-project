# Go Project Starter

Simple "empty" project for use with medium to large golang projects.

### `/cmd`

Main applications for this project. The directory name for each application should match the name of the executable you want to have (e.g., `/cmd/myapp`).

It's common to have a small `main` function that imports and invokes the code from the `/internal` and `/pkg` directories and nothing else.

See [`/cmd`](cmd/README.md) for more details.

### `/internal`

Private application and library code. This is the code you don't want others importing in their applications or libraries. Note that this layout pattern is enforced by the Go compiler itself. See the Go 1.4 [`release notes`](https://golang.org/doc/go1.4#internalpackages) for more details. Note that you are not limited to the top level `internal` directory. You can have more than one `internal` directory at any level of your project tree.

See [`/internal`](internal/README.md) for more details.

### `/pkg`

Library code that's ok to use by external applications (e.g., `/pkg/mypubliclib`). Other projects will import these libraries expecting them to work, so think twice before you put something here :-) Note that the `internal` directory is a better way to ensure your private packages are not importable because it's enforced by Go. The `/pkg` directory is still a good way to explicitly communicate that the code in that directory is safe for use by others.

See [`/pkg`](pkg/README.md) for more details.

### `/api`

OpenAPI/Swagger specs, JSON schema files, protocol definition files, etc.

See [`/api`](api/README.md) for more details.

### `/web`

Web application specific components.

See [`/web`](web/README.md) for more details.

### `/scripts`

Scripts to perform various build, install, analysis, etc.

See [`/scripts`](scripts/README.md) for more detials.

### `/docs`

Design and user documents.

See [`/docs`](docs/README.md) for more details.

### `/tools`

Supporting tools for this project.

See the [`/tools`](tools/README.md) for more details.
