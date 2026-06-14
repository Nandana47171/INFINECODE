
# Gym Management System – QA Testing

**College:** Adi Shankara College of Engineering & Technology
**Module Assigned:** Staff
**Application:** Axo Fitness – Gym Management System
**URL:** truthordarefun.com/axofitness/staff
**Test Date:** 10-06-2026
**Tester:** Nandana

---

## Module Assigned

I was assigned the **Staff** module of the Gym Management System.

This module allows admin to manage gym staff, trainers and their access levels. It includes the following features:

- View all staff members with their Role, Kiosk Lock PIN and Status
- Add new staff member with Full Name, Email, Password, Manager PIN, Access Role and Account Status
- Search staff by name or email
- Filter staff by Role and Status
- Edit and Delete existing staff members

---

## Test Case Format

| Column | Description |
|---|---|
| Sno | Serial number |
| Bug ID | Unique ID for each test case (GYMSTF_0001, 0002...) |
| Date | Date of testing |
| Module | Section of the application tested |
| Feature | Specific field or feature tested |
| Test Scenario | What is being verified |
| Test Cases | What happened when tested |
| Test Status | Pass or Fail |

---

## Test Execution Summary

| Category | Count |
|---|---|
| Total Test Cases | 40 |
| Passed | 25 |
| Failed | 15 |
| Pass Rate | 62% |

---

## Failed Test Cases Summary

| Bug ID | Feature | Issue |
|---|---|---|
| GYMSTF_0006 | Full Name | Accepts numeric input |
| GYMSTF_0007 | Full Name | Accepts special characters |
| GYMSTF_0008 | Full Name | Mandatory but form submits without it |
| GYMSTF_0010 | Email Address | Accepts email without @ symbol |
| GYMSTF_0011 | Email Address | Mandatory but form submits without it |
| GYMSTF_0012 | Email Address | Duplicate email not rejected |
| GYMSTF_0014 | Temporary Password | Mandatory but form submits without it |
| GYMSTF_0015 | Temporary Password | No minimum length validation |
| GYMSTF_0017 | Manager PIN | Accepts less than 4 digits |
| GYMSTF_0018 | Manager PIN | Accepts more than 4 digits |
| GYMSTF_0019 | Manager PIN | Accepts alphabets |
| GYMSTF_0020 | Manager PIN | Mandatory but form submits without it |
| GYMSTF_0027 | Create Account | Submits with all fields empty |
| GYMSTF_0039 | Kiosk Lock PIN | Weak PIN like 1234 allowed without warning |

---

## Key Observations

1. Input validation is missing on almost all fields
2. Form can be submitted with all fields empty
3. Duplicate email addresses are not detected
4. Manager PIN accepts alphabets and wrong length
5. Weak Kiosk PIN like 1234 is allowed without any security warning
6. Password has no minimum length requirement

---

## Suggestions

1. Add validation for Full Name to accept alphabets only
2. Add proper email format validation
3. Reject duplicate email addresses
4. Enforce exactly 4 digits for Manager PIN
5. Add minimum password length validation
6. Warn users when a weak PIN like 1234 is used
7. Enforce all mandatory fields before form submission

---

## Overall Outcome

The Staff module has serious input validation issues. Most fields accept wrong or empty data without showing any error. This is a security risk for a real gym management system as invalid or weak credentials can be created without any restriction.
