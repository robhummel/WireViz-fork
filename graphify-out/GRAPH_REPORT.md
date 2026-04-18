# Graph Report - .  (2026-04-17)

## Corpus Check
- Corpus is ~19,302 words - fits in a single context window. You may not need a graph.

## Summary
- 157 nodes · 356 edges · 13 communities detected
- Extraction: 52% EXTRACTED · 48% INFERRED · 0% AMBIGUOUS · INFERRED: 172 edges (avg confidence: 0.63)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_BOM Logic|BOM Logic]]
- [[_COMMUNITY_HTML & Helpers|HTML & Helpers]]
- [[_COMMUNITY_Harness State|Harness State]]
- [[_COMMUNITY_Graph & Colors|Graph & Colors]]
- [[_COMMUNITY_Harness Core|Harness Core]]
- [[_COMMUNITY_Example Builder|Example Builder]]
- [[_COMMUNITY_SVG Handling|SVG Handling]]
- [[_COMMUNITY_Hardware Syntax|Hardware Syntax]]
- [[_COMMUNITY_Project Config|Project Config]]
- [[_COMMUNITY_Metadata & Templates|Metadata & Templates]]
- [[_COMMUNITY_Setup|Setup]]
- [[_COMMUNITY_Connections|Connections]]
- [[_COMMUNITY_Templating|Templating]]

## God Nodes (most connected - your core abstractions)
1. `Harness` - 33 edges
2. `Connector` - 24 edges
3. `Cable` - 24 edges
4. `parse()` - 22 edges
5. `AdditionalComponent` - 16 edges
6. `Metadata` - 10 edges
7. `Options` - 10 edges
8. `generate_html_output()` - 9 edges
9. `get_additional_component_table()` - 9 edges
10. `generate_bom()` - 9 edges

## Surprising Connections (you probably didn't know these)
- `parse()` --calls--> `expand()`  [INFERRED]
  src/wireviz/wireviz.py → src/wireviz/wv_helper.py
- `parse()` --calls--> `get_single_key_and_value()`  [INFERRED]
  src/wireviz/wireviz.py → src/wireviz/wv_helper.py
- `WireViz` --references--> `PyYAML`  [INFERRED]
  docs/README.md → requirements.txt
- `Harness` --uses--> `Cable`  [INFERRED]
  src/wireviz/Harness.py → src/wireviz/DataClasses.py
- `Harness` --uses--> `Connector`  [INFERRED]
  src/wireviz/Harness.py → src/wireviz/DataClasses.py

## Hyperedges (group relationships)
- **Core YAML Input Sections** — syntax_connectors, syntax_cables, syntax_connections [EXTRACTED 1.00]
- **BOM Generation Flow** — syntax_connectors, syntax_cables, syntax_bom [INFERRED 0.95]

## Communities

### Community 0 - "BOM Logic"
Cohesion: 0.16
Nodes (29): AdditionalComponent, Cable, Connector, bom_entry_key(), bom_list(), component_table_entry(), generate_bom(), get_additional_component_bom() (+21 more)

### Community 1 - "HTML & Helpers"
Cohesion: 0.09
Nodes (22): Connection, _get_yaml_data_and_path(), Parses the provided FILE and generates the specified outputs., wireviz(), aspect_ratio(), awg_equiv(), expand(), file_read_text() (+14 more)

### Community 2 - "Harness State"
Cohesion: 0.22
Nodes (16): MateComponent, MatePin, Metadata, Options, # TODO: allow using pin labels in addition to pin numbers, just like when defini, # TODO: include properties of wire used to create the loop, Tweak, dict (+8 more)

### Community 3 - "Graph & Colors"
Cohesion: 0.18
Nodes (18): Image, graph(), get_color_hex(), get_color_translation(), Return list of hex colors from either a string of color names or :-separated hex, Return list of colors translations from either a string of color names or :-sepa, translate_color(), html_bgcolor() (+10 more)

### Community 4 - "Harness Core"
Cohesion: 0.18
Nodes (4): Harness, _get_output_dir(), _get_output_name(), parse()

### Community 5 - "Example Builder"
Cohesion: 0.24
Nodes (13): build_generated(), clean_generated(), collect_filenames(), compare_generated(), main(), parse_args(), restore_generated(), open_file_append() (+5 more)

### Community 6 - "SVG Handling"
Cohesion: 0.32
Nodes (6): svg(), data_URI_base64(), embed_svg_images(), embed_svg_images_file(), get_mime_subtype(), Return Base64-encoded data URI of input file.

### Community 7 - "Hardware Syntax"
Cohesion: 0.33
Nodes (6): Advanced Image Scaling, Bill of Materials (BOM), Wire Bundles, Cables, Connectors, Ferrules

### Community 8 - "Project Config"
Cohesion: 0.5
Nodes (4): build_examples.py, WireViz, Graphviz, PyYAML

### Community 9 - "Metadata & Templates"
Cohesion: 1.0
Nodes (2): Harness Metadata, HTML Template Placeholders

### Community 10 - "Setup"
Cohesion: 1.0
Nodes (0): 

### Community 11 - "Connections"
Cohesion: 1.0
Nodes (1): Connections

### Community 12 - "Templating"
Cohesion: 1.0
Nodes (1): YAML Anchors and Templates

## Knowledge Gaps
- **24 isolated node(s):** `# TODO: implement CSV output (preferrably using CSV library)`, `Return list of hex colors from either a string of color names or :-separated hex`, `Return list of colors translations from either a string of color names or :-sepa`, `Open utf-8 encoded text file for reading - remember closing it when finished`, `Open utf-8 encoded text file for writing - remember closing it when finished` (+19 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Metadata & Templates`** (2 nodes): `Harness Metadata`, `HTML Template Placeholders`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Setup`** (1 nodes): `setup.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Connections`** (1 nodes): `Connections`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Templating`** (1 nodes): `YAML Anchors and Templates`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Harness` connect `Harness Core` to `BOM Logic`, `Harness State`, `Graph & Colors`?**
  _High betweenness centrality (0.281) - this node is a cross-community bridge._
- **Why does `parse()` connect `Harness Core` to `HTML & Helpers`, `Harness State`, `Example Builder`?**
  _High betweenness centrality (0.244) - this node is a cross-community bridge._
- **Why does `build_generated()` connect `Example Builder` to `Harness Core`?**
  _High betweenness centrality (0.108) - this node is a cross-community bridge._
- **Are the 22 inferred relationships involving `Harness` (e.g. with `Cable` and `Connector`) actually correct?**
  _`Harness` has 22 INFERRED edges - model-reasoned connections that need verification._
- **Are the 20 inferred relationships involving `Connector` (e.g. with `Harness` and `Raise exception for any outdated attributes in args.`) actually correct?**
  _`Connector` has 20 INFERRED edges - model-reasoned connections that need verification._
- **Are the 20 inferred relationships involving `Cable` (e.g. with `Harness` and `Raise exception for any outdated attributes in args.`) actually correct?**
  _`Cable` has 20 INFERRED edges - model-reasoned connections that need verification._
- **Are the 17 inferred relationships involving `parse()` (e.g. with `wireviz()` and `Harness`) actually correct?**
  _`parse()` has 17 INFERRED edges - model-reasoned connections that need verification._