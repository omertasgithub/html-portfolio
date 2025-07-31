1. Data Element Naming Rules
These rules ensure consistency, clarity, and usability of data names.

a. Use meaningful, business-relevant names
The name should describe what the data represents.

Avoid vague or overly technical terms.

❌ Bad: Fld01, Val1
✅ Good: CustomerEmail, InvoiceDate

b. Use consistent case and delimiters
Common naming conventions:

CamelCase: CustomerName

snake_case: customer_name

PascalCase: InvoiceNumber

Pick one and stick to it throughout the system.

c. No special characters or spaces
Use underscores or capitalization instead of spaces.

Avoid characters like /, -, @, #, etc.

d. No abbreviations unless standardized
Avoid using short forms unless they are widely accepted.

If used, document them in a glossary.

❌ Bad: CustNo (unless Cust is a standard abbreviation)
✅ Good: CustomerNumber

e. Avoid system-specific prefixes or suffixes
Don't use table-specific or tool-specific terms in element names (tbl_, fld_, etc.).

f. Avoid reserved keywords
Ensure the name doesn’t conflict with SQL or programming language keywords (like SELECT, FROM, IF, etc.).

✅ 2. Data Element Description Rules
Descriptions provide context and are essential for metadata management and lineage tracing.

a. Use full sentences or complete phrases
Be clear and complete.

Explain what the data is, how it is collected, and its business meaning.

✅ Example:
CustomerEmail: The primary email address used by the customer for communication and login. Collected during account registration.

b. Avoid repeating the name in the description
Focus on purpose or usage, not restating the name.

❌ Bad: “Customer name is the name of the customer.”
✅ Good: “The full legal name of the customer as entered during onboarding.”

c. Include units, format, and valid values (if applicable)
Mention if the field is a percentage, currency, ISO date, etc.

List valid ranges or values if discrete.

✅ Example:
OrderStatus: Current status of the order. Valid values include: Pending, Shipped, Delivered, Cancelled.

d. State the source and frequency (optional but helpful)
Mention where the data comes from and how often it updates.

✅ Example:
CustomerSegment: Marketing-assigned segment classification. Derived from Salesforce weekly.

✅ 3. Optional Governance Guidelines
Data Owner & Steward Assignment: Assign roles for accountability.

Data Sensitivity Tag: Indicate if PII, PHI, or confidential.

Business Rule Link: Describe rules or logic used to derive this field.

Data Type & Format: Include technical metadata (e.g., VARCHAR(50), DATE, etc.).

🧾 Example (Put in Data Dictionary)
Data Element	Description	Data Type	Format	Valid Values	Source	Frequency
CustomerEmail	Primary email for customer contact and login.	VARCHAR	Email format	—	Registration	Real-time
OrderStatus	Status of the order.	VARCHAR	Text	Pending, Shipped, Delivered	Order System	Hourly
InvoiceAmount	Total amount charged on the invoice including taxes.	DECIMAL	Currency	≥ 0	Billing System	Daily
