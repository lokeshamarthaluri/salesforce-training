# Day 6 – Triggers & SOQL

## 1. What is SOQL?

**SOQL (Salesforce Object Query Language)** is a query language used in Salesforce to retrieve data from Salesforce objects. It is similar to SQL but is specifically designed for Salesforce data and relationships.

### Example:

```apex
SELECT Id, Name, Email FROM Contact
```

This query retrieves the Id, Name, and Email fields from the Contact object.

### Why SOQL is Important

* Retrieves records from Salesforce objects.
* Supports filtering, sorting, and relationship queries.
* Used extensively in Apex classes and triggers.
* Helps automate business processes based on data.

---

## 2. What is an Apex Trigger?

An **Apex Trigger** is a piece of Apex code that executes automatically before or after specific database events occur on Salesforce records.

### Trigger Events

* Before Insert
* Before Update
* Before Delete
* After Insert
* After Update
* After Delete
* After Undelete

### Example:

```apex
trigger ContactTrigger on Contact (before insert) {
    for(Contact c : Trigger.new){
        c.Description = 'New Contact Created';
    }
}
```

This trigger automatically sets a description before a Contact record is inserted.

---

## 3. Differences

### Flow vs Trigger

| Flow                                   | Trigger                                               |
| -------------------------------------- | ----------------------------------------------------- |
| Low-code automation tool               | Code-based automation                                 |
| Easy for admins to create and maintain | Requires Apex programming knowledge                   |
| Suitable for simple business processes | Suitable for complex logic and large-scale processing |
| Easier debugging and maintenance       | More flexible and powerful                            |
| Runs through declarative configuration | Runs through Apex code                                |

### Before Trigger vs After Trigger

| Before Trigger                                   | After Trigger                                |
| ------------------------------------------------ | -------------------------------------------- |
| Executes before records are saved                | Executes after records are saved             |
| Used to validate or modify record values         | Used for actions requiring record IDs        |
| Faster because no extra save operation is needed | Used for related record creation and updates |
| Can change field values directly                 | Cannot directly modify Trigger.new records   |
| Common for validations and defaults              | Common for integrations and related records  |

---

## 4. Trigger Use Cases (5 Examples)

### 1. Auto-Populate Fields

Automatically set default values when a new record is created.

### 2. Data Validation

Prevent records from being saved when business rules are violated.

### 3. Create Related Records

Automatically create child records after a parent record is inserted.

### 4. Update Related Objects

When an Opportunity is closed, update related Account information.

### 5. Send Notifications

Trigger email alerts or custom notifications when important changes occur.

---

## 5. Query Examples (English Query Ideas)

### Example 1

Find all contacts whose last name is "Smith".

```apex
SELECT Id, FirstName, LastName
FROM Contact
WHERE LastName = 'Smith'
```

### Example 2

Find all accounts created this month.

```apex
SELECT Id, Name
FROM Account
WHERE CreatedDate = THIS_MONTH
```

### Example 3

Find opportunities worth more than $10,000.

```apex
SELECT Id, Name, Amount
FROM Opportunity
WHERE Amount > 10000
```

### Example 4

Find all active users.

```apex
SELECT Id, Name
FROM User
WHERE IsActive = true
```

### Example 5

Find contacts related to a specific account.

```apex
SELECT Id, Name
FROM Contact
WHERE AccountId = '001XXXXXXXXXXXX'
```

---

## 6. Reflection: Why Enterprise Systems React Automatically to Data Changes

Enterprise systems manage large volumes of data and business processes. Manual monitoring of every change is inefficient and prone to errors. Automated mechanisms such as Apex Triggers allow systems to respond instantly whenever data is created, updated, deleted, or restored.

Automatic reactions help organizations:

* Maintain data consistency.
* Enforce business rules.
* Reduce manual effort.
* Improve operational efficiency.
* Ensure real-time updates across related records.
* Enhance user experience and reliability.

Salesforce uses triggers and automation tools to ensure that important business actions occur immediately when data changes, making enterprise applications more scalable, accurate, and efficient.

# Light Completion Day

## Modules Completed
- Search Solution Basics
- Agentforce 360 Platform Events Basics
- Command-Line Interface
## Key Learnings

### Search Solution Basics
- Salesforce search helps users quickly find records and information.

### Agentforce 360 Platform Events Basics
- Platform events allow systems to communicate through event-driven notifications.

### Command-Line Interface
- CLI tools help developers perform tasks faster through terminal commands.

## Doubt / Question
- How are platform events used in large Salesforce applications?

## Platform Event Thinking
When a student registers for a course, the registration event can automatically notify the student, instructor, and billing system.

## CLI Reflection
Developers use command-line tools because they are faster and can automate repetitive tasks. They also help manage projects efficiently.

## Search Reflection
Fast and accurate search helps employees find information quickly, improving productivity and reducing time spent searching for data.

## Trailhead Progress Screenshot

