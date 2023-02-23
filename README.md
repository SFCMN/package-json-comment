# package-json-comment

This package is used to add comments in `package.json`.

## Background

In the past, in order to solve the security vulnerabilities of some dependent packages, I had to upgrade some dependent package versions.


However, the upgrade work is not easy, and various version conflicts, missing configurations, breaking changes and other issues are often encountered.


And in order to solve such issues, I have to change some configurations or add additional packages.


If the configuration file is a `.js` file, then I can add comments to it so that it can be optimized in the future. However, in `package.json`, I cannot directly add comments. But without the slightest explanation, some third-party packages introduced to solve existing issues may become dead packages that no one dares to remove, which is not what I expected.


So, taking advantage of some features of the `package.json` file, I made this empty package.

## Usage

In order to add comments to the `.json` file without introducing additional workload, my suggestion is to add a field directly and use the value of the field as the comment content.

And, in order to avoid npm errors, the field name uses `package-json-comment`, which is the name of this package.

You just need to add this package:

```bash
npm install --save-dev package-json-comment
```

Then, you can add comment in `package.json` file, the following is an example:

```json
{
  "name": "package-json-comment",
  "version": "0.2.0",
  "description": "This package is used to add comments in package.json",
  "repository": {
    "type": "git",
    "url": "git+https://github.com/quezhongxian/package-json-comment.git"
  },
  "keywords": [
    "package.json",
    "comment"
  ],
  "author": {
    "email": "wsfcmn@163.com",
    "name": "SFCMN"
  },
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/quezhongxian/package-json-comment/issues"
  },
  "homepage": "https://github.com/quezhongxian/package-json-comment#readme",
  "package-json-comment": "This is a comment",
  "scripts": {
    "lint": "eslint --ext .js .",
    "package-json-comment": "This is a comment"
  },
  "devDependencies": {
    "eslint": "^8.34.0",
    "eslint-config-airbnb-base": "^15.0.0",
    "eslint-plugin-import": "^2.27.5",
    "package-json-comment": "^0.2.0",
    "package-json-comment": "This is a comment"
  },
  "dependencies": {
    "package-json-comment": "This is a comment"
  }
}

```
