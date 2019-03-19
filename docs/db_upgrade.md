# Database Upgrades and Migrations

These migrations only need to be conducted when adding or removing tables or columns from tables in the SQLite DB that is included within [models.py](https://github.com/SchwererKonigstiger/HUMVEE)

## Database Upgrade/Migration Setup
Inside the virtual environment (venv), run `flash db migrate -m "table_to_update"`
After this, still inside the virtual environment, run `flask db upgrade` to complete the ugprade.

### Database Downgrade
If there is an issue with your newly updated database, you can conduct `flask db downgrade` to roll it back to the previous version. Keep in mind any changes that were made after the upgrade will be discarded.