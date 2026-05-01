# 🗺️ AflonWeb Project Mapping & Current Status

This document outlines the entire architectural map of the new AflonWeb platform, the phased execution plan, and exactly where the project stands as of this moment.

## 1. Project Vision
To transform AflonWeb from a static, template-based brochure website into a **fully automated Digital Agency & Hosting Platform** (similar to WhoGoHost or Upperlink). Customers will be able to buy domains, purchase hosting, and order agency services 24/7 without manual intervention.

## 2. Architectural Map

The platform is split into two distinct, decoupled systems:

### A. The Storefront (The Frontend)
*   **Purpose:** Marketing, SEO, Service display, and initial domain search.
*   **Tech Stack:** React (Next.js), Framer Motion, Custom CSS Modules.
*   **Design Vibe:** "Tech Dark" — inspired by Webflow and Vercel. Deep black backgrounds, neon glowing gradients, glassmorphism cards.

### B. The Engine Room (The Backend)
*   **Purpose:** Automated billing, server provisioning, and domain registration.
*   **Server Infrastructure:** Managed Reseller Hosting Plan (via InMotion).
*   **Automation Software:** WHMCS (Web Host Billing & Automation Platform).
*   **Integrations:** 
    *   **NiRA API:** For automated `.ng` domain registration.
    *   **WHM API:** For automated cPanel creation on the server.
    *   **Paystack/Flutterwave:** For secure Naira payment processing.

## 3. Project Execution Outline (4 Phases)

*   **[ PHASE 1 ] Frontend UI Build & Design System**
    *   Set up Next.js repository.
    *   Establish CSS variables and global theme.
    *   Build animated Hero section and Bento Box service cards.
    *   Replace legacy dummy text with aggressive, premium copywriting.
*   **[ PHASE 2 ] Infrastructure Upgrade**
    *   Obtain approval to upgrade InMotion plan from "WP Power" to "Reseller".
    *   Install and configure WHMCS on the new server.
    *   Connect WHMCS to NiRA and Paystack.
*   **[ PHASE 3 ] System Integration**
    *   Create service products (SEO, Web Design, Hosting) inside WHMCS.
    *   Link the "Buy Now" buttons on the Next.js Storefront directly to the secure WHMCS checkout carts.
    *   Theme WHMCS to visually match the Next.js Storefront.
*   **[ PHASE 4 ] Testing & Launch**
    *   Run test transactions with dummy credit cards.
    *   Ensure automated cPanel creation and Welcome Emails fire correctly.
    *   Go Live.

---

## 4. 📍 CURRENT STATUS: Where we are right now

We are currently executing **Phase 1** while waiting for clearance to begin **Phase 2**.

**What has been completed:**
1.  **Strategy Approved (Locally):** We have determined that the "Managed Reseller + WHMCS" route is the safest, most profitable path forward, avoiding the high overhead of unmanaged cloud servers (like Kamatera).
2.  **Business Case Documented:** Generated `AflonWeb_Hosting_Strategy.docx` to present the financial and strategic case to management.
3.  **Frontend Initialized:** The Next.js React application has been successfully created in the `frontend/` directory.
4.  **Design System Drafted:** `globals.css` has been updated with the Webflow-inspired color palette.
5.  **Initial Code Written:** `page.tsx` and `page.module.css` have been created, featuring a Framer Motion-powered animated hero section.
6.  **Documentation:** `README.md` created for GitHub deployment.

**Next Immediate Steps:**
1.  Gather visual inspiration links (Awwwards, Webflow sites, etc.) to refine the UI.
2.  Wait for management's "Green Light" on the InMotion upgrade budget (~$35-$45/mo).
3.  Continue building out the individual service pages on the Next.js frontend.
