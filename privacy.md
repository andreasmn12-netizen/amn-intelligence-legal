---
layout: default
title: Privacy Policy
---

# Privacy Policy

_Last updated: 21 October 2026_

This Privacy Policy explains how **AMN Intelligence** (Denmark) ("we", "us",
"our") handles personal data in connection with the **Daily Pour Cross-Poster**
application and related services (the "Service").

We are the data controller for the limited personal data processed by the
Service. This policy complies with the EU General Data Protection Regulation
(GDPR) and the Danish Data Protection Act.

## 1. What data we process

The Service is a backend automation that posts AMN Intelligence's own content
to AMN Intelligence's own social media accounts. The only personal data it
processes is the data required to perform that operation:

- **OAuth access tokens and refresh tokens** issued by TikTok, Instagram, and
  YouTube for the connected accounts. These are issued to AMN Intelligence by
  the respective platforms and allow the Service to publish on those accounts.
- **Account identifiers** (TikTok Open ID, Instagram Business Account ID,
  YouTube channel ID) returned by those platforms when a connection is made.
- **Operational logs** of each upload (timestamp, destination platform, video
  file name, resulting post ID). Logs do not contain information about viewers.

The Service does not collect, store, or process data about end users of
TikTok, Instagram, or YouTube who view or interact with the posted content.
Platform-level analytics (views, likes, comments) remain with the respective
platforms under their own privacy policies.

## 2. How data is stored

- Access tokens are stored as encrypted GitHub Actions Secrets inside the
  private GitHub repository that runs the Service. They are injected into
  the execution environment only at run time and are never written to disk
  outside the ephemeral runner.
- Operational logs are stored inside the same private repository and in
  Google Cloud project logs for the project `daily-pour-uploader`.

Access to these stores is restricted to the operator of AMN Intelligence.

## 3. Why we process this data (lawful basis)

We process the above data on the basis of **GDPR Article 6(1)(f)** – our
legitimate interest in operating our own content distribution infrastructure
for our own social media accounts.

## 4. Sharing with third parties

The Service shares data with the following processors only to the extent
necessary to deliver the Service:

- **Meta Platforms, Inc.** – Instagram Graph API, for uploading videos to our
  Instagram Business account.
- **TikTok Pte. Ltd.** – Content Posting API, for uploading videos to our
  TikTok account.
- **Google LLC** – YouTube Data API, Vertex AI (Gemini + Veo), and Google
  Cloud Logging, for video generation, upload, and operational logging.
- **GitHub, Inc.** – source code hosting, Actions runners, and Secrets storage.

Each of these providers acts as an independent controller or sub-processor
under its own terms. We do not sell or disclose data to any other party.

## 5. International transfers

Our processors are predominantly US-based companies with GDPR-adequate transfer
mechanisms in place (Standard Contractual Clauses, Data Privacy Framework).

## 6. Retention

- **Access tokens:** retained until the owner revokes them in the respective
  platform's app settings, or until AMN Intelligence rotates them.
- **Operational logs:** retained for up to 24 months, then deleted or
  overwritten.

## 7. Your rights

Under the GDPR you have the right to:

- request access to the personal data we hold about you;
- request correction of inaccurate data;
- request deletion of your data;
- object to processing based on our legitimate interests;
- lodge a complaint with the Danish Data Protection Agency
  ([Datatilsynet](https://www.datatilsynet.dk)).

Note: because the Service only processes data about AMN Intelligence's own
accounts and operations, requests from unrelated third parties will typically
be returned with "no personal data held".

## 8. Security

We follow industry best practices including encrypted secrets storage, HTTPS
in transit, scoped OAuth tokens, and principle-of-least-privilege access.

## 9. Changes

We may update this Privacy Policy from time to time. Material changes will be
reflected in the "Last updated" date at the top of this page.

## 10. Contact

For privacy-related questions or GDPR requests, contact
**andreasmn12 [at] outlook.dk**.
