Project Structure:

- football_ai.ipynb → Full pipeline
- models/ → Trained detection models
- assets/ → Output images and demo videos
- requirements.txt → Dependencies

Football Tactical Analysis using Computer Vision
⚙️ Complete Pipeline

Step 1 — Dataset Preparation

Roboflow dataset

4 classes (ball, goalkeeper, player, referee)

298 training images

Image size: 1280

Batch size: 6

Epochs: 50

Step 2 — Player Detection

Model: YOLOv8

mAP@0.5: 0.861

GPU: Tesla T4

Step 3 — Multi-Object Tracking

Tracker: ByteTrack

Assign unique IDs per player

Step 4 — Team Classification

Extract player crops

Use SigLIP embeddings

Cluster into 2 teams

Assign goalkeepers by centroid distance

Step 5 — Field Keypoint Detection

Pretrained Roboflow field detection model

Detect pitch vertices

Step 6 — Homography Transformation

Compute transformation matrix

Convert broadcast coordinates → pitch coordinates

Step 7 — Tactical Visualization

Radar view (FIFA style)

Voronoi diagram (control dominance)

Smooth blended Voronoi map
