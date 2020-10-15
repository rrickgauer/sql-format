# sql-format
Format your SQL statements using the [sql-pretty-printer API](https://github.com/sqlparser/sql-pretty-printer).

## Dependencies

This project uses the following modules:

* [requests](https://github.com/psf/requests)


## Installation

To install, download the repository with pip via:

```sh
pip install --upgrade sql_format
```


## Usage

In the **sql-format** directory, use:

```bash
python sql-format.py
```

## Example

sql-format will take the following SQL statement:

```sql
select Songs.id, Songs.title, Artists.name from Songs left join Artists on Songs.artist_id = Artists.id where Songs.id > 100 order by Songs.title desc limit 20;
```

and turns it into this:

```sql
SELECT Songs.id,
       Songs.title,
       Artists.name
FROM   Songs
       LEFT JOIN Artists
              ON Songs.artist_id = Artists.id
WHERE  Songs.id > 100
ORDER  BY Songs.title DESC
LIMIT  20;
```

