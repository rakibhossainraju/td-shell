## ADDED Requirements

### Requirement: Workspace Enable/Disable Toggle
The system SHALL provide a primary toggle to enable or disable business hours for the entire workspace.

#### Scenario: Enabling Business Hours
- **WHEN** the administrator switches the toggle to "Enabled"
- **THEN** the configuration parameters (Target Inboxes, Time Zone, Operational Hours, Holiday Selection) SHALL become active and editable.

### Requirement: Target Inboxes Configuration
The system SHALL allow the administrator to select which specific inboxes the business hours rules apply to.

#### Scenario: Selecting Target Inboxes
- **WHEN** the administrator selects one or more inboxes from the dropdown list
- **THEN** the system SHALL associate the business hours rules with those specific inboxes.

### Requirement: Time Zone Selection
The system SHALL allow the administrator to set the geographic time zone for the workspace.

#### Scenario: Setting Time Zone
- **WHEN** the administrator selects a time zone from the list
- **THEN** all operational hour calculations SHALL be anchored to that specific time zone.

### Requirement: Operational Hours Definition
The system SHALL allow the administrator to choose between "24/7 Calendar Hours" or "Business Hours".

#### Scenario: Custom Business Hours
- **WHEN** the administrator selects "Business Hours" and configures specific daily slots
- **THEN** the system SHALL enforce operational rules only during those defined time intervals.

### Requirement: Holiday List Association
The system SHALL allow the administrator to associate pre-defined holiday lists as operational block-out dates.

#### Scenario: Associating Holidays
- **WHEN** the administrator selects a holiday list
- **THEN** the system SHALL consider those dates as non-operational regardless of the defined Business Hours.
