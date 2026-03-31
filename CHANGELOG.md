# Changelog

All changes of ParcelSync will be be documented in this document.

## v1.7.0-alpha - March 31, 2026

### Changes in v1.7.0-alpha

- The forms for registering Authorized Persons is now via Google AppScript WebApp

- Changed the data type for `isApproved` column into Enum with values 'pending', 'approved', and 'not approved'

### Added in v1.7.0-alpha

- I added new automation bot called 'Remove Expiring Authorized Person'

- Added PIN feature for secured shifting accounts of security guards.

- New Column in Security Guard Details &rightarrow; `pin`

- New Columns in Security Guards &rightarrow; `activePin`, `loginTimeStamp`, and `updatedLog`

### Fixes in v1.7.0-alpha

- Fixed the approval of Authorized Person, making sure buttons are visible by default

- Every notification, the sender name is now `ParcelSync Admin`

## v1.6.0-alpha - March 30, 2026

### Changes v1.6.0-alpha

- Delivery Logs Weekly Report: A report will be sent to the specific property manager about the delivery logs where he/she is designated building or property.

## v1.5.0-alpha - March 25, 2026

### Changes in v1.5.0-alpha

- Added proper view format for statuses in Delivery Logs and Incoming Authorized Persons
- Minor adjustments in forms of switching Guard Account and User Interface
- Modified proper arrangement of columns in Detailed View and Form Views of Delivery Logs, and Security Guards

### Fixes in v1.5.0-alpha

- Removed the Designated Building showing in the View of Managers causing warning of exposed ID.

## v1.4.0-alpha - March 23, 2026

### Changes in v1.4.0-alpha

- Security Guards sheet restructured into account directory.
- Personal details separated from login data

### Added in v1.4.0-alpha

- Security Guard Details sheet stores personal info referenced by guardAccountID

- activeGuard field in Security Guards references active guard on shift that links account to personal details

- Change Account view to allow shift handover between guards updates activeGuard reference only

- Security Guard Details form view for adding/editing personal details and separate from account management

- Security Guard Account form view for registering building email accounts

### Fixes in v1.4.0-alpha

- Guard identity now properly separated allowing multi-guard but single account

## v1.3.0-alpha - March 19, 20266

### Added in v1.3.0-alpha

- Approval of Authorized Person &rightarrow; every registered person is not going to be subject for approval before officially listed as approved. The property manager can either approve or disapprove.

### Fixes in v1.3.0-alpha

- The images of Authorized Person is now viewable.
- Notifications for Authorized Persons are now only allowed for those who are approved
- The modified forms for registering authorized persons is fixed.

## v1.2.0-alpha - March 17, 2026

### Added in v1.2.0-alpha

- Archive Delivery Logs Bot &rightarrow; it automatically archive the delivery logs which statuses are `claimed` and `returned` after 30 days.

- Old Photo Clean Up Bot &rightarrow; A bot that will run when old photos of QR and Parcel are stored after 30 days will be transfered to Google Drive `trash`.

- Email Report &rightarrow; A report will be sent to the property manager whenever the archive or cleanup occured.

### Fixed in v1.2.0-alpha

- The formula for archiving is changed using HOUR()/24 conversion

## v1.1.0-alpha — March 16, 2026

### Added in v1.1.0-alpha

- Shelf location tracking (Enum field, allows custom values, default: Guard Desk)

- Optional package weight field (kg)

- Tenant ID form validation (regex: TNT-[a-f0-9]{8})

- Tenant ID description text to prevent accidental editing

### Changed

- Package size retained alongside new weight field

- AppScript Forms deployed for Authorized Persons (backup or secondary feature)
