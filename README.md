# etc-shared-biome-rules

A shared configuration package for [Biome](https://biomejs.dev/), designed to provide consistent linting and formatting rules for React projects. This package helps you enforce best practices and maintain code quality across multiple repositories.

## Installation

```bash
npm install etc-shared-biome-rules
# or
yarn add etc-shared-biome-rules
# or
pnpm add etc-shared-biome-rules
```

Replace `etc-shared-biome-rules` with the actual name of this package (e.g., `etc-shared-biome-rules`).

## Usage

To use the shared rules in your project, extend the configuration in your `biome.json` or `biome.jsonc` file:

```json
{
  "extends": ["etc-shared-biome-rules/react"]
}
```

This will apply all the linting and formatting rules defined in the shared configuration for React projects.

## How It Works

- The package exports a Biome configuration for React projects at `rules/react/biome.jsonc`.
- It enables recommended rules and some custom rules for accessibility, correctness, style, and sorting classes.
- The configuration can be extended or overridden in your project's own `biome.json` or `biome.jsonc`.

## Customization

You can further customize the rules in your own configuration file by overriding specific rules after extending this package:

```json
{
  "extends": ["etc-shared-biome-rules/react"],
  "linter": {
    "rules": {
      "style": {
        "noParameterAssign": "error"
      }
    }
  }
}
```

## Example

1. Install Biome and the shared config:

   ```bash
   pnpm add --save-dev --save-exact @biomejs/biome
   pnpm add etc-shared-biome-rules -D
   ```

2. Create or update your `biome.json`:

   ```json
   {
     "extends": ["etc-shared-biome-rules/react"]
   }
   ```

3. Run Biome:

   ```bash
   npx biome check .
   ```

## License

MIT
