The customer wants a program that displays goods receipt details. The user will input parameters for query restrictions:

- Material Document Number: `MKPF-MBLNR`
- Document Year: `MKPF-MJAHR`
- Plant: `MSEG-WERKS`
- Material Number: `MSEG-MATNR`

The final table should show:

- Material Document Number: `MSEG-MBLNR`
- Document Year: `MSEG-MJAHR`
- Item Number: `MSEG-ZEILE`
- Posting Date: `MKPF-BUDAT`
- Plant: `MSEG-WERKS`
- Storage Location: `MSEG-LGORT`
- Movement Type: `MSEG-BWART`
- Material Number: `MSEG-MATNR`
- Material Description: `MAKT-MAKTX`
- Quantity in Unit of Entry: `MSEG-MENGE`
- Base Unit of Measure: `MARA-MEINS`

**Create a selection screen** with the following requirements:
1. Material Document Number as a range and set default value as '4900000012'.
2. Document Year is required.
3. Plant is required.
4. Material Number as a range.
5. Add text-elements for each input field.

**Check the existence of the material document in `MKPF`.** Display an error message if not found.

Check Material document input field cannot be empty using the **AT SELECTION SCREEN** event.

**Retrieve data from `MKPF` and `MSEG` tables** based on user input in the selection screen.

**Populate fields `MAKT-MAKTX` for the material description and `MARA-MEINS` for the base unit of measure,** ensuring the retrieved `MAKTX` data language is based on the system language
