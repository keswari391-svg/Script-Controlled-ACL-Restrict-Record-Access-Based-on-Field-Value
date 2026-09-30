script-Controlled ACL - Restrict Record Access Based on Field Value

This repository contains ServiceNow Scripted ACL to restrict record access based on field value.

## Use Case
Restrict access to records where field value is specific (e.g., status = closed)

## Script
if (current.u_status == 'closed' && !gs.hasRole('admin')) {
    answer = false;
} else {
    answer = true;
}

## How to Configure in ServiceNow
1. Go to System  security1. Go to System Security > Access Control (ACL)
2. Create new ACL for table and operation
3. Check Scripted ACL
4. Paste this script
