# Design Tokens Repository

This repository contains design tokens exported from Figma using Tokens Studio, structured for use with Style Dictionary.

## About This Repository

This is a dedicated repository for storing and versioning design tokens separate from implementation code. It serves as a single source of truth for design tokens across projects.

## Repository Structure

```
design-tokens/
├── tokens.json       # Main tokens file exported from Tokens Studio
├── README.md
└── CHANGELOG.md      # Optional: Document token changes
```

## Usage

### Direct Usage

This repository is intended to be consumed by projects that process design tokens with tools like Style Dictionary.

### Reference Implementation

For a complete implementation of how these tokens can be used in a React component library, see the [Reference Component Library](https://github.com/camcavers/reference-component-library) project.

The reference implementation demonstrates:
- Importing tokens from this repository
- Processing them with Style Dictionary
- Using them in React components

## Integration

To use these tokens in your project, you can:

1. **Clone or download** this repository and copy the tokens
2. **Submodule** this repository into your project
3. **Fetch directly** from this repository in your build process

### Example Integration Script

The Reference Component Library includes a script to fetch tokens directly from this repository:

```bash
# Basic usage
npm run fetch-tokens https://github.com/username/design-tokens.git

# Using a specific branch 
npm run fetch-tokens https://github.com/username/design-tokens.git develop

# Using a custom file path
npm run fetch-tokens https://github.com/username/design-tokens.git main path/to/tokens.json
```

## Token Updates

When design changes occur in Figma:

1. Export new tokens from Tokens Studio
2. Commit them to this repository
3. Create a new version tag if needed
4. Projects consuming these tokens can then update

## Contribution Guidelines

1. **Do not** manually edit token files - they should be exported directly from Tokens Studio
2. Always include a descriptive commit message
3. Consider tagging significant changes with semantic versioning
4. Document breaking changes in CHANGELOG.md

## License

MIT