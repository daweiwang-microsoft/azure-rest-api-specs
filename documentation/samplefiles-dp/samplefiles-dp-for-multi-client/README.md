# [[ServiceName]]

> see https://aka.ms/autorest

This is the AutoRest configuration file for [[ServiceName]].

## Getting Started

To build the SDKs for My API, simply install AutoRest via `npm` (`npm install -g autorest`) and then run:

> `autorest readme.md`

To see additional help and options, run:

> `autorest --help`

For other options on installation see [Installing AutoRest](https://aka.ms/autorest/install) on the AutoRest github page.

---

## Configuration

### Basic Information

These are the global settings for the [[ServiceName]].

```yaml
openapi-type: [[OpenApiType]]
tag: package-[[Version]]
security: AADToken
security-scopes: [[SecurityScopes]]
```

```yaml && $(package-A)
title: [[Title_A]]
package-A-tag: package-A-[[Version]]
```

```yaml && $(package-B)
title: [[Title_B]]
package-B-tag: package-B-[[Version]]
```

### Tag: package-[[Version]]

These settings apply only when `--tag=package-[[Version]]` is specified on the command line.

```yaml $(tag) == 'package-[[Version]]'
input-file:
  - Microsoft.YourServiceName/stable/YYYY-MM-DD/YourServiceNameA.json
  - Microsoft.YourServiceName/stable/YYYY-MM-DD/YourServiceNameB.json
```

### Tag: package-A-[[Version]]

These settings apply only when `--package-A-tag=package-A-[[Version]]` is specified on the command line.

```yaml $(package-A-tag) == 'package-A-[[Version]]'
input-file:
  - Microsoft.YourServiceName/stable/YYYY-MM-DD/YourServiceNameA.json
```

### Tag: package-B-[[Version]]

These settings apply only when `--package-B-tag=package-B-[[Version]]` is specified on the command line.

```yaml $(package-B-tag) == 'package-B-[[Version]]'
input-file:
  - Microsoft.YourServiceName/stable/YYYY-MM-DD/YourServiceNameB.json
```

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

```yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-net-track2
```