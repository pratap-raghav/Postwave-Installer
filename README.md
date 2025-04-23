![Newpostwave](https://github.com/user-attachments/assets/626a5840-64b2-4d94-89ff-e09acc6f1263)

---

# Postwave - Personalized Email Automation Tool

**Postwave** is a powerful, desktop-based email automation tool designed to streamline the process of sending personalized, large-scale email campaigns with attachments. Built with **Python** and using **CustomTkinter** for a modern and user-friendly GUI, Postwave combines technical efficiency with simplicity for end-users who want a no-code solution for automating email workflows.

## Key Features

- **Excel-Driven Personalization**: Users can import recipient data from an Excel spreadsheet. Fields like name, email address, and custom variables (e.g., company, product, etc.) are used to personalize each email.  
- **Attachment Support**: Postwave allows attaching files (e.g., invoices, certificates, PDFs, etc.) to each email — either the same file for all recipients or unique files per user based on file paths listed in the Excel file.  
- **Intelligent Message Templating**: Dynamic placeholders like `{name}`, `{company}` or custom fields are replaced in real-time to create personalized messages that feel human-written.  
- **SMTP Integration**: Seamless configuration for sending emails via SMTP (Gmail only). Includes error-handling and logging for delivery status.  
- **Delivery Report**: Built-in logging system to generate a summary of sent emails, failures, and skipped rows, helping users quickly diagnose issues or verify success.  
- **Intuitive GUI**: A modern, drag-and-drop friendly interface designed with CustomTkinter ensures that non-technical users can set up and execute campaigns effortlessly.  

## Technical Stack

- **Frontend**: Python with **CustomTkinter**  
- **Backend**: Python core libraries (`smtplib`, `openpyxl`, `email`, `os`)  
- **File I/O**: Reads and parses `.xlsx` files; supports CSV integration as well  
- **Architecture**: Modular, with extensibility for future integration with APIs (e.g., Gmail API, SendGrid)  

## Use Cases

- HR teams sending **offer letters or certificates** in bulk  
- Educators emailing **grade sheets or documents** to students  
- Businesses conducting **personalized outreach or follow-ups**  
- Developers building custom tools on top of Postwave’s core architecture  

## Why Postwave?

Unlike traditional email platforms, Postwave runs **locally** without requiring third-party logins, giving you full control over data privacy. It eliminates the need to repeatedly upload files or manage lists online — simply load your Excel file, craft your message, and press send.

Whether you're a solo entrepreneur, an office manager, or a tech-savvy developer, Postwave gives you **speed**, **control**, and **flexibility** to communicate with your audience at scale — without compromise.

---

## In-Depth Technical Overview

**Postwave** is a Python-based, desktop GUI application built for automating personalized email workflows at scale. Designed with modularity and extensibility in mind, Postwave leverages key Python libraries to enable data-driven message generation, secure file-based attachments, and efficient SMTP-based email dispatch.

### Core Architecture

- **Language**: Python 3  
- **GUI Framework**: [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) for a modern, theme-aware interface  
- **Email Handling**: Uses the `email`, `smtplib`, and `ssl` modules to construct MIME-compliant messages and securely send them via SMTP  
- **Excel Parsing**: Powered by `openpyxl` for `.xlsx` files; supports row-wise iteration and dynamic field mapping  
- **File Management**: Uses `os`, `pathlib`, and dynamic resolution of attachment paths per user (e.g., `./attachments/{UniqueID}.pdf`)  
- **Templating Engine**: Custom string substitution for placeholders like `{name}`, `{email}`, `{product}` based on Excel column headers  

### SMTP & Email Dispatch

- **Configurable SMTP Settings**: Supports TLS/SSL ports, login authentication, sender identity  
- **Failure Recovery**: Graceful error handling with per-email try-catch and exception logging  
- **Rate Control**: Optional delay between emails to avoid SMTP throttling  
- **Logging**: Local generation of delivery reports with metadata (e.g., timestamp, status, skipped rows)  

### Input Format & Processing

- **Input File**: `.xlsx` format with required columns like `name`, `email`, and optional columns for dynamic values and attachments  
- **Attachments**:  
  - *Global*: A single file attached to all emails  
  - *Per User*: Attachment path specified per row in Excel  
- **Email Body**: Composed with placeholders resolved per recipient using string formatting (`str.format()`-style)  

### Developer Features

- **Modular Codebase**: Clean separation between UI logic, SMTP engine, templating logic, and file operations  
- **Extensibility**: Designed to support future plugins (e.g., Gmail API integration, retry queues, analytics dashboard)  
- **Local-Only Runtime**: No internet dependency beyond SMTP; ensures full control and privacy over input/output data  

### Ideal For

- Internal teams automating document dispatch (HR, education, operations)  
- Developers building internal tooling for email workflows  
- Use cases where cloud-based email platforms are restricted or overkill  

---
