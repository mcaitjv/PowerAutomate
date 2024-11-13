# Power BI with Power Automate Integration

This repository contains the necessary resources to set up a Power BI report that integrates with Power Automate. The Power BI report includes a button within it, which when clicked, triggers a Power Automate flow designed to refresh the dataset used by the report. This solution is useful for initiating on-demand refreshes of your Power BI reports, providing updated data visualizations based on the latest available data.

## Repository Contents

- `powerAutomateRefresh.pbix` - The Power BI report file containing the visualization and embedded Power Automate button.
- `PowerBIDatasetRefresh_20241113083848.zip` - Export of the Power Automate flow used to refresh the Power BI dataset.
- `powerautomateRefresh.xlsx` - Sample dataset used in the Power BI report.

## Getting Started

Follow these steps to get started with this project:

### Prerequisites

- Access to Microsoft Power BI Service with permissions to create and publish reports.
- Access to Microsoft Power Automate with permissions to create and manage flows.
- Microsoft Excel or compatible software to view and modify the sample xlsx data.

### Setup Guide

#### Power BI Report

1. **Open Power BI Desktop**.
2. **Import the PBIX File**:
   - Go to `File > Open` and select `powerAutomateRefresh.pbix`.
3. **Check Data Source**:
   - Make sure the data source points to the correct location of `powerautomateRefresh.xlsx`.
   - Update the source path if necessary under `Transform Data > Data Source Settings`.

#### Power Automate Flow

1. **Import the Flow**:
   - Sign in to your [Power Automate](https://flow.microsoft.com) account.
   - Navigate to `My flows > Import` and upload `PowerBIDatasetRefresh_20241113083848.zip`.
   - Follow on-screen instructions to set up connections and credentials.

2. **Link Power BI Button to Flow**:
   - Ensure the Power BI button is correctly configured to trigger this flow. This should be set up under the Action settings of the button in your Power BI report.

#### Setup Dataset Refresh

1. **Configure Dataset**:
   - Ensure the dataset in Power BI is set to allow API refreshes and that the correct permissions are configured.

#### Publishing Report

1. **Publish Your Report**:
   - Once all configurations are verified, publish the report to Power BI Service by selecting `File > Publish > To Power BI`.

### Testing

- **Test the Button in Power BI**:
  - Open the report in Power BI Service.
  - Add sample data into the powerautomateRefresh.xlsx
  - Click the button embedded in the report to trigger the refresh and observe if the dataset refreshes as expected.

---
