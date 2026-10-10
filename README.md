# ServiceNow Business Rules – Automatic Record Updates

## Project Overview
This project demonstrates how to use ServiceNow Business Rules to automatically update Incident records using server-side JavaScript.

## Objective
Automatically change an Incident's state to **In Progress** when its priority is set to **Critical**.

## Technologies Used
- ServiceNow Platform
- JavaScript
- Business Rules
- Incident Management

## Business Rule Configuration

| Property | Value |
|---|---|
| Name | Auto Update Incident State |
| Table | Incident [incident] |
| When | Before |
| Advanced | Enabled |
| Insert | Disabled |
| Update | Enabled |
| Active | Enabled |

## Business Rule Script

```javascript
(function executeRule(current, previous) {

    if (current.priority == '1') {
        current.state = '2';
    }

})(current, previous);
```

## How It Works
1. An Incident record is created or updated.
2. The Business Rule checks whether the priority is Critical.
3. If the condition is true, the state is set to In Progress.
4. The updated state is saved with the Incident record.

## Testing
1. Open the Incidents list in ServiceNow.
2. Create or update an Incident.
3. Set Priority to Critical.
4. Save the record.
5. Verify that the State changes to In Progress.

**Expected Result:** The Incident state is automatically updated when the Business Rule condition is satisfied.

## Screenshots
Add screenshots showing:
- Business Rule configuration
- Business Rule script
- Incident before the update
- Incident after the update

## Learning Outcome
Learned how to configure and test ServiceNow Business Rules for automated record updates.

## Author
Burjangi Krishna
