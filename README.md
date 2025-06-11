# Rental-Data-Cleaning-Script
Google Appscript file that contains code to clean data in a spreadsheet

## Overview: processTenantData
This Google Apps Script automates the cleaning, validation, and transformation of tenant data within a Google Sheet, ensuring consistency across the tenant_directory and rent_roll sheets. It also separates and stores data needing attention or subject to privacy.

### 🔧 What the Script Does
Validates required sheets: Ensures both tenant_directory and rent_roll exist.

### Cleans tenant data:

1. Normalizes email to the first entry if multiple are found.

2. Converts tenant names to Proper Case and strips special characters.

3. Formats phone numbers and sets a default rent due day if missing.

4. Ensures rent amount is within a valid range ($100–$15,000).

5. Handles missing lease data:

6. Auto-generates lease start date if only the end date exists.

7. Moves rows with missing critical lease info to a separate sheet.

8. Cleans and sets balances:

9. Normalizes the outstanding balance using values from the rent roll or defaults.

10. Creates specialized sheets:

no email: Rows missing an email address.

no lease from: Rows missing lease start and end dates.

### PII: Extracted personal data including name, email, and DOB for privacy isolation.

### Final touches:

- Removes the dob column from tenant_directory.

- Deletes any extra blank rows.
