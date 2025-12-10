# Getting Started

Install the package using npm:

```
npm install --save @watts-ai/cli.ts
```

or if you use Yarn:

```
yarn add @watts-ai/cli.ts
```

## Using `@watts-ai/cli.ts`

All the interesting stuff is exported from the main module. Try writing the following app:

```ts
import { command, run, string, positional } from '@watts-ai/cli.ts';

const app = command({
  name: 'my-first-app',
  args: {
    someArg: positional({ type: string, displayName: 'some arg' }),
  },
  handler: ({ someArg }) => {
    console.log({ someArg });
  },
});

run(app, process.argv.slice(2));
```

This app is taking one string positional argument and prints it to the screen. Read more about the different parsers and combinators in [Parsers and Combinators](./parsers.md).

> **Note:** `string` is one type that comes included in `@watts-ai/cli.ts`. There are more of these bundled in the [included types guide](./included_types.md). You can define your own types using the [custom types guide](./custom_types.md)
