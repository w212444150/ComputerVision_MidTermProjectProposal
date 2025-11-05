# ComputerVision_MidTermProjectProposal
THEFT PREVENTION using a Computer Vision Solution 

Team: Khalida Bestani, Malcolm Richardson, R. Brandon Thompson

This repository contains a project proposal to a real world solution. 

Tier 3 + justification

Problem Statement (2–3 sentences) Museums lost over $5 billion last year to thefts and damages. Traditional security systems are too expensive and cannot monitor every exhibit at all times and respond fast enough to prevent loss or damage. There is an urgent need for affordable real-time security that prevents loss and damage before it happens for institutions of all sizes.

Solution Overview: THEFT PREVENTION using a Computer Vision Solution that spots when someone is getting too close to the exhibits or is acting suspicious. The model identifies threatening or sketchy behavior, filters out false alarms while verifying actual threats to then alert security in real time.

Team: Khalida Bestani, Malcolm Richardson, R. Brandon Thompson

This repository contains a project proposal to a real world solution.

Analyze, detect and alert. Veesion uses Video Deep Learning

Object Detection (OD) and Action Recognition (AR) to detect people and identify their behavior. Just watching people is not enough. OD to detect people and products. AR to identify suspicious behavior, "theft" and track the suspects throughout the building(s). Neuroevolution to evolve from new data and improve continuosly. Evolutionary Video Deep Learning learns patterns that evolves better architecture or strategies for learning those patterns.

Deep spatiotemporal learning and continual learning through: Convolutional 3D Neural Networks, Recurrent Neural Networks and Video Tranformers


Technical Approach (technique, model, framework) Import the following libraries and framework: Ultralytics for YOLOv8 that looks and identifies people, actions, exhibits and other objects in images is ultimately the brain for our AI system; Opencv-python-headless to read video files and break them into individual frames; PyTorch framework (torch and torchvision) to build and train the neural networks performing math calculations learning from examples during training and run predictions on new videos, inference; Transformers to connect images to text descritpion and generate explanations, utilizing CLIP and BLIP, to reduce false alarms by understanding the intent and not just actions; Scikit-learn to calculate accuracy, precision, recall and F1-scores through splitting our data into training, validation and testing groups creating confusion matrices showing which behaviors our AI confuses; Matplotlib and Seaborn show results with visual charts and graphs helping track training curves and prove the system is working; Pytorchvideo for analyzing frame sequences and understand behavior over time. Our system balances a lot of competing demands simultaneously including tediously composing datasets, continuous active learning that improves detection and minimizes human labeling, real-time image processing at 20-30 fps, and high recall in order to be successful.  

Dataset Plan (source, size, labels, link if public) A strong foundation is built for our behavioral theft detection system using multiple sources to avoid bias by combining large-scale datasets for training and specialized behaviorial  data for rare theft events used for fine-tuning.  UCF-101 has > 13,000 videos that cover 101 action categories that has demonstrated 96% accuracy with YOLO architectures which brings us to believe is ideal for the intial transfer learning. UCF-Crime or Anomaly Detection datasets - has actual suspicious behavior videos. COCO - has people, bags, products (good starting point) Roboflow - for "shoplifting detection" or "retail security" datasets. Unity Perception - synthetic datasets that allow us to generate correct labels that would be difficult to get in actual museums. Can build "scenes" for bounding box and labeler to capture boundaries, person crossing boundaries, hands, gestures, artifacts, reaching, bags, etc

Metrics (primary + secondary)

Week-by-Week Plan

Resources Needed (compute, cost, APIs) Changed runtime to L4 GPU to handle required video sequencing needed for this project that performs great with YOLOv8 for training. The project calls for no less than 30 frames per second (fps) and batch sizes can range between 16-32 for faster training which L4 GPU excels in and makes perfect for this project.

Risks & Mitigation Table

Risk Probability Mitigation Low accuracy Medium Use data augmentation Missing data High Switch to Roboflow dataset

Used Claude AI for insight on what models Veesion and other top companies are using for retail prevention with AI. Claude provided a breakdown of the models used, ML domains, architectures and examples of real world use cases outside of retail theft prevention.
Copilot was used to design powerpoint slides. ChatGPT was utilized to provide information on the best datasets and how/when to implement them into training, testing or fine-tuning stages.
Gemini AI coding assistant used to fix and explain the imported code used for YOLOv8, RoboFlow...
