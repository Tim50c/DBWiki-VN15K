# DBWiki-VN15K: Vietnamese Multimodal Knowledge Graphs for Entity Alignment

## Dataset Overview

The dataset contains exactly 15,000 aligned entity pairs across both graphs, enriched with:
- **Relational Triples:** Graph structural data.
- **Numerical Attributes:** Measurable local characteristics.
- **Images:** Visual modalities providing cross-modal alignment signals.

## Graph Statistics
| Feature | Wikidata (KG1) | DBpedia (KG2) |
| --- | --- | --- |
| **Entities** | 14,999 | 12,064 |
| **Relationships** | 410 | 350 |
| **Relational Triples** | 203,192 | 150,233 |
| **Numeric Literals** | 26,206 | 165,685 |
| **Images** | 14,999 | 12,064 |
| **Aligned Entities (sameAs)**| \- | 12,064 |

*(Note: Ground-truth cross-KG alignment links define the equivalent entity pairs).*

## Data Files
- **`rel_triples_1`**: Relational triples for Wikidata (KG1). Each line contains a triple in the format: `head_entity \t relation \t tail_entity`.
- **`rel_triples_2`**: Relational triples for DBpedia (KG2). Each line contains a triple in the format: `head_entity \t relation \t tail_entity`.
- **`attr_triples_1`**: Numerical attributes for Wikidata (KG1). Each line contains an attribute in the format: `entity \t attribute \t "value"^^<type>`.
- **`attr_triples_2`**: Numerical attributes for DBpedia (KG2). Each line contains an attribute in the format: `entity \t attribute \t "value"^^<type>`.
- **`entity_images_1.txt`**: Image mappings for Wikidata (KG1). Each line contains an image mapping in the format: `Entity \t Image_ID \t Image_URL`.
- **`entity_images_2.txt`**: Image mappings for DBpedia (KG2). Each line contains an image mapping in the format: `Entity \t Image_ID \t Image_URL`.
- **`ent_links`**: The ground-truth cross-KG entity alignment links. Each line contains an alignment link in the format: `Wikidata_Entity \t DBpedia_Entity` (e.g., `Q100 \t <http://vi.dbpedia.org/resource/Boston>`).
