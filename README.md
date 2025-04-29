# Postwave - Personalized Email Automation Tool

[![Download Postwave Installer](https://img.shields.io/badge/Download-Postwave%20Installer-blue?style=flat&logo=github&logoColor=white)](https://github.com/pratap-raghav/Postwave-Installer/releases/download/Postwave-Installer/Postwave-Installer.exe)

![Newpostwave](https://github.com/user-attachments/assets/626a5840-64b2-4d94-89ff-e09acc6f1263)

**Postwave** is a powerful, desktop-based email automation tool designed to streamline the process of sending personalized, large-scale email campaigns with attachments. Built with **Python** and using **CustomTkinter** for a modern and user-friendly GUI, Postwave combines technical efficiency with simplicity for end-users who want a no-code solution for automating email workflows.

---

## Login Interface
![1](https://github.com/user-attachments/assets/68c78cf3-62ca-43e4-8c69-4a8edff26a8b)

## Main Dashboard Overview
![2](https://github.com/user-attachments/assets/9a93beaf-c51b-447c-a046-70755f552036)

## Example of a Personalized Email Received
![output](https://github.com/user-attachments/assets/758f5b75-955b-4280-8cde-cf798bf1323d)

## Sample Excel Data
![1](https://github.com/user-attachments/assets/a45bd3b6-0b02-4135-8c09-a061cf8c0a73)

---

## Key Features

- **Excel-Driven Personalization**: Import recipient data from Excel and use fields like `{name}`, `{company}`, etc.  
- **Attachment Support**: Attach same or user-specific files based on Excel data.  
- **Intelligent Message Templating**: Personalize messages with dynamic placeholders.  
- **SMTP Integration**: Easy configuration for Gmail SMTP, with error logging.  
- **Delivery Report**: Automatic summary log of email delivery status.  
- **Intuitive GUI**: Built with CustomTkinter for a no-code experience.

---

## Technical Stack

- **Frontend**: Python + CustomTkinter  
- **Backend**: Core Python libraries (`smtplib`, `openpyxl`, `email`, `os`)  
- **File I/O**: `.xlsx` & CSV support  
- **Architecture**: Modular, extensible for future API integrations

---

## Use Cases

- HR teams sending **offer letters or certificates**  
- Educators emailing **grades or documents**  
- Businesses doing **follow-ups or bulk outreach**  
- Developers building custom automations with Postwave core

---

## Why Postwave?

Postwave is local, offline-first, and privacy-conscious. No external dashboards or third-party logins — just your Excel file, message, and a click to send.

Whether you're an educator, admin, or techie — Postwave empowers **personalized communication at scale**.

---

## In-Depth Technical Overview

### Core Architecture

- **Language**: Python 3  
- **GUI Framework**: [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter)  
- **Email Handling**: `email`, `smtplib`, `ssl` for secure message creation  
- **Excel Parsing**: `openpyxl` for row-wise personalization  
- **File Management**: `os`, `pathlib` for dynamic attachments  
- **Templating Engine**: Placeholder replacement like `{name}`, `{email}`

### SMTP & Email Dispatch

- **Configurable SMTP Settings**  
- **Failure Recovery** via try-except logging  
- **Rate Control** support to prevent throttling  
- **Logging**: Local `.log` file of sent/skipped/failed emails

### Input Format & Processing

- **Input File**: `.xlsx` or `.csv` with recipient data  
- **Attachments**:  
  - *Global*: One file for all  
  - *Per User*: Path from Excel column  
- **Email Body**: With `{placeholders}` for personalization

### Developer Features

- Modular code structure  
- Extensible architecture for Gmail API, retry queues, analytics  
- Local-only operation for privacy

---

## Ideal For

- **Internal teams** automating document delivery  
- **Educators** sharing results or resources  
- **Businesses** managing campaign follow-ups  
- **Developers** customizing scalable email solutions

---
