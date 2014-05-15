laravel-schema-summary
======================

Creates a summary file of all migrations. This package is inspired by the `schema.rb` file of [Active Record Migrations](http://guides.rubyonrails.org/migrations.html).

## Installation

1. Add the following to your composer.json and run `composer update`

    ```json
    {
        "require": {
            "schickling/laravel-schema-summary": "dev-master"
        }
    }
    ```

2. Add `Schickling\SchemaSummary\SchemaSummaryServiceProvider` to your config/app.php

## Usage

The following command creates a `Schema.md` file in your `app/database` directory which contains a summary of all migrations. This summary can be understood as **one big migration** for documentation purposes.

```sh
$ php artisan migrate:schema
```

## Example Output

### users
Field | Type | Length | Unsigned | Default
--- | --- | --- | --- | ---
id | INT | 10 | yes |
name | VARCHAR | 128 (default) |  |

### photos
Field | Type | Length | Unsigned | Default
--- | --- | --- | --- | ---
id | INT | 10 | yes |
user_id | INT | 10 | yes | 0
url | VARCHAR | 128 (default) |  | 
