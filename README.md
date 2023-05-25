# BecaGIS_MapViewer_Test

## Setup
```shell
curl -s "https://laravel.build/mapviewer?devcontainer" | bash
```

## Packages
### [Debugbar for Laravel](https://github.com/barryvdh/laravel-debugbar)

```shell
composer require barryvdh/laravel-debugbar --dev
```

### Laravel Telescope

```shell
composer require laravel/telescope --dev
sail artisan telescope:install
sail artisan migrate
```

Manually register Telescope's service providers `App\Providers\AppServiceProvider`

```php
/**
 * Register any application services.
 */
public function register(): void
{
    if ($this->app->environment('local')) {
        $this->app->register(\Laravel\Telescope\TelescopeServiceProvider::class);
        $this->app->register(TelescopeServiceProvider::class);
    }
}
```

Adding the following to your composer.json file

```shell title="composer.json"
"extra": {
    "laravel": {
        "dont-discover": [
            "laravel/telescope"
        ]
    }
},
```


```shell
$schedule->command('telescope:prune')->daily();
```

```shell title="composer.json"
{
    "scripts": {
        "post-update-cmd": [
            "@php artisan vendor:publish --tag=laravel-assets --ansi --force"
        ]
    }
}
```

### Laravel Pint

```shell
composer require laravel/pint --dev
```

### Laravel Sail

```shell
composer require laravel/sanctum
artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
artisan migrate
```

### Laravel Horizon

```shell
composer require laravel/horizon
artisan horizon:install
```

## Links
Requirements:
https://github.com/spatie/laravel-google-fonts
https://github.com/spatie/eloquent-sortable
https://github.com/spatie/laravel-model-cleanup
https://github.com/spatie/laravel-sluggable
https://github.com/binarcode/laravel-restify
https://laravel.com/docs/10.x/octane
https://github.com/hammerstonedev/fast-paginate
https://github.com/filamentphp/filament

https://github.com/kolossal-io/laravel-multiplex
https://github.com/l3aro/pipeline-query-collection
https://github.com/touhidurabir/laravel-model-sanitize
https://github.com/clickbar/laravel-magellan
https://laravel-auditing.com/

Dev:
https://github.com/rezaamini-ir/migrator
https://github.com/worksome/envy


Optional:
https://github.com/spatie/laravel-view-models
https://github.com/spatie/laravel-options
https://github.com/spatie/laravel-directory-cleanup
https://github.com/spatie/laravel-googletagmanager
https://github.com/spatie/laravel-blade-javascript
https://github.com/qruto/laravel-flora
https://github.com/laravel/pint




https://github.com/spatie/laravel-options
https://github.com/spatie/laravel-responsecache
https://github.com/michael-rubel/laravel-formatters
https://github.com/rappasoft/laravel-authentication-log
https://github.com/tpetry/laravel-postgresql-enhanced
https://laravelactions.com/
https://github.com/javoscript/laravel-macroable-models
https://github.com/haruncpi/laravel-user-activity
https://github.com/spatie/laravel-settings

https://github.com/coderello/laravel-shared-data
https://github.com/cviebrock/eloquent-sluggable


Optional
https://github.com/spatie/laravel-model-status

https://github.com/opcodesio/log-viewer
https://github.com/spatie/laravel-navigation
https://github.com/awssat/laravel-visits



