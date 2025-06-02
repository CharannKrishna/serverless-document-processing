# 🗂️ Serverless Document Processing

A fully serverless document ingestion and processing pipeline using AWS CDK (TypeScript), Lambda, S3, and Amazon Textract.

---

## 📦 Features

- 🔁 Event-driven document processing via S3 triggers
- 🧠 Text, form, and table extraction with Amazon Textract
- ⚡ Scalable and serverless with AWS Lambda
- 💡 Written using AWS CDK in TypeScript

---

## 🧱 Architecture

S3 Bucket (Upload)
↓
Lambda: document-processor.ts
↓
Amazon Textract API
↓
Lambda: textract-handler.ts (optional post-processing)

yaml
Copy
Edit

> 🔽 You can replace this with a visual PNG/SVG if preferred.

---

## 📁 Folder Structure

serverless-document-processing/
├── bin/
│ └── app.ts # CDK app entry
├── lib/
│ └── document-stack.ts # Infrastructure stack
├── lambdas/
│ ├── document-processor.ts # Triggered on S3 upload
│ ├── textract-handler.ts # Handles Textract result (optional)
├── test/
│ └── document-stack.test.ts # Unit test for stack
├── package.json
├── tsconfig.json
└── README.md

yaml
Copy
Edit

---

## 🚀 Deploy Instructions

### ✅ Prerequisites

- Node.js v16+
- AWS CDK v2 installed: `npm install -g aws-cdk`
- AWS CLI configured (`aws configure`)
- Git installed and linked to GitHub

### 🛠 Setup

Go to Terminal
git clone https://github.com/CharannKrishna/serverless-document-processing.git
cd serverless-document-processing
npm install
cdk bootstrap
cdk deploy
