<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please do not update manually -->
# gitleaks [![GitHub last commit](https://img.shields.io/github/last-commit/zricethezav/gitleaks)](https://github.com/zricethezav/gitleaks/commits)

## gitleaks documentation

- Version in MegaLinter: **8.12.0**
- Visit [Official Web Site](https://github.com/zricethezav/gitleaks#readme){target=_blank}
- See [How to configure gitleaks rules](https://github.com/zricethezav/gitleaks#configuration){target=_blank}
  - If custom `.gitleaks.toml` config file is not found, [.gitleaks.toml](https://github.com/oxsecurity/megalinter/tree/main/TEMPLATES/.gitleaks.toml){target=_blank} will be used
- See [How to ignore files and directories with gitleaks](https://github.com/zricethezav/gitleaks#configuration){target=_blank}

[![gitleaks - GitHub](https://gh-card.dev/repos/zricethezav/gitleaks.svg?fullname=)](https://github.com/zricethezav/gitleaks){target=_blank}

## Configuration in MegaLinter

- Enable gitleaks by adding `REPOSITORY_GITLEAKS` in [ENABLE_LINTERS variable](https://oxsecurity.github.io/megalinter/beta/configuration/#activation-and-deactivation)
- Disable gitleaks by adding `REPOSITORY_GITLEAKS` in [DISABLE_LINTERS variable](https://oxsecurity.github.io/megalinter/beta/configuration/#activation-and-deactivation)

| Variable                                        | Description                                                                         | Default value                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------|
| REPOSITORY_GITLEAKS_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`            |                                                 |
| REPOSITORY_GITLEAKS_PRE_COMMANDS                | List of bash commands to run before the linter                                      | None                                            |
| REPOSITORY_GITLEAKS_POST_COMMANDS               | List of bash commands to run after the linter                                       | None                                            |
| REPOSITORY_GITLEAKS_CONFIG_FILE                 | gitleaks configuration file name</br>Use `LINTER_DEFAULT` to let the linter find it | `.gitleaks.toml`                                |
| REPOSITORY_GITLEAKS_RULES_PATH                  | Path where to find linter configuration file                                        | Workspace folder, then MegaLinter default rules |
| REPOSITORY_GITLEAKS_DISABLE_ERRORS              | Run linter but consider errors as warnings                                          | `false`                                         |
| REPOSITORY_GITLEAKS_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                    | `0`                                             |

## MegaLinter Flavours

This linter is available in the following flavours

|                                                                         <!-- -->                                                                         | Flavor                                                                               | Description                                                            | Embedded linters |                                                                                                                                                                                                   Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|:----------------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://oxsecurity.github.io/megalinter/beta/supported-linters/)               | Default MegaLinter Flavor                                              |       107        |                             ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |
|      <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/ci_light.ico" alt="" height="32px" class="megalinter-icon"></a>       | [ci_light](https://oxsecurity.github.io/megalinter/beta/flavors/ci_light/)           | Optimized for CI items (Dockerfile, Jenkinsfile, JSON/YAML schemas,XML |        20        |           ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-ci_light/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-ci_light) |
|    <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/documentation.ico" alt="" height="32px" class="megalinter-icon"></a>    | [documentation](https://oxsecurity.github.io/megalinter/beta/flavors/documentation/) | MegaLinter for documentation projects                                  |        46        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-documentation/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-documentation) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/dotnet.ico" alt="" height="32px" class="megalinter-icon"></a>        | [dotnet](https://oxsecurity.github.io/megalinter/beta/flavors/dotnet/)               | Optimized for C, C++, C# or VB based projects                          |        55        |               ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-dotnet/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-dotnet) |
|         <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/go.ico" alt="" height="32px" class="megalinter-icon"></a>          | [go](https://oxsecurity.github.io/megalinter/beta/flavors/go/)                       | Optimized for GO based projects                                        |        48        |                       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-go/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-go) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/java.ico" alt="" height="32px" class="megalinter-icon"></a>         | [java](https://oxsecurity.github.io/megalinter/beta/flavors/java/)                   | Optimized for JAVA based projects                                      |        49        |                   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-java/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-java) |
|     <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/javascript.ico" alt="" height="32px" class="megalinter-icon"></a>      | [javascript](https://oxsecurity.github.io/megalinter/beta/flavors/javascript/)       | Optimized for JAVASCRIPT or TYPESCRIPT based projects                  |        55        |       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-javascript/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-javascript) |
|         <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/php.ico" alt="" height="32px" class="megalinter-icon"></a>         | [php](https://oxsecurity.github.io/megalinter/beta/flavors/php/)                     | Optimized for PHP based projects                                       |        50        |                     ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-php/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-php) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/python.ico" alt="" height="32px" class="megalinter-icon"></a>        | [python](https://oxsecurity.github.io/megalinter/beta/flavors/python/)               | Optimized for PYTHON based projects                                    |        56        |               ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-python/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-python) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/ruby.ico" alt="" height="32px" class="megalinter-icon"></a>         | [ruby](https://oxsecurity.github.io/megalinter/beta/flavors/ruby/)                   | Optimized for RUBY based projects                                      |        47        |                   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-ruby/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-ruby) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/rust.ico" alt="" height="32px" class="megalinter-icon"></a>         | [rust](https://oxsecurity.github.io/megalinter/beta/flavors/rust/)                   | Optimized for RUST based projects                                      |        47        |                   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-rust/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-rust) |
|     <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/salesforce.ico" alt="" height="32px" class="megalinter-icon"></a>      | [salesforce](https://oxsecurity.github.io/megalinter/beta/flavors/salesforce/)       | Optimized for Salesforce based projects                                |        49        |       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-salesforce/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-salesforce) |
|      <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/security.ico" alt="" height="32px" class="megalinter-icon"></a>       | [security](https://oxsecurity.github.io/megalinter/beta/flavors/security/)           | Optimized for security                                                 |        21        |           ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-security/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-security) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/swift.ico" alt="" height="32px" class="megalinter-icon"></a>        | [swift](https://oxsecurity.github.io/megalinter/beta/flavors/swift/)                 | Optimized for SWIFT based projects                                     |        47        |                 ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-swift/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-swift) |
|      <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/terraform.ico" alt="" height="32px" class="megalinter-icon"></a>      | [terraform](https://oxsecurity.github.io/megalinter/beta/flavors/terraform/)         | Optimized for TERRAFORM based projects                                 |        52        |         ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-terraform/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-terraform) |

## Behind the scenes

### How are identified applicable files

- If this linter is active, all files will always be linted

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

gitleaks is called once on the whole project directory (`project` CLI lint mode)

- filtering can not be done using MegaLinter configuration variables,it must be done using gitleaks configuration or ignore file (if existing)
- `VALIDATE_ALL_CODEBASE: false` does not make gitleaks analyze only updated files

### Example calls

```shell
gitleaks detect --no-git --verbose --source .
```

```shell
gitleaks detect -c .gitleaks.toml --no-git --verbose --source .
```


### Help content

```shell
Gitleaks scans code, past or present, for secrets

Usage:
  gitleaks [command]

Available Commands:
  completion  generate the autocompletion script for the specified shell
  detect      detect secrets in code
  help        Help about any command
  protect     protect secrets in code
  version     display gitleaks version

Flags:
  -c, --config string          config file path
                               order of precedence:
                               1. --config/-c
                               2. env var GITLEAKS_CONFIG
                               3. (--source/-s)/.gitleaks.toml
                               If none of the three options are used, then gitleaks will use the default config
      --exit-code int          exit code when leaks have been encountered (default 1)
  -h, --help                   help for gitleaks
  -l, --log-level string       log level (trace, debug, info, warn, error, fatal) (default "info")
      --redact                 redact secrets from logs and stdout
  -f, --report-format string   output format (json, csv, sarif) (default "json")
  -r, --report-path string     report file
  -s, --source string          path to source (default: $PWD) (default ".")
  -v, --verbose                show verbose output from scan

Use "gitleaks [command] --help" for more information about a command.
```

### Installation on mega-linter Docker image

- Dockerfile commands :
```dockerfile
FROM zricethezav/gitleaks:v8.12.0 as gitleaks
COPY --from=gitleaks /usr/bin/gitleaks /usr/bin/
```
