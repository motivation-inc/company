# Code Standards

## Rust
For Rust, the formatting provided by rustfmt is followed. Use `cargo fmt` on any code before pushing changes. 

Additionally, clippy can be used to further structure code, although it is not required.

## Python

Python code should follow a consistent, modular, and data-driven style oriented toward building reusable tools and systems rather than one-off scripts.

### General Style

- Prefer small, focused helper functions over large monolithic functions.
- Keep functions single-purpose and easy to compose.
- Use clear and explicit logic rather than overly abstract or “clever” patterns.
- Avoid unnecessary complexity; favor readability and maintainability.

### Structure & Organization

**Organize code into:**

- Utility/helper functions
- Core logic (classes or main functions)
- Higher-level orchestration

**Separate concerns between:**

- Data extraction/parsing
- Transformation/processing
- Execution/side effects

### Functional Patterns

- Use helper functions for reusable operations (e.g., property access, conversions).
- Prefer deterministic outputs with minimal hidden state.
- Keep nesting shallow and return early when appropriate.

### Object-Oriented Design

- Use classes when modeling entities with shared behavior.
- Favor shallow inheritance hierarchies.
- Base classes should define shared behavior; subclasses extend rather than complicate.
- Avoid over-abstraction or deep polymorphism unless clearly beneficial.

### Data Handling
Prefer data-driven designs:

- Use dictionaries, lists, and simple structures to represent events or state.
- Avoid hardcoding behavior where configuration/data-driven approaches suffice.

Pass configuration explicitly via parameters rather than relying on global state.

### Type Specifications
Use type hinting where possible.

- Add type hints on function definitions and return values.
- Keep object types consistent (e.g., `my_favorite_number` should be an integer, and never flip to a string type.)  

### Dynamic / Reflection Usage
It is acceptable to use dynamic attribute access (`getattr`, `setattr`) when:

- It simplifies interaction with external APIs or frameworks
- It enables flexible property addressing

When used, encapsulate this behavior inside helper functions.

### Naming Conventions

- Use descriptive, intention-revealing names.
- Functions should read like actions (e.g., `get_*`, `set_*`, `generate_*`).
- Classes should represent clear conceptual entities.

### Error Handling

- Use `try/except` for expected failure points (e.g., file loading).
- Fail early when critical assumptions are not met.
- Avoid excessive or overly defensive error handling.

### External Integration (Any API)

- Wrap external API interactions in helper functions to isolate complexity.
- Avoid scattering direct API calls throughout the codebase.
- Treat external systems as boundaries and keep your core logic independent where possible.

### Formatting

- Follow PEP 8 conventions where applicable.
- Use consistent indentation, spacing, and import organization.
- Keep code clean and readable without unnecessary stylistic deviation.

