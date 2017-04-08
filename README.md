# Melbourne CocoaHeads Events API Spec

## Online Documentation

Documentation is available at http://docs.melbournecocoaheads.apiary.io

## Tests

You can test the production api against the swagger.yml file using the [dredd][2] tool. Dredd is setup as a dependency in the `package.json`. A compatible node version is specified for [nvm][3] in the `.nvmrc` file.

```
npm run test
```

## Swift Code Generation

This project relies on [swagger-codegen][1] which can be installed with homebrew on macOS to generate a swift3 api client.

```
swagger-codegen generate -i swagger.yaml -l swift3 -o ApiClient
```


[1]: https://github.com/swagger-api/swagger-codegen
[2]: https://dredd.readthedocs.io
[3]: https://github.com/creationix/nvm