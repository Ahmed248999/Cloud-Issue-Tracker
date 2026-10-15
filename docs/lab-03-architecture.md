# Lab 3 — Cloud Issue Tracker Architecture

## 1. Application Goal

To create a website that tracks cloud-based issues and records them to be resolved later .

## 2. Functional Scope
* To issues card to record issues.
* To remove card to if the issue is resolved

## 3. Request Flow

VIEW ISSUES
Page load → GET /api/issues → API → Data layer
 ← Render list ← 200 + JSON array ←───┘

 VIEW ISSUES
Page load → GET /api/issues → API → Data layer
 ← Render list ← 200 + JSON array ←───┘

 CHANGE STATUS
Button → PATCH /api/issues/{id}/status → API validation → Data layer
 ← Re-render issue 

## 4. Trust Boundaries
USER-CONTROLLED SIDE APPLICATION-CONTROLLED SIDE
Browser input ───── HTTP request ─────▶ REST API ─────▶ Data
    ▲                                      │
    └────────── JSON response ◀────────────┘