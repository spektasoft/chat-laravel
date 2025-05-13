# Chat Laravel

## Important Notice

ULIDs are used as the default ID type.

## Local Development

1. Download this repository and extract it anywhere in your local environment.

1. Install dependencies:

    ```
    composer install
    ```

    ```
    npm i
    ```

1. Create the `.env` file:

    ```
    cp .env.example .env
    ```

1. Assign Super User(s) by assigning `Fortify` username(s) (default to email) in `.env` file:

    ```
    AUTH_SUPER_USERS={FORTIFY_USERNAMES}
    # Separated with a comma (,)
    # Example: admin@example.com,su@example.com
    ```

1. Assign a backup email address to send backup result notifications:

    ```
    BACKUP_MAIL_TO_ADDRESS={EMAIL_ADDRESS}
    ```

1. Generate the `APP_KEY`:

    ```
    php artisan key:generate
    ```

1. Create the symbolic link for storage:

    ```
    php artisan storage:link
    ```

1. Run the migration:

    ```
    php artisan migrate
    ```

1. Run the app:

    ```
    composer run dev
    ```

## LLM Commands

This app includes LLM (Language Model) commands to assist with generating commit messages and pull request messages.

To generate a commit message based on staged changes:

```
php artisan llm:commit
```

To generate a pull request message based on a commit range:

```
php artisan llm:pr
```

## Upstream

Apply any changes available from the Starter Kit Laravel [main branch](https://github.com/spektasoft/starter-kit-laravel/compare/6d3ad17d6b1e38678bbc1f2c10c85fab5887a520...main).

## License

The app is open-sourced software licensed under the [MIT license](LICENSE).
