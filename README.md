# no-orm

This package aims to make sql queries type safe and easy to build dynamically with expresive api

```typescript
import { query } from 'no-orm';

interface IRawA { id: string; foo: string; }

const findA = query<IRawA, { id: string }>`
SELECT id, foo FROM public.a
WHERE id = ${'id'};
`;
```