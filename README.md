# balena-firefly

[Firefly III](https://www.firefly-iii.org/) is a self-hosted financial manager.
It can help you keep track of expenses, income, budgets and everything in between.

## Getting Started

You can one-click-deploy this project to balena using the button below:

[![deploy-with-balena](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/klutchell/balena-firefly)

## Manual Deployment

Alternatively, deployment can be carried out by manually creating a [balenaCloud account](https://dashboard.balena-cloud.com) and application, flashing a device, downloading the project and pushing it via the [balena CLI](https://github.com/balena-io/balena-cli).

### Application Environment Variables

Application environment variables apply to all services within the application, and can be applied fleet-wide to apply to multiple devices.

| Name           | Description                                                                                                                                                             |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `TZ`           | Inform services of the [timezone](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) in your location.                                                       |
| `APP_KEY`      | The encryption key for your sessions. Keep this very secure. Change it to a string of exactly 32 chars or use something like `php artisan key:generate` to generate it. |
| `SET_HOSTNAME` | Set a custom hostname on application start. Default is `firefly`.                                                                                                       |

There are many environment variables that you can set in Firefly III. Just check out the [default env file](https://raw.githubusercontent.com/firefly-iii/firefly-iii/main/.env.example) that lists them all.

## Usage

Once your device joins the fleet you'll need to allow some time for it to download the various services.

When it's done you should be able to access the access the dashboard at <http://firefly.local>.

Documentation for Firefly III can be found at <https://docs.firefly-iii.org/>.

## Contributing

Please open an issue or submit a pull request with any features, fixes, or changes.
