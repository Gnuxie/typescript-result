<!--
SPDX-FileCopyrightText: 2024 Gnuxie <Gnuxie@protonmail.com>

SPDX-License-Identifier: CC-BY-SA-4.0
-->

# Typescript result

This is just a simple result type so that we can have type checked error
handling pretty please.

This allows you to do cool stuff like this:

```typescript
const result = await api.getCatPictures();
if (isError(result)) {
  // forced to handle error here before we can access `result.ok`.
  displayError(`We couldn't get the cat pictures`, result.error);
  return;
}
displayCats(result.ok);
```
