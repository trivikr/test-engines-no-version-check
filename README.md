# test-engines-node-version-check

Tests experience for deprecated Node.js versions in package managers using engines field.

## With engines field

Testing with Node.js version `v8.11.3`

```console
$ node --version
v8.11.3
```

### npm

The package installation succeeds, as engine-strict is not defined.

```console
$ npm --version
5.6.0

$ npm install test-engines-node-version-check@0.0.2
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN test-warning@1.0.0 No description
npm WARN test-warning@1.0.0 No repository field.

+ test-engines-node-version-check@0.0.2
added 1 package in 0.725s
```

### yarn

The package installation fails.

```console
$ yarn --version
1.22.10

$ yarn add test-engines-node-version-check@0.0.2
yarn add v1.22.10
info No lockfile found.
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
error test-engines-node-version-check@0.0.2: The engine "node" is incompatible with this module. Expected version ">=10.0.0". Got "8.11.3"
error Found incompatible module.
info Visit https://yarnpkg.com/en/docs/cli/add for documentation about this command.
```

### pnpm

The package installation succeeds, as engine-strict is not defined.

```console
$ pnpm --version
3.8.1

$ pnpm add test-engines-node-version-check@0.0.2
Already up-to-date
Resolving: total 1, reused 0, downloaded 1, done

dependencies:
+ test-engines-node-version-check 0.0.2
```

## With engines field and engineStrict=true

Testing with Node.js version `v8.11.3`

```console
$ node --version
v8.11.3
```

### npm

The package installation succeeds, as engine-strict is not defined.

```console
$ npm --version
5.6.0

$ npm install test-engines-node-version-check@0.1.1
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN test-warning@1.0.0 No description
npm WARN test-warning@1.0.0 No repository field.

+ test-engines-node-version-check@0.1.1
added 1 package in 0.796s
```

### yarn

The package installation fails.

```console
$ yarn --version
1.22.10

$ yarn add test-engines-node-version-check@0.1.1
yarn add v1.22.10
info No lockfile found.
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
error test-engines-node-version-check@0.1.1: The engine "node" is incompatible with this module. Expected version ">=10.0.0". Got "8.11.3"
error Found incompatible module.
info Visit https://yarnpkg.com/en/docs/cli/add for documentation about this command.
```

### pnpm

The package installation succeeds, as engine-strict is not defined.

```console
$ pnpm --version
3.8.1

$ pnpm add test-engines-node-version-check@0.1.1
Already up-to-date
Resolving: total 1, reused 0, downloaded 1, done

dependencies:
+ test-engines-node-version-check 0.1.1
```

## Supported Node.js version `v10.24.0`

```console
$ node --version
v10.24.0
```

### npm

The package installation succeeds.

```console
$ npm --version
6.14.11

$ npm install test-engines-node-version-check@0.0.2
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN test-warning@1.0.0 No description
npm WARN test-warning@1.0.0 No repository field.

+ test-engines-node-version-check@0.0.2
added 1 package from 1 contributor and audited 1 package in 0.544s
found 0 vulnerabilities
```

### yarn

The package installation succeeds.

```console
$ yarn --version
1.22.10

$ yarn add test-engines-node-version-check@0.0.2
yarn add v1.22.10
info No lockfile found.
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...

success Saved lockfile.
success Saved 1 new dependency.
info Direct dependencies
└─ test-engines-node-version-check@0.0.2
info All dependencies
└─ test-engines-node-version-check@0.0.2
✨  Done in 0.28s.
```

### pnpm

The package installation succeeds.

```console
$ pnpm --version
5.18.9

$ pnpm add test-engines-node-version-check@0.0.2
Packages: +1
+
Packages are hard linked from the content-addressable store to the virtual store.
  Content-addressable store is at: /Users/trivikr/.pnpm-store/v3
  Virtual store is at:             node_modules/.pnpm
Progress: resolved 1, reused 0, downloaded 1, added 1, done

dependencies:
+ test-engines-node-version-check 0.0.2
```
