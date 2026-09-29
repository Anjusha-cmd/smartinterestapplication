# SmartInterestX Database Schema

## CONTACTS

- id — primary key
- name
- mobile
- email
- type — Borrower or Lender

## TRANSACTIONS

- id — primary key
- contact_id — links to contacts.id
- amount
- type — Given or Taken
- rate
- rate_type — Monthly or Yearly
- start_date
- due_date
- note

## PAYMENTS

- id — primary key
- transaction_id — links to transactions.id
- amount
- payment_date
- mode — UPI / Bank Transfer / Cash / Other
- proof_path

## Relationship

CONTACTS 1 ---- many TRANSACTIONS
TRANSACTIONS 1 ---- many PAYMENTS
