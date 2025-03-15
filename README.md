# Lib Template

A reusable template library for creating standardized components and structures.

## Installation

```bash
npm install @santosl2/lib-template
# or
yarn add @santosl2/lib-template
# or
pnpm add @santosl2/lib-template
```

## Features

- Template components and structures
- Written in TypeScript
- Easy to use and integrate
- Standardized patterns
- Automated testing
- Continuous integration on GitHub Actions (Only when release is published)

## Development

To build the project:

```bash
npm run build
```

## Package.json Configuration

Before using this library, make sure to update the following fields in your `package.json`:

```json
{
  "name": "your-project-name",
  "version": "1.0.0",
  "repository": {
    "type": "git",
    "url": "git+https://github.com/yourusername/your-project-name.git"
  }
}
```

Replace `your-project-name` and `yourusername` with your actual project name and GitHub username.

## Configuring npm to use GitHub Packages

To use GitHub Packages with npm, you need to:

1. Add a `.npmrc` file to the root of your project with the following content:

```
//npm.pkg.github.com/:_authToken=${GITHUB_TOKEN}
```

2. Create a GitHub personal access token (PAT):

- Go to GitHub Settings > Developer settings > Personal access tokens
- Generate a new token with the `write:packages` scope
- Copy the token and set it as an environment variable named `GITHUB_TOKEN` or replace `${GITHUB_TOKEN}` with the actual token in the `.npmrc` file

This configuration allows npm to authenticate with GitHub Packages when installing or publishing packages.

## Publishing Your Package

### Publish Your Package

Now, let's publish the package to GitHub Packages. Run the following command:

```bash
npm publish --registry=https://npm.pkg.github.com
```

If everything is set up correctly, your package will be published to GitHub Packages and available for others to install.

## Automated Publishing

This project is configured with a CI/CD pipeline that automatically publishes the library to npm whenever a new release is created on GitHub. To trigger an automated deployment:

1. Create a new release on GitHub
2. Tag it with a semantic version (e.g., v1.0.0)
3. Add release notes
4. Publish the release

The GitHub Actions workflow will handle the rest, making the updated package available on npm without manual intervention.

## License

MIT © [Santosl2](https://github.com/Santosl2)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Authors

- **Santosl2** - [GitHub Profile](https://github.com/Santosl2)
