Shows issue with @types/copy-webpack-plugin

Run `npm run build`

There are type errors because of the dependency on `@types/webpack`, which don't match webpack v5.

```
> copy-webpack-plugin-types-typescript-test@1.0.0 build /Users/jonstich/dev/copy-webpack-plugin-types
> tsc

node_modules/@types/webpack/index.d.ts:32:3 - error TS2305: Module '"../../tapable/tapable"' has no exported member 'Tapable'.

32   Tapable,
     ~~~~~~~

node_modules/@types/webpack/index.d.ts:1062:23 - error TS2707: Generic type 'SyncWaterfallHook<T, AdditionalOptions>' requires between 1 and 2 type arguments.

1062             resolver: SyncWaterfallHook;
                           ~~~~~~~~~~~~~~~~~

node_modules/@types/webpack/index.d.ts:1063:22 - error TS2707: Generic type 'SyncWaterfallHook<T, AdditionalOptions>' requires between 1 and 2 type arguments.

1063             factory: SyncWaterfallHook;
                          ~~~~~~~~~~~~~~~~~

node_modules/@types/webpack/index.d.ts:1064:28 - error TS2707: Generic type 'AsyncSeriesWaterfallHook<T, AdditionalOptions>' requires between 1 and 2 type arguments.

1064             beforeResolve: AsyncSeriesWaterfallHook;
                                ~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@types/webpack/index.d.ts:1065:27 - error TS2707: Generic type 'AsyncSeriesWaterfallHook<T, AdditionalOptions>' requires between 1 and 2 type arguments.

1065             afterResolve: AsyncSeriesWaterfallHook;
                               ~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@types/webpack/index.d.ts:1066:27 - error TS2707: Generic type 'SyncBailHook<T, R, AdditionalOptions>' requires between 2 and 3 type arguments.

1066             createModule: SyncBailHook;
                               ~~~~~~~~~~~~
```