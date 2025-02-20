Here's how to publish a new version of your private npm package:

Make sure your working tree is empty (publish your changes to git) before starting.

1. First, make sure you're logged in to npm:
```bash
npm login
```

2. Update the version number in your `package.json` file. You can do this manually or use one of these commands:
```bash
npm version patch  # for bug fixes (1.0.0 -> 1.0.1)
npm version minor  # for new features (1.0.0 -> 1.1.0)
npm version major  # for breaking changes (1.0.0 -> 2.0.0)
```

3. Then publish the package:
```bash
npm publish
```

Since it's a private package (starts with @), make sure:
- You're a member of the organization (@eml-henn)
- The `package.json` has the `"private": true` field
- You have the proper scope access

If you get any errors about access, you might need to add the access flag:
```bash
npm publish --access private
```

Remember to commit and push your changes to your version control system (like git) after publishing.