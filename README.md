
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Ticket Lifecycle Examples
This documentation explores the lifecycle of tickets within the osTicket help desk system. It demonstrates how tickets are created, managed, and resolved, emphasizing the roles of end-users, agents, and administrators. The guide also touches on best practices for ticket management in real-world scenarios.

osTicket is an open-source ticketing system that helps organizations manage customer and internal support requests efficiently. This lab highlights practical workflows and illustrates how tickets progress from creation to resolution.

---

## Table of Contents
1. [Access Points](#access-points)
2. [Ticket Lifecycle Walkthrough](#ticket-lifecycle-walkthrough)
    - [Setup and Initial Configuration](#setup-and-initial-configuration)
    - [Creating and Resolving Tickets](#creating-and-resolving-tickets)
    - [Escalation and Access Control](#escalation-and-access-control)
3. [Best Practices in Ticketing Systems](#best-practices-in-ticketing-systems)
4. [Troubleshooting](#troubleshooting)
5. [Licensing Information](#licensing-information)
6. [Contact Information](#contact-information)

---

## Access Points

- **Admin/Analyst Login Page**: [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)  
- **End Users osTicket URL**: [http://localhost/osTicket](http://localhost/osTicket)  

---

## Ticket Lifecycle Walkthrough

### Setup and Initial Configuration
1. Change **SysAdmins Department** to a Top-Level Department.
2. Delete the **Maintenance Department** (do not archive).

### Creating and Resolving Tickets
#### Ticket 1: Mobile/Online Banking System Down
1. **As an End-User**:  
   - Create a ticket: "Entire mobile/online banking system is down."
2. **As a Help Desk Agent (john)**:  
   - Observe ticket properties:  
     - Priority  
     - Department  
     - SLA  
     - Assigned To  
   - Update ticket properties:  
     - SLA: **Sev-A (1 hour, 24/7)**  
     - Department: **Online Banking Department**  
3. Attempt to observe the ticket as "john" and verify access restrictions.
4. Work the ticket to completion as "jane."

#### Ticket 2: Adobe Upgrade Request
1. **As an End-User**:  
   - Create a ticket: "Accounting department needs Adobe upgrade, broken."
2. **As a Help Desk Agent (john)**:  
   - Observe ticket properties:  
     - Priority  
     - Department  
     - SLA  
     - Assigned To  
   - Update ticket properties:  
     - SLA: **Sev-B (4 hours, 24/7)**  
     - Department: **Support**  
3. Work the ticket to completion as "john."

#### Ticket 3: CFO’s Laptop Will Not Turn On
1. **As an End-User**:  
   - Create a ticket: "CFO’s laptop will no longer turn on."
2. **As a Help Desk Agent (john)**:  
   - Observe ticket properties:  
     - Priority  
     - Department  
     - SLA  
     - Assigned To  
   - Update ticket properties:  
     - SLA: **Sev-B (4 hours, 24/7)**  
     - Department: **Support**  
3. Work the ticket to completion as "john."

### Escalation and Access Control
1. Set the SLA for all tickets to **Sev-A** (1 hour, 24/7).
2. Observe that tickets become inaccessible to "john" after reassignment to SysAdmins.
3. Switch to the Admin Panel and assign "john" view access to the SysAdmins Department.
4. Return to the Agent Panel to observe escalated tickets and verify restricted permissions.

---

## Best Practices in Ticketing Systems

1. **Email Notifications**:  
   - osTicket and similar systems typically send email updates for every ticket action. These updates keep users informed and allow them to respond directly.

2. **Ticket Intake in Real-Life Scenarios**:  
   - Tickets may be created via multiple channels:  
     - Phone  
     - Chat applications  
     - Email  
     - Web forms  
     - In-person interactions  
   - Always create a ticket for every task completed, even if resolved on the spot. This builds a record for metrics and accountability.

3. **Repetition and Practice**:  
   - Repeatedly performing this lab will build intuition for managing tickets and understanding system workflows.
   - Explore additional features like email integration and advanced SLAs.

---

## Troubleshooting

1. **Issue**: Unable to access escalated tickets.  
   - **Cause**: Incorrect department or role permissions.  
   - **Solution**: Assign view access to the department through the Admin Panel.

2. **Issue**: SLA settings are not applied to tickets.  
   - **Cause**: SLA not updated during ticket creation.  
   - **Solution**: Ensure SLAs are assigned when setting ticket properties.

3. **Issue**: Email notifications are not sent to users.  
   - **Cause**: Email configuration is incomplete.  
   - **Solution**: Configure the email settings in the Admin Panel and test the connection.

---

## Licensing Information
osTicket is distributed under the GNU General Public License (GPL). For more information, visit the [osTicket License](https://osticket.com).

---

## Contact Information
For questions or feedback, feel free to reach out:  
- **GitHub**: https://github.com/Pieratboi  
- **LinkedIn**: <a href="https://www.linkedin.com/in/rafael-razapov-60391a2b8/?trk=opento_sprofile_topcard"> Rafael Razapov </a>  

