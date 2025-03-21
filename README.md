# Rust Tauri Monorepo

This is a Rust monorepo containing a Tauri desktop application along with shared Rust crates.

## Project Structure

- **crates/**: Shared Rust crates
  - **common/**: Common utilities and models shared across projects
  - **core/**: Core business logic and services

- **src-tauri/**: Tauri desktop application
  - Consumes the common and core crates

- **src-web/**: Frontend web code (React, Vue, etc.)

## Development

### Prerequisites

- [Rust](https://www.rust-lang.org/tools/install)
- [Node.js](https://nodejs.org/) (for web frontend)
- [Tauri CLI](https://tauri.app/v1/guides/getting-started/prerequisites)

### Building

From the root of the repository:

```bash
# Build all Rust crates
cargo build

# Build and run the Tauri app (from src-tauri directory)
cd src-tauri
cargo tauri dev
```

## Adding New Crates

To add a new crate to the workspace:

1. Create a new directory in the `crates/` folder
2. Initialize a new crate with `cargo new --lib crates/your-crate-name`
3. Add the crate to the workspace members in the root `Cargo.toml`

## License

MIT 