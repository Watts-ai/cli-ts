# URL Battery Pack

The URL battery pack contains the following types:

### `Url`

```typescript
import { Url } from '@watts-ai/cli.ts/batteries/url';
```

Resolves into a `URL` class. Fails if there is no `host` or `protocol`.

### `HttpUrl`

```typescript
import { HttpUrl } from '@watts-ai/cli.ts/batteries/url';
```

Resolves into a `URL` class. Fails if the protocol is not `http` or `https`
