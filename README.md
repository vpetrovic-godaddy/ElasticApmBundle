# ElasticApmBundle

* This is a **downgraded symfony version** of the original bundle made for symfony ^4.0|^5.0
* Symfony version for this one is ~2.6|~3.0, a version that the original bundle doesn't support.
* It requires PHP version >= 7.1

## Original bundle info:
[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE)
[![Build Status][ico-travis]][link-travis]
[![Coverage Status][ico-scrutinizer]][link-scrutinizer]
[![Quality Score][ico-code-quality]][link-code-quality]
[![Total Downloads][ico-downloads]][link-downloads]

ElasticApmBundle is a symfony bundle that allows you to track your symfony application's performance by sending transactions and metrics to elastic apm server instance.

## Installation
* Add configuration to main config file

```yaml
elastic_apm:
    enabled: true
    agent:
        appName: '' # Name of this application, Required
        serverUrl: 'http://127.0.0.1:8200' # APM Server Endpoint, Default: 'http://127.0.0.1:8200'
        secretToken: null # Secret token for APM Server, Default: null
        environment: 'development' # Environment, Default: 'development'
```

## Customization

### Transaction tracking blacklist and whitelist

### Exception tracking blacklist and whitelist

### Transaction name

### Shared context

### User context

## Configuration Reference

```yaml
elastic_apm:
    enabled: true
    agent:
        appName: '' # Name of this application, Required
        serverUrl: 'http://127.0.0.1:8200' # APM Server Endpoint, Default: 'http://127.0.0.1:8200'
        secretToken: null # Secret token for APM Server, Default: null
        environment: '' # Environment, Default: 'development'
    transactions:
        include:
            # - App\Controller\API\OAuthController::tokenAction
            # - App\Controller\Backend\DashboardController::*
        exclude:
            # - web_profiler.controller.profiler::toolbarAction
            # - web_profiler.controller.profiler::panelAction
            # - App\Controller\Backend\UserController::loginAction
            # - App\Controller\Backend\ReportController::*
    exceptions:
        include:
        exclude:
            # - Symfony\Component\Security\Core\Exception\AccessDeniedException

```

## License

The Apache-2.0 License. Please see [License File](LICENSE) for more information.

[ico-version]: https://img.shields.io/packagist/v/spacespell/elastic-apm-bundle.svg?style=flat-square
[ico-license]: https://img.shields.io/packagist/l/spacespell/elastic-apm-bundle
[ico-travis]: https://img.shields.io/travis/spacespell/elastic-apm-bundle/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/spacespell/elastic-apm-bundle.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/spacespell/elastic-apm-bundle.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/spacespell/elastic-apm-bundle.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/spacespell/elastic-apm-bundle
[link-travis]: https://travis-ci.org/spacespell/elastic-apm-bundle
[link-scrutinizer]: https://scrutinizer-ci.com/g/spacespell/elastic-apm-bundle/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/spacespell/elastic-apm-bundle
[link-downloads]: https://packagist.org/packages/spacespell/elastic-apm-bundle
[link-author]: https://github.com/phoenixgao
