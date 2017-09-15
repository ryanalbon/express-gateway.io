---
layout: doc-section
title: eg plugins install <name>
---

### Description

Installs a plugin

### Usage

```shell
eg plugins install [options] <package>
```
Notes: 
- package is any valid npm link like `ExpressGateway/express-gateway-plugin-example#master`
### Options

| Name, longform | Type      | Default | Description      | Required |
| ---            | ---       | ---     | ---              | ---      |
| `-n, --enable` | `boolean` | `true`  | Enable plugin in system config    | Optional |
| `-g, --update-gateway-config`|`boolean` | `true`  | Update policy whitelist in gateway config| Optional|
| `-o, --option`|   `string`| |Plugin options in the form [-o 'foo=bar']| Optional|

### Examples

#### Install the Example plugin by name (example -> express-gateway-plugin-example)

```shell
$ eg plugin install example
? Set value for baseUrl: http://example.com
? Set value for maxRequestsPerSecond: 234
? Would you like to enable this plugin in system config? Yes
? Would you like to add new policies to gateway config? Yes
Plugin installed!
```

#### Install the Example plugin from github 

```shell
eg plugin install ExpressGateway/express-gateway-plugin-example
? Set value for baseUrl: http://example.com
? Set value for maxRequestsPerSecond: 234
? Would you like to enable this plugin in system config? Yes
? Would you like to add new policies to gateway config? Yes
Plugin installed!
```