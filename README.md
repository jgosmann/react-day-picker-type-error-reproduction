# react-day-picker type error reproduction

See https://github.com/gpbl/react-day-picker/issues/2563

To reproduce:

1. Clone this repository.
2. `npm install`
3. `npx tsc`

You'll get the following type error:

```
node_modules/react-day-picker/dist/esm/formatters/formatMonthDropdown.d.ts:12:17 - error TS2307: Cannot find module 'date-fns/locale/types.js' or its corresponding type declarations.

12 locale?: import("date-fns/locale/types.js").Locale): string;
                   ~~~~~~~~~~~~~~~~~~~~~~~~~~


Found 1 error in node_modules/react-day-picker/dist/esm/formatters/formatMonthDropdown.d.ts:12
```

This only happens from react-day-picker 9.2.0 onwards.
