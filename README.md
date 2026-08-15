# 🍱 FeedOne

### Verified Coordination & Accountability for Time-Sensitive Surplus Food

FeedOne is a verification, coordination, and accountability platform that connects **verified food donors with verified NGOs** to help surplus food move from availability to responsible handover before it becomes unusable.

## 🚀 What FeedOne Does

**Donor → Listing → NGO → Claim → Handover → Confirmation → Audit**

FeedOne turns an otherwise unstructured surplus-food donation process into a traceable digital workflow.

### ✨ Key Features

* 🔐 Authentication and role-based access
* ✅ Verified Donor & NGO profiles
* 🍱 Surplus food listing management
* ⏱️ Availability and expiry tracking
* 🤝 NGO food claiming
* 🔄 Handover lifecycle tracking
* 📋 Donor & NGO confirmations
* 🧾 Audit logging
* 🛡️ Row Level Security (RLS)
* ☁️ Cloud-backed PostgreSQL database

## 🏗️ Architecture

```text
                  FEEDONE
                     │
          ┌──────────┴──────────┐
          │                     │
      FRONTEND               BACKEND
   HTML / CSS / JS           Supabase
          │                     │
          │          ┌──────────┼──────────┐
          │          │          │          │
          │        Auth     PostgreSQL    RLS
          │                     │
          │          ┌──────────┼──────────┐
          │          │          │          │
          │      Profiles    Listings   Handovers
          │                                │
          │                           Audit Logs
          │
          └──────── Supabase API ──────────┘
```

## 🔄 Core Workflow

```text
Verified Donor
      ↓
Create Surplus Listing
      ↓
AVAILABLE
      ↓
Verified NGO
      ↓
CLAIM
      ↓
CLAIMED
      ↓
Handover
      ↓
Confirmation
      ↓
COMPLETED
      ↓
Audit Log
```

## 🛠️ Technology Stack

| Layer          | Technology               |
| -------------- | ------------------------ |
| Frontend       | HTML5, CSS3, JavaScript  |
| Backend        | Supabase                 |
| Database       | PostgreSQL               |
| Authentication | Supabase Auth            |
| Security       | Row Level Security (RLS) |
| Hosting        | Netlify                  |

## 🔐 Security

FeedOne uses Supabase Authentication and PostgreSQL Row Level Security to restrict data access based on authenticated users and their roles.

Examples include:

* Donors can manage their own listings.
* Verified users can perform permitted actions.
* NGO and donor workflows are separated by role.
* Database constraints prevent invalid workflow states.
* Operational actions can be recorded through audit logs.

## 🎯 Vision

FeedOne is not simply a food-donation listing platform.

Our goal is to build a **trusted coordination layer for time-sensitive surplus food**, ensuring that the right surplus reaches the right verified organization with a traceable handover.

> **From surplus to responsible handover — with verification, coordination, and accountability.**

## 📌 Hackathon Prototype

FeedOne is currently developed as a functional hackathon prototype demonstrating the complete donor-to-NGO coordination workflow using real authentication, database operations, security policies, handovers, and audit logging.

## 👥 Team

**Team FEEDONE**

Built for the hackathon with the goal of reducing avoidable surplus-food waste through technology-enabled coordination.
