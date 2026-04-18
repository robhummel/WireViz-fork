# BOM Logic

> 33 nodes · cohesion 0.16

## Key Concepts

- **Cable** (24 connections) — `src/wireviz/DataClasses.py`
- **Connector** (24 connections) — `src/wireviz/DataClasses.py`
- **AdditionalComponent** (16 connections) — `src/wireviz/DataClasses.py`
- **wv_bom.py** (13 connections) — `src/wireviz/wv_bom.py`
- **generate_bom()** (9 connections) — `src/wireviz/wv_bom.py`
- **get_additional_component_table()** (9 connections) — `src/wireviz/wv_bom.py`
- **bom_entry_key()** (6 connections) — `src/wireviz/wv_bom.py`
- **component_table_entry()** (6 connections) — `src/wireviz/wv_bom.py`
- **get_additional_component_bom()** (5 connections) — `src/wireviz/wv_bom.py`
- **make_str()** (5 connections) — `src/wireviz/wv_bom.py`
- **optional_fields()** (5 connections) — `src/wireviz/wv_bom.py`
- **# TODO: If category can have other non-empty values than 'bundle', maybe it shou** (5 connections) — `src/wireviz/wv_bom.py`
- **Return id of BOM entry or raise exception if not found.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return list of BOM rows as lists of column strings with headings in top row.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return a diagram node table row string with an additional component.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return part field values for the optional BOM columns as a dict.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return the company name and/or the part number in one single string or None othe** (5 connections) — `src/wireviz/wv_bom.py`
- **Return the value indexed if it is a list, or simply the value otherwise.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return value if a list, empty list if None, or single element list otherwise.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return comma separated elements if a list, empty string if None, or value as a s** (5 connections) — `src/wireviz/wv_bom.py`
- **Return a list of diagram node table row strings with additional components.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return a list of BOM entries with additional components.** (5 connections) — `src/wireviz/wv_bom.py`
- **Return a tuple of string values from the dict that must be equal to join BOM ent** (5 connections) — `src/wireviz/wv_bom.py`
- **Return a list of BOM entries generated from the harness.** (5 connections) — `src/wireviz/wv_bom.py`
- **bom_list()** (4 connections) — `src/wireviz/wv_bom.py`
- *... and 8 more nodes in this community*

## Relationships

- No strong cross-community connections detected

## Source Files

- `src/wireviz/DataClasses.py`
- `src/wireviz/wv_bom.py`
- `src/wireviz/wv_helper.py`

## Audit Trail

- EXTRACTED: 95 (44%)
- INFERRED: 121 (56%)
- AMBIGUOUS: 0 (0%)

---

*Part of the graphify knowledge wiki. See [[index]] to navigate.*