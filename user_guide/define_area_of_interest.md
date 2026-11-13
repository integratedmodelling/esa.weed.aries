# *WEED champion user guide:*
## _How to define and share an area of interest?_

**Audience:** WEED application users  
**Purpose:** Provide the geographic boundary to observe in WEED.  
**Preferred deliverables:** (1) WKT text with its coordinate reference system (CRS), or (2) a ZIP archive containing a vector file (shapefile format).  

You do **not** need to write k.LAB observation code. The WEED technical team will use your boundary to configure the observation.

## _Which areas of interest are currently used?_
You can check which are are used directly in the WEED application or in [this QGIS project](https://drive.google.com/drive/folders/1VxrGTC7qqHhDvlrBR15VjfIJNWapf4qt?usp=sharing), also shared in the Rocket chat channel dedicated to the champion users [WEED-CU](https://chat.integratedmodelling.org/group/dPGBCCXJu8rZ9AFE5).

#### ESA_WEED_New_Contexts_for_map_validation
This project contains the areas of interest and the global refernce data available for each country
<img width="960" height="564" alt="image" src="https://github.com/user-attachments/assets/b4726402-1367-44e8-b640-840d9b87803c" />



## 1. Choose the easiest method

| Your situation | Recommended method | What to send |
|---|---|---|
| You can access **k.Explorer** and want to select an area on the map | **Method A — Draw in k.Explorer** | Copy the context WKT and send it as text or a `.txt` file |
| You already have a GIS boundary in a shapefile | **Method B — Existing shapefile** | A `.zip` containing the complete shapefile |
| You have GeoJSON, KML or GeoPackage data | **Method C — Convert in QGIS** | A shapefile ZIP or WKT |
| You want to draw a boundary but cannot use k.Explorer | **Method D — Draw in an external map editor** | Export GeoJSON, then convert it to shapefile or WKT |

**Tip:** Use a polygon for an irregular area. A circle is convenient for a quick approximation, but it may include locations outside your intended site. If you need exact administrative or ecological boundaries, use an authoritative polygon dataset where possible.

## 2. Method A — Draw a context directly in k.Explorer

This method uses the drawing and context-history tools in **k.Explorer**. The images below show the interface used for this guide; controls may look slightly different in other versions.

### Step 1 — Open the context drawing tools

1. Navigate the map to your area of interest.
2. Expand the context controls from the knowledge bar by clicking the **`>`** arrow.
3. In the **Context** menu, select **Draw context**.

![Image 1: Context menu with Draw context option](https://github.com/user-attachments/assets/11230c30-aaf3-48b5-b192-1c1b0042d87c)

### Step 2 — Draw a polygon or a circle

- **Polygon:** Select the polygon drawing tool, then click on the map to place the vertices that outline your area. Complete the shape using the tool's finishing interaction.
- **Circle:** Select the circle tool, click to position its centre and adjust the radius to cover your area.
- Adjust the shape if necessary before accepting it.

**Polygon example:**

![Image 2: Drawing a polygon](https://github.com/user-attachments/assets/622e8ab1-9fe8-45be-ae3e-a58954f1884e)

**Circle example:**

![Image 3: Drawing a circle](https://github.com/user-attachments/assets/a601d4de-888f-4599-884a-7220a0f8d618)

### Step 3 — Confirm the context

Click the **green check mark** in the drawing toolbar to use the selected shape as the current geographic context. The screenshot shows the drawn area before confirmation.

![Image 4: Green check mark confirms the selected shape](https://github.com/user-attachments/assets/d0a09d91-29a9-4a9e-9874-445b3ddde5cd)

### Step 4 — Make an observation in the selected area

1. Use the knowledge bar to search for an observable, for example **Elevation** by typing in ``elevation``.
2. Once the observation is complete, the context is stored until the end of the session

![Image 5: Searching for Elevation](https://github.com/user-attachments/assets/ff7f409f-3cd5-4a9d-889e-33f81ae16963)

![Image 6: Observation panel for the selected context](https://github.com/user-attachments/assets/0d65b392-ad81-4e1e-8e6f-4ff697d0a77d)

![Image 7: Elevation observation and value on the map](https://github.com/user-attachments/assets/bd66185b-dc46-47a1-a225-21c52b42de4c)


If you want to query a the public results for Ecosystem Typology as modelled in the ARIES for SEEA:

- type in _**ecos**_

![Image 8](https://github.com/user-attachments/assets/48cde5c4-3542-4e28-9fca-0b470cd9bdf1) 

- select the  quality _**EcosystemType**_ (light green font)
![Image 9](https://github.com/user-attachments/assets/a21af1e9-caa6-41f0-a0ca-629f65430964)

**Note:** The observations in these screenshots are only an example. The purpose of this guide is to define and share the **area boundary**, not to prescribe which observable to select.

### Step 5 — Reuse or copy the saved context

After drawing and using the area, open the context menu again and select **Previous contexts**. The interface displays contexts used during the current session.

1. Locate the relevant previous context.
2. Use it again if you want to make another observation in the same area.
3. Click the **copy** icon beside the context to copy its boundary to the clipboard.
4. Paste the copied text into a plain-text file, email or message and send it to the WEED team.

![Image 10: Previous contexts and the copy context shape control](https://github.com/user-attachments/assets/6fa59823-8570-4a7c-9ced-997840ec5ba4)

![Image 11: Confirmation that the context was copied to the clipboard](https://github.com/user-attachments/assets/471fb8ae-d72b-4a18-b270-c2febe4091fe)

![Image 12: Example copied boundary text](https://github.com/user-attachments/assets/c73ba43f-44a6-4325-a435-b7c3bc789a52)

The copied text looks similar to this (illustrative coordinates only):

```text
EPSG:4326 POLYGON ((14.8434 11.1926, 14.8495 11.1925, 14.8496 11.1898, 14.8435 11.1900, 14.8434 11.1926))
```

**Important:** Contexts in **Previous contexts** are available for reuse during the session, but should not be treated as permanent storage. **Copy and save the WKT before ending the session** if you want the WEED team to reproduce the same area later. The coordinates in the example are longitude followed by latitude.

## 3. Method B — Provide an existing shapefile

If you already have the geographic boundary as an ESRI shapefile, there is no need to redraw it.

1. Check that the dataset contains a **polygon or multipolygon**, not only points or lines.
2. Check that the polygon covers the intended site and is not accidentally a large bounding rectangle.
3. If possible, export it using **EPSG:4326 (WGS 84)**. If you retain a different CRS, make sure its definition is included.
4. Put the files with the **same base name** into one ZIP archive. At minimum, include:
   - `site_boundary.shp` — geometry
   - `site_boundary.shx` — shape index
   - `site_boundary.dbf` — attribute table
   - `site_boundary.prj` — coordinate reference system
   - `site_boundary.cpg` — character encoding, if available
5. Name the ZIP clearly, e.g. `CMR_Zina_boundary.zip`, and share it with the WEED team.

Do not send the `.shp` file by itself: it depends on its companion files.

## 4. Method C — Convert GeoJSON, KML or GeoPackage in QGIS

[QGIS](https://qgis.org/) is a free desktop GIS application. It can open many common geographic file formats and export the area to a shapefile or WKT.

### Convert a GeoJSON (or KML/GeoPackage) to a shapefile

1. Open QGIS.
2. Add your boundary using **Layer → Add Layer → Add Vector Layer** (or drag the file onto the map).
3. Confirm that the correct boundary is visible and that it is a polygon layer.
4. Right-click the layer → **Export → Save Features As…**.
5. Choose **ESRI Shapefile** as the format.
6. Select **EPSG:4326 — WGS 84** as the output CRS, unless the WEED team has requested a different one.
7. Choose a file name and save.
8. ZIP the resulting `.shp`, `.shx`, `.dbf`, `.prj` and any `.cpg` files together.

### Convert a polygon to WKT in QGIS

1. Load the polygon in QGIS and **export/reproject it to EPSG:4326** if necessary.
2. Open the layer's attribute table and use the **Field Calculator** to create a text field, or use an expression-based export workflow.
3. Use the expression:

   ```text
   geom_to_wkt($geometry)
   ```

4. Copy the WKT value for the desired feature. It should start with `POLYGON` or `MULTIPOLYGON`.
5. State **CRS: EPSG:4326** alongside the WKT. You can also place `EPSG:4326 ` immediately before the WKT in a text file to match the format copied by k.Explorer.

If the dataset contains **several separate features** that together define one area, tell the WEED team whether all of them should be included. Do not silently select only the first feature.

## 5. Method D — Draw outside k.Explorer

If k.Explorer is unavailable, you can draw a polygon using a browser-based map editor such as [geojson.io](https://geojson.io/).

1. Open the editor and navigate to the intended location.
2. Choose the polygon tool and draw the boundary.
3. Check the shape on the map and save/export it as **GeoJSON**.
4. Follow **Method C** to convert that GeoJSON to a shapefile or WKT.

A GeoJSON file is a useful **intermediate format**, but for the WEED submission described in this guide, please provide **WKT or a zipped shapefile**.

## 6. What makes a good boundary?

Before sending the boundary, verify the following:

- **Correct location:** The area appears in the expected country and region.
- **Correct extent:** The boundary covers the actual intended area, not an accidental map viewport or oversized rectangle.
- **Suitable geometry:** The geometry is a polygon/multipolygon; a circle drawn in a map interface is represented as an approximating polygon when exported to WKT.
- **Correct CRS:** Prefer **EPSG:4326**. For WKT, clearly state the CRS and use **longitude, latitude** coordinate order.
- **Valid geometry:** Polygon rings are closed and boundaries do not cross themselves. If QGIS reports invalid geometries, ask the WEED team for help or use QGIS's geometry-validation tools.
- **Appropriate detail:** Include enough vertices to represent the intended area, but avoid unnecessary complexity. For very detailed areas, a shapefile is usually easier to share than a very long WKT string.
- **Source and confidence:** Mention whether the boundary is official, digitized manually, or approximate.

## 7. What to send to the WEED team

Please include the following information with your file or copied WKT:

| Field | Example |
|---|---|
| **Area name** | Zina study area |
| **Country / region** | Cameroon — Extrême-Nord |
| **Champion user / contact** | Name and email |
| **Boundary format** | WKT copied from k.Explorer / zipped shapefile |
| **Coordinate reference system** | EPSG:4326 |
| **Boundary source** | Drawn in k.Explorer / official GIS layer |
| **Accuracy / limitations** | Approximate extent; to be reviewed locally |
| **Purpose / requested observation** | Ecosystem mapping and validation |
| **Relevant year or period (if known)** | 2024 |

### Suggested submission message

> **Subject:** WEED area of interest — [country] — [area name]  
> **Area name:** ...  
> **Country / region:** ...  
> **Boundary source:** ...  
> **CRS:** EPSG:4326  
> **Boundary:** [paste WKT or attach zipped shapefile]  
> **Notes:** ...

## 8. Frequently asked questions

**Do I need to know GIS software?**  
No. If you have access to k.Explorer, drawing a context and copying its WKT is usually the simplest option.

**Can I send a screenshot instead of a boundary file?**  
A screenshot is helpful for explaining the location, but it does not provide the exact geometry needed for integration. Please also send WKT or a zipped shapefile.

**Can I draw a circle?**  
Yes, in k.Explorer. Be aware that a circle may be an approximation of the actual study-area boundary.

**Will my drawn area remain available forever in k.Explorer?**  
No. The illustrated workflow provides access to previous contexts **within the session**. Save the copied WKT for future use.

**Should I specify the observation's grid size or write k.LAB code?**  
No. The WEED technical team will configure observation parameters, including spatial resolution and time, separately from the boundary you provide.

**What if my dataset is in another CRS?**  
Either reproject it to EPSG:4326 using QGIS, or share the original shapefile with its `.prj` and clearly state the CRS. Ask the WEED team if you are unsure.

---

**Key takeaway:** The easiest route is **k.Explorer → Draw context → Green check → Observe → Previous contexts → Copy boundary → Send WKT**. If you already have an authoritative GIS boundary, send a **complete zipped shapefile** instead.
