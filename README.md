# Melbourne CocoaHeads Events API Spec

## Online Documentation

Documentation is available at http://docs.melbournecocoaheads.apiary.io

## Tests

You can test the production api against the swagger.yml file using the [dredd][2] tool. Dredd is setup as a dependency in the `package.json`. A compatible node version is specified for [nvm][3] in the `.nvmrc` file.

```zsh
$ nvm use
# Found '/.../events-api-spec/.nvmrc' with version <v6.10>
# Now using node v6.10.1 (npm v3.10.10)

$ npm i

$ npm run test

# pass: GET /api/events duration: 2061ms
# complete: 1 passing, 0 failing, 0 errors, 0 skipped, 1 total
# complete: Tests took 2065ms
```

## Swift Code Generation

This project relies on [swagger-codegen][1] which can be installed with homebrew on macOS to generate a swift3 api client.

```
swagger-codegen generate -i swagger.yaml -l swift3 -o ApiClient
```


[1]: https://github.com/swagger-api/swagger-codegen
[2]: https://dredd.readthedocs.io
[3]: https://github.com/creationix/nvm