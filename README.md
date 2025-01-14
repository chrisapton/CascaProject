## Casca Project
# **Financial Document Analysis for Loan Eligibility**

This project processes financial documents (e.g., bank statements) to evaluate loan eligibility using OpenAI's GPT-4 model (`gpt-4o`). The workflow includes converting PDF files into images, organizing them into folders, and analyzing the data using GPT-4 along with a custom text prompt.

---

## **Features**
- **PDF to Image Conversion**:
  - Converts each page of a PDF document into high-resolution images.
  - Stores the images in separate folders, with one folder per PDF.

- **Custom Financial Analysis**:
  - Sends the images to OpenAI's `gpt-4o` model for analysis.
  - Includes a custom text prompt to extract key financial insights:
    - Total monthly deposits and withdrawals.
    - Identification of recurring expenses (e.g., rent, employee salaries, utilities).
    - Detection of outstanding loans or liabilities.
    - A final evaluation of loan eligibility based on spending patterns and financial health.

- **Automated Workflow**:
  - Handles multiple PDFs and folders seamlessly.
  - Encodes images into base64 for efficient transfer to the GPT model.

---

## **Workflow**
1. **PDF Processing**:
   - Input: A folder containing one or more PDF files.
   - Output: Each PDF is converted into a folder containing images of its pages.

2. **Image Preprocessing**:
   - Converts images to grayscale and applies thresholding to enhance text readability.
   - Prepares the images for OCR and GPT processing.

3. **GPT Analysis**:
   - Encodes images into base64 format and sends them to `gpt-4o`.
   - A custom text prompt guides GPT to extract financial insights and make loan recommendations.

4. **Output**:
   - A detailed report for each PDF, including:
     - Monthly cash flow summary.
     - Key recurring expenses.
     - Loan eligibility decision and reasoning.

---

### **Prerequisites**
- Python 3.12 or later.
- OpenAI API Key with access to `gpt-4o`.
- Required Python libraries
