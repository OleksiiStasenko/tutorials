---
title: AlexS_2
description: Create a database table in SAP Cloud Platform ABAP Environment and prefill it with data.
primary_tag: products>sap-cloud-platform--abap-environment  
tags: [  tutorial>beginner, topic>abap-development, products>sap-cloud-platform]
time: 10
---

## Prerequisites  
- You must have an SAP Cloud Platform ABAP Environment user.

## Details
### You will learn
- How to create a database table
- How to `prefill` your database table with data

In this tutorial, wherever `XXX` appears, use a number (e.g. `000`).

---

[ACCORDION-BEGIN [Step 1: ](Open Eclipse)]
Open Eclipse, and select **New** > **ABAP Package**.

!![Open Eclipse](cat.png)
 
[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 2: ](Create ABAP package)]
  1. Maintain following information in the appearing dialog and  click **Next**.

      - Name: **`Z_Booking_XXX`**
      - Description: **Package Booking**

      ![Create ABAP package](package2.png)

  2. Move on with **Next**.

      ![Create ABAP package](package3.png)

  3. Select transport request and click **Finish**.

      ![Create ABAP package](package4.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 3: ](Open ABAP repository object)]
Right-click on your package and navigate to **New** > **Other ABAP Repository Object** from the appearing context menu.

![Open ABAP repository object](object.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 4: ](Create database table)]
  1. Search for **database table**, select the appropriate entry and click **Next**.

      ![Create database table](db.png)
  2. Maintain the required information and click **Next**.

      - Name: **`ZTBOOKING_XXX`**
      - Description: **Table Booking**

      ![Create database table](db2.png)

  3. On the next dialog, provide a transport request and click **Finish**.

      ![Create database table](db3.png)

  4. Check result. An empty table is now created.

      ![Check code](empty.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 5: ](Define database table)]
  1. Define the table columns (client, booking, `customername`, `numberofpassengers`, …). Specify client and booking as key fields, and the field `currencycode` as currency key for cost as displayed below. The table annotations (beginning with @) remain unchanged. For that, you can copy the database table definition provided below.

    ```AB
    @EndUserText.label : 'Demo: Booking Data
    ```

  2. Save and activate the database table.

      ![Define database table](saveandactivate.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 6: ](Create ABAP class)]
  1. Create a class in order to `prefill` our created database table. Right-click on your package and navigate to **New** > **ABAP Class** in the appearing context menu.

      ![Create ABAP class](class.png)

  2. Provide the required information and click **Next**.

    - Name: **`ZCL_GENERATE_BOOKINGS_XXX`**
    - Description: **Class to generate bookings**

      ![Create ABAP class](class2.png)

  3. Provide a transport request and click **Finish**.

      ![Create ABAP class](class3.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 7: ](Replace source code)]
  1. Replace the source code of your class with the one provided below:

    ```Shell
    CLASS zcl_generate_bookings_xxx DEFINITION
    ```

  2. Save and active your class.

      ![Replace source code](saveandactivate.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 8: ](Run ABAP application)]
  1. Run your class as an ABAP application (console) or press **F9**.

      ![Run ABAP application](application.png)

  2. Check console output.

      ![Check console output](output.png)

  3. Switch back to your data definition and press **F8** to see the inserted data.

      ![Check inserted data](data.png)

  4. Now check your result.

      ![Check inserted data](result.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 9: ](Test yourself)]
Define a table (without metadata) with following information in the correct order:

 - Name: `ztestyourself`
 - Key-Element: `key client`: `abap.clnt not null`
 - Elements:
    - `customername`: `abap.char(50)`
    - `country`: `abap.char(50)`
    - `emailaddress`: `abap.char(50)`

[DONE]
[ACCORDION-END]
