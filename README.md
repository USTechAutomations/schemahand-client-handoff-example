# SchemaHand client-handoff example

When a developer hands a database over to a client, someone has to explain what
every table and column means. This repository is one finished example of that
handoff, produced by the SchemaHand offline tool from a single made-up PostgreSQL
schema. Every value here is synthetic — no real customer, client, or production
database appears.

**[Download the example (`example.zip`)](https://raw.githubusercontent.com/USTechAutomations/schemahand-client-handoff-example/main/example.zip)**

## What is inside

Unzip it and you get five files:

- `source.sql` — the made-up PostgreSQL script used as input: 12 tables across two
  schemas (`app` and `audit`), with primary keys, foreign keys, and comments.
- `handoff.html` — the schema diagram with editable notes. Open it in a browser to
  see the tables and how they connect. You can type notes against any table, then
  click **Save edited copy** to write a new HTML file. That save does not change
  `dictionary.csv`.
- `dictionary.csv` — a flat table-and-column dictionary from the same parse: 54
  columns with their types, primary and foreign keys, defaults, and notes.
- `README.md` — the notes that ship with the sample.
- `MANIFEST.sha256` — SHA-256 hashes of the four files above, so you can confirm
  the contents were not altered.

Start with `handoff.html` to read the schema visually, then open `dictionary.csv`
if you want the same information as a spreadsheet.

## What it does and does not do

This zip is a fixed worked example. It is **not** a general SQL parser, and it
cannot read a schema you supply — the files and counts are frozen to this one
input. It makes no database connection, runs no queries, and moves no data. Review it against the included source before using it as a handoff reference.

Running SchemaHand against **your own** SQL is what the paid offline tool does.

## Links

- Walkthrough of this example: https://ustechautomations.com/feeds/schemahand/client-handoff-example/
- Buy the offline tool: https://ustechautomations.gumroad.com/l/schemahand-offline?utm_source=github&utm_medium=example&utm_campaign=non_ecommerce_20260921
