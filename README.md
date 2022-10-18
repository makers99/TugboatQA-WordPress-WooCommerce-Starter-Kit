# Tugboat QA template for WordPress and WooCommerce

This is a more sophisticated template for deploying large-scale WordPress and WooCommerce
sites on [TugboatQA.com](https://www.tugboatqa.com/).

## Environment Variables

You can set them in the environment variables of your Tugboat project.

| Name | Default value | Description |
| ---- | ------------- | ----------- |
| DB_BUFFER_POOL_SIZE | `512` | The MySQL innodb_buffer_pool_size to set (in Megabytes). Defaults to 512 MB. |
| HTTP_BASIC_USERNAME | `user` | The username to set for HTTP Basic Authentication. |
| HTTP_BASIC_PASSWORD | `pass` | The password to set for HTTP Basic Authentication. |
| ELASTICPRESS_HOST | – | The hostname and port of the ElasticPress instance, if any. |
| ELASTICPRESS_SHIELD | – | The HTTP Authorization string for ElasticPress shield. |
| SSH_HOSTNAME | – | The SSH hostname from which to download the database. |
| SSH_PORT | `22` | The SSH port for downloading the database. |
| SSH_USER | `stage` | The SSH username for downloading the database. |
| WEB_REPLACE_DOMAIN | `example.com` | The domain to replace in the database after importing it. |


## Database Provisioning

You should avoid working with real customer data in testing environments to prevent
triggering unintended communication or actions.  You also want to minimize the
database size to only contain data necessary for testing to maintain fast deployments.

We worked hard to create a WP-CLI package that achieves this for you:

https://github.com/makers99/wp-cli-db-export-clean


## Credits

Brought to you by the team at [makers99](https://makers99.com)

Contributions and PRs are always welcome.
