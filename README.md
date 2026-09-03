# Criminal Risk Assessment Request - ODK XLSForm

## Video Demonstration

The assignment demonstration video explains the XLSForm structure, form logic, validations, and working preview.

[Click here to view the assignment demonstration video](https://drive.google.com/file/d/1P2U70CDKb1bz3YZNr7kUiELLFHGRl1B0/view?usp=sharing)


## Overview

This project contains an ODK XLSForm developed from the provided **Criminal Risk Assessment Request** PDF as part of the Odiona Technologies internship selection assignment.

The original PDF contains personal information fields, identification details, consent information, agency details, and risk assessment information. The objective of this assignment was to convert that structure into a functional digital form using the XLSForm standard so that it can be validated and previewed using ODK tools.

## Objective

The main objective of this project was to:

- Convert the provided PDF form into an ODK-compatible XLSForm.
- Maintain the structure and required information from the original form.
- Use appropriate XLSForm question types.
- Add validations wherever required.
- Add conditional logic for dependent fields.
- Test the completed form using the ODK XLSForm Online tool and Enketo preview.

## XLSForm Structure

The XLSForm contains three main sheets:

### 1. survey

The `survey` sheet contains the complete form structure and logic.

It includes:

- Text fields for names, addresses, phone numbers, and agency details.
- Date fields for Date of Birth, Request Date, and previous assessment date.
- Select-one questions for fields such as gender and risk assessment reason.
- Select-multiple questions for identification types.
- Informational notes for consent and legal information.
- Groups for organizing related sections of the form.
- Required field rules.
- Conditional display logic using the `relevant` column.
- Validation rules using the `constraint` column.
- Calculation logic for displaying the name of the person being assessed.

### 2. choices

The `choices` sheet contains the answer options used by selection-based questions.

It includes:

- Gender options.
- Identification type options.
- Risk assessment reason options.

These lists are linked to the corresponding `select_one` and `select_multiple` questions in the survey sheet.

### 3. settings

The `settings` sheet contains the basic form configuration such as:

- Form title.
- Form ID.
- Version.

## Form Sections

The completed XLSForm is organized into the following sections:

### Consent

The consent section contains the consent and information text from the original Criminal Risk Assessment Request form.

### Personal Information

This section collects details such as:

- First name.
- Second name.
- Last name.
- Date of birth.
- Gender.
- Other names used.
- Current address.
- Phone number.
- Place of birth.

### Identification

The identification section allows the user to select the identification documents provided.

The form requires at least two pieces of identification.

Additional conditional fields are used for:

- Other identification type.
- Manitoba Driver's Licence number.

### Agency and Risk Assessment Information

This section contains:

- Name of the person being assessed.
- Agency submitting the request.
- Reason for risk assessment.
- Assigned worker.
- Date of previous criminal risk assessment.
- Submitting designate details.
- Phone number.
- Email.
- Fax number.
- Request date.

## Form Logic and Validation

Several XLSForm features were used to improve the functionality of the form.

### Minimum Identification Validation

The original form requires two pieces of identification.

A constraint was added so that the user must select at least two identification options before the form can be successfully validated.

### Conditional Other Identification Field

When the user selects **Other** as an identification type, an additional field is displayed so that the identification can be specified.

### Conditional Driver's Licence Field

When **MB Driver's License with Photo** is selected, an additional field is displayed for entering the licence number.

### Automatic Name Display

The name entered in the personal information section is used in the agency section so that the name shown there matches the information entered earlier in the form.

### Conditional Consent Information

For applicable risk assessment reasons such as:

- Place of Safety.
- Kinship.
- Customary Care Agreement.

the form displays a note indicating that consent is required.

### Email Validation

The Designate Email field contains validation to ensure that the entered value follows a valid email format.

### Date Validation

Date validation is used to prevent invalid future dates where appropriate.

## Testing

The completed XLSForm was downloaded as a Microsoft Excel `.xlsx` file and uploaded to the ODK XLSForm Online tool.

The form was then tested using the Enketo preview.

The following functionality was checked:

1. The XLSForm converts successfully without errors.
2. All main sections of the form are displayed.
3. Selection fields display the correct choices.
4. Selecting **Other** displays the additional identification field.
5. Selecting **MB Driver's License with Photo** displays the licence number field.
6. The minimum two-identification validation works correctly.
7. Conditional consent information is displayed for the appropriate risk assessment reasons.
8. Invalid email addresses are rejected.
9. Date validation works correctly.
10. The name of the person being assessed is displayed correctly in the agency section.
11. Required fields are validated correctly.

## How to Test the XLSForm

The form can be tested using the ODK XLSForm Online tool.

1. Download the `Criminal_Risk_Assessment_Request.xlsx` file from this repository.
2. Open the ODK XLSForm Online tool.
3. Upload the `.xlsx` file.
4. Convert the XLSForm.
5. Open the generated Enketo preview.
6. Fill the form and test the validations and conditional fields.

## Project Files

- `Criminal_Risk_Assessment_Request.xlsx` - Completed ODK XLSForm.
- `README.md` - Project documentation.

## Tools Used

- Google Sheets
- ODK XLSForm
- ODK XLSForm Online
- Enketo
- GitHub

## Conclusion

The provided Criminal Risk Assessment Request PDF was converted into a structured and functional ODK XLSForm.
The final form includes appropriate question types, grouped sections, validation rules, conditional fields, and selection options. The completed XLSForm was tested using the ODK XLSForm Online tool and Enketo preview before submission.