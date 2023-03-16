# GBFS-LD GitHub action workflow

built with `3.2.7`

[GBFS-LD workflow](./github/workflows/gbfs-ld.yml) is a CI/CD pipeline to convert GBFS JSON Schemas to RDF vocabulary and Shacl shapes using [jsc-ld package](https://www.npmjs.com/package/jsc-ld).

## Prerequisite

```
GBFS-LD/
├── Version
├── configs/
│   └── config.json
├── v2.2/
│   └── JSC-LD/
│       ├── free-bike_status.json
│       ├── gbfs.json
│       └── ...
└── v2.3/
    └── JSC-LD/
        ├── free-bike_status.json
        ├── gbfs.json
        └── ...

```
- JSON Schema files with [JSC-LD annotation](https://github.com/jiaoxlong/jsc-ld-spec/blob/main/build/html/jsc_ld_syntax.html) if needed.
- JSC-LD configuration ./configs/config.json
- a Version file contains GBFS versions to be converted. 
```
cat ./GBFS-LD/Version
v2.3
v2.2
```

## Workflow steps

1. allocate GitHub server
2. install nodejs 
3. install and run jsc-ld
4. push back the changes to the repository.




