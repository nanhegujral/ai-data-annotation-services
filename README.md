# AI Data Annotation & Data Labeling — Formats & Reference

Maintained by [Precise BPO Solution](https://www.precisebposolution.com)

> Part of a documentation collection. Start at the
> [hub repository](https://github.com/nanhegujral/enterprise-data-labeling-and-data-entry)
> for an overview of all related resources, including online data entry and product
> data management. This repository focuses specifically on annotation types and
> output formats.

## Annotation types

**Computer vision**
Bounding box · polygon · polyline · semantic segmentation · instance segmentation ·
3D cuboid · keypoint/landmark · image classification · video object tracking

**NLP**
Named entity recognition (NER) · text classification · sentiment annotation · intent
classification · document annotation

**OCR & document AI**
OCR annotation, layout-aware document annotation

## Output format examples

Below are minimal, illustrative examples of the formats most commonly requested for
annotated training data. These are structural examples for reference, not sample data
from any client project.

### Bounding box — COCO JSON (excerpt)

```json
{
  "images": [{ "id": 1, "file_name": "img_001.jpg", "width": 1920, "height": 1080 }],
  "annotations": [
    {
      "id": 1,
      "image_id": 1,
      "category_id": 3,
      "bbox": [412, 158, 220, 340],
      "area": 74800,
      "iscrowd": 0
    }
  ],
  "categories": [{ "id": 3, "name": "vehicle" }]
}
```

### Bounding box — YOLO (`.txt`, one line per object)

```text
# class_id  x_center  y_center  width  height   (all normalized 0-1)
2 0.4931 0.4123 0.1146 0.3148
```

### Polygon segmentation — LabelMe JSON (excerpt)

```json
{
  "shapes": [
    {
      "label": "road_marking",
      "points": [[100, 200], [140, 210], [138, 260], [95, 250]],
      "shape_type": "polygon"
    }
  ],
  "imageWidth": 1920,
  "imageHeight": 1080
}
```

### NER — CoNLL-style tagging

```text
Precise   B-ORG
BPO       I-ORG
Solution  I-ORG
is        O
based     O
in        O
Pune      B-LOC
```

## Supported output formats

YOLO / YOLOv8 · COCO · Pascal VOC XML · CVAT XML · LabelMe JSON · VGG JSON · JSON ·
CSV · XML

## Industries

Manufacturing · healthcare · agriculture · retail · sports analytics · autonomous
driving · construction · satellite & geospatial · logistics · insurance

*(Full cross-collection industry table is in the
[hub repository](https://github.com/nanhegujral/enterprise-data-labeling-and-data-entry#industries-served).)*

## Capability profile

The complete Enterprise AI Data Annotation & Data Labeling Capability Profile PDF is
included in this repository:
[`PRECISE_BPO_Solution_AI_Data_Annotation_Capability_Profile.pdf`](./PRECISE_BPO_Solution_AI_Data_Annotation_Capability_Profile.pdf)

## Related resources

- [Documentation hub](https://github.com/nanhegujral/enterprise-data-labeling-and-data-entry)
- [Data entry & document processing](https://github.com/nanhegujral/precise-online-data-entry-services)
- [Data labeling services (official page)](https://www.precisebposolution.com/data-labeling-services.html)

## Contact

Email: info@precisebposolution.com
Website: [precisebposolution.com](https://www.precisebposolution.com)
