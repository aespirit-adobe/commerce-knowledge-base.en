---
title: Adobe Commerce status column missing exported products CSV file
description: This article provides a solution for the issue when you cannot locate the status column (i.e., indicating whether the product is *Enabled* or *Disabled*) in the CSV file containing exported products.
exl-id: 3cbe1e6c-fc73-4331-add7-1ebcb28a4580
---
# Adobe Commerce status column missing exported products CSV file 

This article provides a solution for the issue when you cannot locate the status column (i.e., indicating whether the product is *Enabled* or *Disabled*) in the CSV file containing exported products. The status of the product is indicated by the product_online column.

## Affected products and versions

Adobe Commerce (all deployment methods) all [supported versions](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf)

## Issue

You are unable to locate the status column in the CSV file containing exported products. So, for example, you export a CSV of all SKUs, with their status, but the table appears to be missing the status column. 

<u>Steps to reproduce:</u>

1. In the Commerce Admin, select **System**, under *Data Transfer* select **Export**.
1. In the *Export Settings* section, select on the *Entity Type* drop down **Products**.
1. Search for *status*, listed under Attribute Code. You see that attribute code in the list of available attributes (*Enable Product*).
1. Click on **Export**.

<u>Expected result:</u>

In the CSV file that you just exported, you see a column labeled *status*.

<u>Actual result:</u>

You do not see a column labeled *status* in the exported csv file.  

## Cause

The product's status attribute has been renamed in the CSV file. It is now the product_online column.

## Solution

1. Select **System** under *Data Transfer* select **Import**.
1. Click **Download Sample File**.
1. You can see the product_online column in the CSV file.

## Related reading

* [Working with CSV files](https://docs.magento.com/user-guide/system/data-csv.html) in our user guide.
* [Product Export Attributes Reference](https://docs.magento.com/user-guide/system/data-attributes-product.html) in our user guide.