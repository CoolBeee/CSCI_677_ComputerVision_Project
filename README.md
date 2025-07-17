# Extrapolating Bounding Boxes from Occluded Objects
- Showcase of the work I did for my CSCI677 - Computer Vision course at USC

# Motivation
- Explore how to build a detection system that remains reliable in situtations in which objects become slightly or fully occluded. Specifically in critical applications like self-driving cars. For example, if a pedestrian walks behind a parked car, the system still needs to reason about their continued presence and future location, even if they're not directly visible; in the case they suddenly reappear. 

# Methods
YoloV11
- YOLOv11 offers enhanced accuracy, faster inference speeds, and broader applicability across various computer vision tasks, making it a highly efficient and versatile choice for object detection.
- That is why it is used for the system's initial object detection and bounding box generation.

KalmanFilter
- Used to estimate a state, comprised of a position and velocity, using predictions and measurements.
- Based on this, predict and draw where the subsequent bounding box velocity and path.

<image width="25%" src ="https://github.com/user-attachments/assets/72dc0de1-bd01-4a18-89bf-52645d798a7e"></image>

Intersection over Union (IoU)
- Used to link object detections when the objects reappear after occlusion by assigning the best available matches based on the Intersection over Union.
- This algorithm allows us to see the spatial overlap between two bounding boxes over a adjustable threshold, the predicted bounding box and current detection bounding box area.

<image width="50%" src="https://github.com/user-attachments/assets/56b51c52-1d0e-4719-9a7d-90c8a3adee34"> </image>

# Example of the system in action
<video src="https://github.com/user-attachments/assets/bb4137ec-0927-4cac-9027-4585c108ea7e"> </video>




