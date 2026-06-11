# Day 8 - LWC Basics

## What is LWC?

Lightning Web Components (LWC) is Salesforce's modern UI development framework built on web standards such as JavaScript, HTML, and CSS. It allows developers to create reusable, efficient, and lightweight components for Salesforce applications.

LWC follows a component-based architecture where each component is self-contained and can be combined with other components to build complex user interfaces.

### Key Features

* Reusable components
* Fast performance
* Modern JavaScript support
* Secure framework architecture
* Easy integration with Salesforce data and services

---

## Why Salesforce Uses LWC

Salesforce introduced Lightning Web Components to provide a faster, more scalable, and standards-based development experience.

### Benefits of LWC

* Improved performance compared to older frameworks
* Uses native browser capabilities
* Easier for web developers familiar with HTML, CSS, and JavaScript
* Better maintainability through reusable components
* Enhanced user experience with responsive interfaces
* Supports enterprise-scale application development

---

## UI Screens

### Home Screen

*Insert Screenshot Here*

Description:

* Displays the main user interface.
* Provides navigation and interaction options.

### Component View

*Insert Screenshot Here*

Description:

* Shows individual Lightning Web Components.
* Demonstrates component rendering and user interactions.

### Final Output Screen

*Insert Screenshot Here*

Description:

* Displays the completed application output.
* Verifies successful implementation of LWC concepts.

---

## Component Breakdown

### Parent Component

Responsibilities:

* Acts as the main container.
* Manages data flow between child components.
* Handles application-level logic.

### Child Component(s)

Responsibilities:

* Display specific UI elements.
* Receive data from parent components through properties.
* Trigger events back to the parent when required.

### Component Structure

```text
Parent Component
│
├── Child Component 1
├── Child Component 2
└── Child Component 3
```

### Files Used

```text
componentName/
│
├── componentName.html
├── componentName.js
├── componentName.js-meta.xml
└── componentName.css (optional)
```

---

## Frontend vs Backend Logic

| Frontend Logic        | Backend Logic                        |
| --------------------- | ------------------------------------ |
| UI rendering          | Data processing                      |
| User interactions     | Database operations                  |
| Form validation       | Business rules                       |
| Event handling        | Server-side execution                |
| HTML, CSS, JavaScript | Apex Classes and Salesforce Services |

### Frontend (LWC)

* Creates and manages user interfaces.
* Handles button clicks and user actions.
* Updates data displayed on the screen.

### Backend (Salesforce/Apex)

* Retrieves records from Salesforce.
* Executes business logic.
* Performs data updates and validations.

---

## Reflection

Working with Lightning Web Components helped me understand how modern Salesforce applications are built using reusable UI components. I learned how components communicate with each other, how frontend logic is separated from backend processing, and how Salesforce leverages modern web standards to improve performance and maintainability. The component-based approach makes applications easier to develop, test, and scale.

---

# Reflection Task

## Why do modern enterprise systems use component-based UI architecture?

Modern enterprise systems use component-based UI architecture because it improves scalability, maintainability, and development efficiency.

### Reasons

1. **Reusability**

   * Components can be created once and reused across multiple pages and applications.

2. **Maintainability**

   * Changes made to a component automatically apply wherever it is used.

3. **Scalability**

   * Large applications can be divided into smaller, manageable pieces.

4. **Team Collaboration**

   * Multiple developers can work on different components simultaneously.

5. **Consistency**

   * Shared components ensure a uniform user experience across the application.

6. **Faster Development**

   * Developers can assemble applications from existing components rather than building everything from scratch.

7. **Better Testing**

   * Individual components can be tested independently, improving software quality.

### Conclusion

Component-based architecture enables enterprise applications to remain organized, efficient, scalable, and easier to maintain as business requirements grow. This is one of the main reasons Salesforce adopted Lightning Web Components as its modern UI framework.

