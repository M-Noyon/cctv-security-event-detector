# CCTV Person Tracking and Restricted-Zone Intrusion Detector

A Google Colab video-analytics prototype using a custom YOLOv8 person
detector, ByteTrack tracking, OpenCV polygon rules, and FFmpeg.

## Features

- Custom-trained person detector
- Person tracking across video frames
- User-defined restricted-zone polygon
- Two-second continuous-presence intrusion confirmation
- Timestamped JSON alerts
- Annotated video
- Incident clips with overlapping intervals merged

## Run

1. Open notebooks/CCTV_Event_Detector.ipynb in Google Colab.
2. Install dependencies and FFmpeg.
3. Restore the trained person model.
4. Upload an authorized test video.
5. Configure the restricted zone.
6. Run tracking, alert generation, and highlight export.

## Dataset and model

Before publishing, add:
- Original dataset URL, author, version, and license
- Training configuration
- Trained checkpoint download link
- Authorized demonstration-video link

## Results

See sample_outputs/evaluation_metrics.json.

Person-detector validation results measure bounding-box detection.
Intrusion-event precision and recall require separately labelled events
and have not been evaluated unless explicitly reported.

## Limitations

- Track IDs can change during occlusion.
- Missed detections reset the intrusion timer.
- The polygon assumes a stationary camera.
- Timestamp calculation assumes constant-frame-rate video.
- Detector confidence is not incident probability.
- Fall detection is not implemented in this version.
- This educational prototype is not a safety-critical alarm system.

## Privacy and licensing

Use only footage you have permission to process and share.
Do not publish API keys, private CCTV footage, or identifying data.
Check dataset and dependency licensing before redistribution.
