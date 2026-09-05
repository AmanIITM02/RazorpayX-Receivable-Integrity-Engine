# 🛡️ RazorpayX & Capital — AI Receivable Integrity Engine

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Target: Razorpay](https://img.shields.io/badge/Target-RazorpayX%20%26%20Capital-blueviolet.svg)](https://razorpay.com)

An enterprise-grade, multi-modal AI microservice designed to detect **Accounts Payable duplicate vendor payouts** and **cross-lender double-financing fraud** in real time.

Engineered specifically for **RazorpayX** (Vendor Payments) and **Razorpay Capital** (Line of Credit) to plug quiet balance-sheet revenue leaks before payout execution.

---

## 📌 Executive Summary & Problem Statement

In B2B payments and supply-chain finance, legacy database validation relies heavily on exact-string matching and manual audits. This creates two catastrophic vulnerability vectors:

# Clone the repository
git clone [https://github.com/AmanITM02/RazorpayX-Receivable-Integrity-Engine.git](https://github.com/AmanITM02/RazorpayX-Receivable-Integrity-Engine.git)
cd RazorpayX-Receivable-Integrity-Engine

# Install system OCR dependencies (Linux/Debian)
sudo apt-get install -y tesseract-ocr poppler-utils

# Create virtual environment and install requirements
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook RazorpayX_Receivable_Integrity_Engine.ipynb

{
  "audit_timestamp": "2026-09-05T14:30:00Z",
  "final_decision": "REJECTED",
  "risk_score": 0.98,
  "extracted_entities": {
    "invoice_number": "INV-2026-001A",
    "vendor_name": "Acme Industrial Supplies Pvt Ltd",
    "total_amount": "150000.00",
    "buyer_gstin": "27AAACA12341ZV"
  },
  "policy_checks": {
    "razorpayx_ap_duplicate": {
      "is_duplicate": true,
      "matched_invoice_id": "INV-2026-001",
      "similarity_score": 92.5,
      "risk_reason": "High metadata similarity with existing RazorpayX bill"
    },
    "razorpay_capital_double_pledged": {
      "already_funded": false,
      "commitment_hash": "4a2f8b9e1d3c5a7b9e0f2a4c6e8d1b3f5a7c9e1d3f5a7b9c0e2d4f6a8b0c2d4e",
      "action_plan": "Clear: No external double-financing record found."
    }
  }
}

