# lumen_api_gateway

Features :
1. oAuth with passport
2. Throtle Request

https://packagist.org/packages/dusterio/lumen-passport

# Create new tables for Passport
php artisan migrate

# Install encryption keys and other necessary stuff for Passport
php artisan passport:install


Personal access client created successfully.
Client ID: 1
Client Secret: Md7KZEL29UU2M838nohukX8PVBszQi7xaZqqEl3W
Password grant client created successfully.
Client ID: 2
Client Secret: aIt3rhabV7JF50xuoxACwBGPGdbKswrFmtkGzjkt

Make sure your user model uses Passport's HasApiTokens
class User extends Model implements AuthenticatableContract, AuthorizableContract
{
    use HasApiTokens, Authenticatable, Authorizable;

    /* rest of the model */
}