https://github.com/spatie/laravel-deleted-models
https://github.com/spatie/laravel-query-builder
https://github.com/spatie/laravel-image-optimizer
https://github.com/spatie/laravel-health
https://github.com/spatie/laravel-webhook-client
https://github.com/spatie/laravel-multitenancy
https://github.com/spatie/laravel-collection-macros
https://github.com/spatie/laravel-notification-log
https://github.com/spatie/laravel-horizon-watcher
https://github.com/spatie/laravel-model-info
https://github.com/spatie/laravel-robots-middleware
https://github.com/spatie/laravel-schemaless-attributes
https://github.com/spatie/laravel-url-signer
https://github.com/spatie/laravel-personal-data-export
https://github.com/spatie/laravel-queueable-action
https://github.com/spatie/laravel-cookie-consent
https://github.com/spatie/laravel-webhook-server
https://github.com/spatie/laravel-http-logger
https://github.com/spatie/laravel-server-monitor
https://github.com/spatie/laravel-database-mail-templates
https://github.com/spatie/laravel-github-webhooks
https://github.com/spatie/laravel-site-search
https://github.com/spatie/laravel-stats
https://github.com/spatie/laravel-enum
https://github.com/spatie/laravel-cronless-schedule
https://github.com/spatie/laravel-short-schedule
https://github.com/spatie/laravel-disk-monitor
https://github.com/spatie/laravel-schedule-monitor
https://github.com/spatie/laravel-menu
https://github.com/spatie/laravel-html
https://github.com/spatie/laravel-stubs
https://github.com/spatie/laravel-flash





https://github.com/protonemedia/laravel-cross-eloquent-search
https://github.com/spatie/laravel-searchable
https://github.com/spatie/laravel-model-info
https://github.com/surgiie/transformer
https://github.com/pricecurrent/laravel-eloquent-filters
https://github.com/mostafaznv/laracache
https://github.com/hammerstonedev/flaky
https://github.com/ryangjchandler/laravel-comments
https://github.com/jessarcher/zsh-artisan
https://github.com/maize-tech/laravel-markable
https://github.com/hotmeteor/receiver
https://github.com/BinarCode/laravel-mailator
https://github.com/milwad-dev/laravel-validate
https://github.com/tpetry/laravel-query-expressions
https://github.com/michael-rubel/laravel-auto-binder
https://github.com/devNoiseConsulting/laravel-scout-postgres-tsvector
https://github.com/mchev/banhammer
https://github.com/oneduo/laravel-recaptcha-enterprise
https://github.com/MohsenAbrishami/stethoscope
https://github.com/spatie/laravel-model-flags
https://github.com/tkaratug/laravel-notification-event-subscriber
https://github.com/oddvalue/laravel-drafts
https://github.com/Sammyjo20/laravel-haystack
https://github.com/dive-be/laravel-dry-requests
https://github.com/PHLAK/Splat
https://github.com/ryangjchandler/blade-cache-directive
https://github.com/archtechx/enums
https://github.com/cerbero90/eloquent-inspector
https://github.com/glhd/laravel-dumper
https://github.com/cybercog/laravel-ban
https://github.com/bilfeldt/laravel-route-statistics
https://github.com/michael-rubel/laravel-enhanced-container
https://github.com/mateusjunges/laravel-kafka
https://github.com/datacreativa/laravel-presentable
https://github.com/staudenmeir/eloquent-has-many-deep
https://github.com/kirschbaum-development/eloquent-power-joins
https://github.com/robersonfaria/laravel-database-schedule
https://github.com/qirolab/laravel-themer
https://github.com/spatie/laravel-package-tools
https://github.com/squirephp/squire
https://github.com/Qoraiche/laravel-mail-editor
https://github.com/spatie/laravel-flash
https://github.com/appstract/laravel-options
https://github.com/cybercog/laravel-love
https://github.com/tenancy/tenancy


Tips:
https://medium.com/@soulaimaneyh/laravel-repository-pattern-da4e1e3efc01
https://laravel-news.com/working-with-laravel-model-events
https://laravel-news.com/creating-helpers
Multiple Vite



Filament:
https://github.com/rgasch/filament-extended-starter-kit

https://github.com/devtical/filament-sanctum
https://github.com/TappNetwork/filament-auditing
https://github.com/bezhanSalleh/filament-exceptions

https://filamentphp.com/plugins/access-and-menu-management



https://github.com/husam-tariq/filament-database-schedule
https://github.com/pascalebeier/filament-pages

