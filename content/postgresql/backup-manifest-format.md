## Chapter 77. Backup Manifest Format

**Table of Contents**

  * *   [77.1. Backup Manifest Top-level Object](backup-manifest-toplevel.html)
  * [77.2. Backup Manifest File Object](backup-manifest-files.html)
  * [77.3. Backup Manifest WAL Range Object](backup-manifest-wal-ranges.html)

The backup manifest generated by [pg\_basebackup](app-pgbasebackup.html "pg_basebackup") is primarily intended to permit the backup to be verified using [pg\_verifybackup](app-pgverifybackup.html "pg_verifybackup"). However, it is also possible for other tools to read the backup manifest file and use the information contained therein for their own purposes. To that end, this chapter describes the format of the backup manifest file.

A backup manifest is a JSON document encoded as UTF-8. (Although in general JSON documents are required to be Unicode, PostgreSQL permits the `json` and `jsonb` data types to be used with any supported server encoding. There is no similar exception for backup manifests.) The JSON document is always an object; the keys that are present in this object are described in the next section.