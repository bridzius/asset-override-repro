# Asset configuration override.


## Reproduction

1. `npm ci`
2. `npx ng build --configuration development`
3. See `dist/hello-world/assets/empty-file.txt`
4. `npx ng build --configuration production`
5. Expectation: basi configuration should be merged and `dist/hello-world/assets/empty-file.txt` should exist since it's defined in base config.
6. Actual: production configuration fully overrides the base config and only `dist/hello-world/folder/folder.txt` is available.