https://filamentphp.com/plugins/profile
https://github.com/pxlrbt/filament-excel
https://filamentphp.com/plugins/breezy
https://filamentphp.com/plugins/shield
https://filamentphp.com/plugins/navigation
https://filamentphp.com/plugins/user-role-resource-management
https://github.com/althinect/filament-spatie-roles-permissions
https://github.com/3x1io/filament-user
https://filamentphp.com/docs/2.x/spatie-laravel-media-library-plugin/installation
https://filamentphp.com/plugins/fabricator
https://filamentphp.com/plugins/alperenersoy-export
https://filamentphp.com/docs/2.x/spatie-laravel-settings-plugin/installation
https://filamentphp.com/plugins/spatie-health
https://github.com/z3d0x/filament-logger
https://filamentphp.com/plugins/import
https://github.com/shuvroroy/filament-spatie-laravel-backup
https://github.com/rahmanramsi/filament-editorjs
https://github.com/mohamedsabil83/filament-forms-tinyeditor
https://filamentphp.com/plugins/blog
https://github.com/DutchCodingCompany/filament-socialite
https://filamentphp.com/plugins/curator
https://filamentphp.com/plugins/badgeable-column
https://github.com/webbingbrasil/filament-advancedfilter
https://filamentphp.com/plugins/simple-repeater
https://filamentphp.com/plugins/filter-sets
https://filamentphp.com/plugins/email-log
https://github.com/3x1io/filament-menus
https://github.com/3x1io/filament-themes
https://filamentphp.com/plugins/browser

https://filamentphp.com/plugins/impersonate
https://github.com/ryangjchandler/filament-feature-flags
https://filamentphp.com/plugins/password-reveal-input
https://github.com/webbingbrasil/filament-copyactions
https://github.com/latvel/filament-template
https://filamentphp.com/plugins/lucasgiovanny-multiselect-two-sides
https://filamentphp.com/plugins/json-editor-field
https://filamentphp.com/plugins/date-filter
https://github.com/reworck/filament-settings
https://github.com/codeWithDiki/filament-theme-manager
https://filamentphp.com/plugins/icon-picker
https://filamentphp.com/plugins/fortify
https://filamentphp.com/plugins/spatie-tags
https://github.com/yemenpoint/FilamentTree
https://filamentphp.com/plugins/code-editor
https://github.com/alexjustesen/filament-spatie-laravel-activitylog
https://filamentphp.com/plugins/pxlrbt-activity-log

https://filamentphp.com/plugins/password-reveal-input

https://filamentphp.com/plugins/ryangjchandler-log-viewer
https://filamentphp.com/plugins/tree-page
https://github.com/codeWithDiki/filament-daterange
https://github.com/yepsua/filament-rating-field
https://github.com/awcodes/filament-versions
https://filamentphp.com/plugins/phone-field
https://github.com/ysfkaya/filament-phone-input
https://filamentphp.com/plugins/import-inline-form-paste
https://filamentphp.com/plugins/static-asset-handler
https://github.com/konnco/filament-safely-delete
https://github.com/stephenjude/filament-debugger
https://github.com/marjose123/filament-no-connection
https://filamentphp.com/plugins/website-cms-management
https://filamentphp.com/plugins/google-recaptcha-field
https://filamentphp.com/plugins/avatar-provider
https://github.com/awcodes/filament-gravatar
https://github.com/msuhels/editorjs
https://github.com/solutionforest/filament-grid-layout-plugin
https://github.com/solutionforest/filament-tab-plugin
https://filamentphp.com/plugins/bandel
https://github.com/KoalaFacade/Filament-Navigation-Holder

https://github.com/TappNetwork/filament-timezone-field
https://filamentphp.com/plugins/sweebee-char-counter
https://filamentphp.com/plugins/multi-widget
https://github.com/solutionforest/filament-firewall
