# DynamoDB Table Cleanup Script

## Overview

This script is designed to delete all items from multiple DynamoDB tables associated with a specific AppSync ID. It is useful when you need to clean up large amounts of data across many DynamoDB tables. The script scans each relevant table and removes all items, ensuring efficient batch deletion.

The script can handle pagination when there are more than 100 tables, and it will process all of them by scanning each one and deleting items in batches.

## Features

- **Identify Tables**: The script searches for DynamoDB tables whose names contain a specified AppSync ID.
- **Batch Deletion**: It deletes items from the tables in batches to optimize performance.
- **Pagination Support**: Handles pagination if more than 100 tables are present.
- **Error Handling**: The script includes error handling to log any issues encountered during the process.

## Requirements

- Python 3.x
- AWS Lambda (for serverless execution) or local testing using AWS SDK for Python (Boto3).
- Proper AWS IAM permissions for DynamoDB actions (list, scan, delete).

## Installation

1. Clone or download this repository to your local machine.

2. Ensure that you have the **Boto3** library installed. You can install it via pip if you're running this script locally:
