# Software Developer Job Application Form - Assignment 02

## Project Overview
A multi-section Software Developer Job Application Form built with pure semantic HTML5. It collects personal details, role preferences, and application documents while enforcing native browser-side form validation.

## Form Elements & Input Types Used
- **Grouping & Accessibility:** Structured into logical blocks using `<fieldset>` and `<legend>`, with every form control paired to a descriptive `<label for="...">`.
- **Text-Based Inputs:** `text` (Full Name), `email` (Email Address), `password` (Account Password), `tel` (Phone Number), `url` (Portfolio/GitHub URL), and `number` (Years of Experience).
- **Choice Inputs:** `radio` buttons for single-choice Work Mode, `checkbox` inputs for multiple Technical Skills, `<select>` with `<option>` for Role selection, and `<input list="...">` paired with `<datalist>` for Preferred City autocomplete.
- **Specialized Inputs:** `date` (Available Start Date), `time` (Preferred Interview Time), `file` (Resume/ID Upload with `enctype="multipart/form-data"`), `range` (Coding Proficiency slider), `color` (Profile/Badge Color picker), and `<textarea>` (Cover Letter).

## Validation & Controls
- **HTML5 Validation Attributes:**
  - `required`: Enforced on mandatory fields (Full Name, Email, Password, Phone, Work Mode, Role, Start Date, and Resume Upload).
  - `placeholder`: Provides clear format hints inside text, email, phone, URL, number, datalist, and textarea inputs.
  - `min` & `max`: Restricts Years of Experience (`0` to `40`), Coding Proficiency slider (`1` to `10`), and Start Date bounds.
  - `minlength`: Enforces at least 3 characters for Full Name, 8 characters for Account Password, and 20 characters for the Cover Letter.
  - `pattern` & `title`: Validates a 10-digit mobile number (`[0-9]{10}`) with a helpful tooltip prompt.
- **Action Buttons:** Includes `<button type="submit">` to validate and submit the form and `<button type="reset">` to clear all entered data.

## How to View
1. Navigate to the `assignment-02/` folder.
2. Open `index.html` directly in any web browser, or launch it using the **Live Server** extension in VS Code.