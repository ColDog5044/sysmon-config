# sysmon-config | A Sysmon configuration file

This is a forked and modified version of [@SwiftOnSecurity's](https://twitter.com/SwiftOnSecurity) [sysmon config](https://github.com/SwiftOnSecurity/sysmon-config) and
a modified version of Neo23x0's [sysmon blocking config](https://github.com/Neo23x0/sysmon-config). This includes all pull requests, updated schema, and additional blocking rules.

## Maintainers of this Fork

- Collin Laney @ColDog5044

## Maintainers of Neo23x0 Fork

- Florian Roth @Neo23x0
- Tobias Michalski @humpalum
- Christian Burkard @phantinuss
- Nasreddine Bencherchali @nas_bench

## Additional coverage includes

- Cobalt Strike named pipes
- PrinterNightmare
- HiveNightmare

## Configs in this Repository

This repo includes the original and two additional configurations

- `sysmonconfig-export.xml` the original config provided by @SwiftOnSecurity
- `sysmonconfig-export-block.xml` the original config provided by @SwiftOnSecurity with some basic blocking rules usable since Sysmon v14 (WARNING: use it with care!)
- `sysmonconfig-trace.xml` a config by @Cyb3rWard0g that logs just everything with a few examples for debugging or threat research purposes

## Other Sysmon Configs

- Olaf Hartong's [Sysmon Modular](https://github.com/olafhartong/sysmon-modular) - modular Sysmon config for easier maintenance and generation of specific configs

## Testing

Please report:

1. Expressions that cause a high volume of events
2. Broken configuration elements (typos, wrong conditions)
3. Missing coverage (preferrably as a pull request)

## Usage

### Install

Run with administrator rights

```cmd
sysmon64.exe -accepteula -i sysmonconfig-export.xml
```

### Update existing configuration

Run with administrator rights

```cmd
sysmon64.exe -c sysmonconfig-export.xml
```

### Uninstall

Run with administrator rights

```cmd
sysmon64.exe -u
```
