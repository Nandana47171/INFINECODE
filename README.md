# Gym Management System – QA Testing

**College:** Adi Shankara College of Engineering & Technology

**Module Assigned:** New Member

**Application:** Axo Fitness – Gym Management System

**URL:** truthordarefun.com/axofitness/members/entry

**Test Date:** 04-06-2026

**Tester:** Nandana Ramachandran

---

## Module Assigned

I was assigned the **New Member** module of the Gym Management System.

This module allows admin staff to register a new gym member by filling in the following sections:

- Personal Information (Name, DOB, Blood Group, Gender, etc.)
- Contact Information (Address, Mobile, Email, Emergency Contact)
- Health Details (Health Problems, Joint Problems, Side Effects, Remarks)
- Notification Preferences (SMS, Email, WhatsApp)
- Face Verification Setup (Upload / Web Camera)

---

## Test Case Format

| Column | Description |
|---|---|
| Sno | Serial number |
| Bug ID | Unique ID for each test case (GYMINT_0001, 0002...) |
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
| Total Test Cases | 35 |
| Passed | 21 |
| Failed | 14 |
| Pass Rate | 60% |

---

## Failed Test Cases Summary

| Bug ID | Feature | Issue |
|---|---|---|
| GYMINT_0001 | First Name | Accepts numeric input |
| GYMINT_0002 | First Name | Accepts special characters |
| GYMINT_0006 | Date of Birth | Accepts future dates |
| GYMINT_0007 | Date of Birth | Accepts invalid date format |
| GYMINT_0012 | Mobile Number | Accepts less than 10 digits |
| GYMINT_0013 | Mobile Number | Accepts alphabets |
| GYMINT_0015 | Email | Accepts email without @ symbol |
| GYMINT_0017 | Pincode | Accepts alphabets |
| GYMINT_0028 | Face Verification | Upload button not disabled when offline |
| GYMINT_0031 | Form Submit | Member added without First Name |
| GYMINT_0035 | UI | Typo – "Side Affects" should be "Side Effects" |

---

## Key Observations

1. Input validation is missing on most fields
2. Date of Birth does not prevent future dates
3. Member can be submitted without First Name — mandatory field bypass
4. Upload button remains active even when Face Service is offline
5. Typo found in Health Details label

---

## Suggestions

1. Add validation for all input fields
2. Disable Upload button when Face Service is offline
3. Fix typo in Health Details label
4. Enforce all mandatory fields before form submission
