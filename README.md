# Control Tower Inbound Dashboard - Pure Frontend Guide

This repository contains the Control Tower Inbound Dashboard, configured to run as a **pure frontend application** with rich simulated sample data. No python servers or databases are required.

## How to Run

1. Open the workspace folder in your file explorer:
   `c:\Users\AxeGlobal Ai\Desktop\NVO_warehouse`
2. Locate the file:
   [CT Template.html](file:///c:/Users/AxeGlobal%20Ai/Desktop/NVO_warehouse/CT%20Template.html)
3. Double-click it to open it directly in any modern web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, or Safari).

## Simulated Features

Because the app intercepts all network requests client-side, the following features work out-of-the-box:

- **Interactive Filters**: Filter by Operation Type (Inbound/Outbound), Warehouse, Client, Status, Date range, or free-text search.
- **Dynamic KPI Cards & Gauges**: Calculate metrics on-the-fly based on the filtered dataset.
- **Charts & Drill-downs**: Click on weekly volumes or warehouse bars to open detailed shipment listings.
- **Standard Operating Procedures (SOP)**: Explore, search, add, or delete procedural steps.
- **CT Entry Excel-like Grid**: Edit data entries directly in the grid view. All edits are persisted in your browser's `localStorage`.
