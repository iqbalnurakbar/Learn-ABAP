The customer requests a program to display delivery document details. The user will input parameters for query restrictions:
- Delivery Document: `LIKP-VBELN`
- Shipping Point: `LIKP-VSTEL`
- Material Number: `LIPS-MATNR`

The final table should show:
- Delivery Document Number: `LIPS-VBELN`
- Item Number: `LIPS-POSNR`
- Shipping Point: `LIKP-VSTEL`
- Customer Number: `LIKP-KUNNR`
- Customer Name: `KNA1-NAME1`
- Material Number: `LIPS-MATNR`
- Material Description: `MAKT-MAKTX`
- Delivery Quantity: `LIPS-LFIMG`
- Delivery Unit: `LIPS-VRKME`
- Net Weight: `LIPS-BRGEW`
- Gross Weight: `LIPS-NTGEW`

**Objectives:**
1. Create a selection screen with the following requirements:
  - Shipping Point are required.
  - Delivery Document as a range with default "80000017".
  - Material Number as a range.
  - Add text-elements for input fields.
2. Set Input variant for your selection screen.
3. Check the existence of the delivery document in `LIKP`. Provide an error message if not found.
4. Check Delivery document input field cannot be empty using the **AT SELECTION SCREEN** event.
5. Get data from `LIKP` and `LIPS` tables based on user input.
6. Populate the remaining fields `KNA1-NAME1` based on customer data found on the previous step and `MAKT-MAKTX` based on material data found on the previous step and for `MAKTX` get the material description which language is = system language
7. **DISPLAY** your final ITAB result

**Specification**
1. Follow the naming convention for defining variables
2. Use text elements if possible instead of hard code text for description
3. Use constants if possible instead of hard code text for values
4. Give comments to your code explaining the core logic
5. Select the required fields only, do not use select *