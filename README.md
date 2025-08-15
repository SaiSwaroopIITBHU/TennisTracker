# TennisTracker

A complete **YOLOv8-based tennis player tracking and movement analysis** pipeline — fixed to work with **PyTorch 2.7** despite the `weights_only` loading issue.  
This script detects players in a tennis match video, tracks them across frames, calculates distances traveled, and generates a **comprehensive visual analysis** with charts, tables, and court movement paths.

---

## 📌 Features

- **Fixed PyTorch 2.7 Compatibility**  
  - Handles `weights_only` loading issues with YOLOv8.
  - Safe globals patching for YOLO model classes.

- **Accurate Player Detection**
  - YOLOv8 person detection (fine-tuned filtering for tennis scenarios).
  - Bounding box area and aspect ratio filtering to avoid false positives.

- **Robust Player Tracking**
  - **CentroidTracker** with distance-based matching.
  - Handles player disappearance and re-entry.
  - Maintains unique IDs across the match.

- **Distance & Path Analysis**
  - Pixel-to-meter conversion based on court dimensions.
  - Per-player movement trails.
  - Total, average, and distribution metrics.

- **Comprehensive Analysis Output**
  - Distance bar charts (pixels & meters).
  - Pie chart of movement distribution.
  - Player movement paths overlay.
  - Detailed statistics table.
  - Summary box highlighting most active player.

- **Video Output**
  - Saves a processed MP4 video with:
    - Bounding boxes.
    - Distance overlays.
    - Player trails.
    - Frame count & tracking stats.

