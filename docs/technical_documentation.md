# SmartInterestX Technical Documentation

## Stack

- Flutter
- Dart
- Provider
- SQLite using sqflite
- fl_chart
- csv
- share_plus
- image_picker
- shared_preferences
- flutter_local_notifications

## Architecture

The project is intentionally kept simple for a beginner:

lib/
- models/       data classes
- services/     database, interest calculation, notifications
- providers/    simple Provider state
- screens/      app screens
- utils/        formatting helpers

## Interest Logic

Simple interest:

I = P × R × T / 100

Monthly:
T = days / 30

Yearly:
T = days / 365

The transaction detail screen shows interest till today and, when a due date exists, interest till due date.

## Notifications

The project uses local notifications. A simple reminder notification is shown when a transaction with a due date is saved. A full production version should schedule exact notifications 1, 3 and 7 days before the due date as requested by the specification.

## Backup / Export

Transactions can be exported to CSV and shared using the Android share sheet. SQLite is the local database.

The specification recommends Firebase Firestore, Firebase Storage and Google Drive as cloud options, but cloud services are not enabled in this beginner version.

## Security

A simple device PIN is stored using shared_preferences. This is intentionally basic. A production version can replace it with local_auth biometric/PIN protection and encrypted backups.
