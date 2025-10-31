# HeistHalters Theft Prevention by ScreenScavers
THEFT PREVENTION using a Computer Vision Solution 

Team: Khalida Bestani, Malcolm Richardson, R. Brandon Thompson

This repository contains a project proposal to a real world solution. 

Tier 3 - We want the system to analyze the motion to determine if a theft is in progress. If a theft is determined, the authorities will be alerted by the system.

Problem Statement: 
  Museums lost over $5 billion last year to thefts and damages. Traditional security systems are too expensive and cannot monitor every exhibit at all times and respond fast enough to prevent loss or damage. There     is an urgent need for affordable real-time security that prevents loss and damage before it happens for institutions of all sizes.

Solution Overview: 
  THEFT PREVENTION using a Computer Vision Solution that spots when someone is getting too close to the exhibits or is acting suspicious. The model identifies threatening or sketchy behavior, filters out false     alarms while verifying actual threats to then alert security in real time.

  Object Detection (OD) and Action Recognition (AR) to detect people and identify their behavior. Just watching people is not enough. OD to detect people and products. AR to identify suspicious behavior, "theft"       and track the suspects throughout the building(s). Neuroevolution to evolve from new data and improve continuosly. Evolutionary Video Deep Learning learns patterns that evolves better architecture or                 strategies for learning those patterns.

  Deep spatiotemporal learning and continual learning through: Convolutional 3D Neural Networks, Recurrent Neural Networks and Video Tranformers

  UCF-Crime or Anomaly Detection datasets - has actual suspicious behavior videos COCO - has people, bags, products (good starting point) Roboflow - search for "shoplifting detection" or "retail security" datasets     Unity Perception - synthetic datasets that allow us to generate correct labels that would be difficult to get in actual museums.Can build "scenes" for bounding box and labeler to capture boundaries, person           crossing boundaries, hands, gestures, artifacts, reaching, bags, etc

Technical Approach (technique, model, framework)-Technique: Object Detection & Classification​

​  Model: YOLOv8 trained on behavioral, theft detection, and action recognition datasets from COCO, RoboFlow Universe, UCF-101​

  Framework: PyTorch handles 30+ fps real-time video analysis for threat events with no lag time between threat event and alert being sent out. Flexible to fine-tune for threat behaviors.​

​  Justification: Enables fast, real-time detection and classification, providing a reliable and practical solution for protecting valuable museum artifacts. Has access to proven real-world detection models ​

Dataset Plan (source, size, labels, link if public) - 

  Specialized behavioral datasets 📊 will be collected from COCO's Keypoint detection. 🔍Train, validation and test sets that have more than 200,000 available images.​

  Roboflow Universe's open-source shoplifting/gesture datasets 📊 will help our model learn typical movement patterns before we train it on real museum scenarios to provide a solid foundation. 🤖​

  Unity Perception open-source package provides synthetic data for computer vision by training the synthetic datasets on a 2D object detection model.  🤖​

  UFC-Crime Dataset for anomaly detection to identify and label abnormal and normal behavior. The system learns to detect anomalies by comparing patterns and context to what is "normal."​ 10,000-20,000 high-quality     labeled data images needed to train, validate and test model​

​  https://universe.roboflow.com/search?q=class%3Ashoplifting​

  cocodataset.org/#keypoints-2020​

  https://arvix.org.abs.2107.04259​

  https://www.crcv.ucf.edu/projects/real-world/

Metrics (primary + secondary)

  Primary Metric:  Our model prioritizes recall because failing to identify actual thefts costs 5-20x less than looking into false alarms. False negatives result in money lost with every undetected theft, legal       issues and possible regulatory penalties. False positives create friction among the staff, can cause alarm fatigue then real threats get ignored or missed. False alarms do not have the catastrophic outcomes such     as the loss of multi-million dollar or even priceless artifacts. This leads us to optimize for high recall first then fine tune the precision as we go.​

  Secondary Metrics: Precision target of 80-90% is achievable and realistic by training on high-quality labeled datasets of behavioral anomalies, general surveillance, and theft detection images. We also focus on       speed to maximize the efficiency from real-time detection with 50-500 4K cameras achieving 30 FPS continuous recording.​

Week-by-Week Plan:

  Week 10 - (Oct 30)	Get dataset, set up environment	Dataset ready

  Week 11 - (Nov 6)	Train or fine-tune model	Model working

  Week 12 - (Nov 13)	Test and improve	Good accuracy

  Week 13 - (Nov 20)	Create demo / video	Demo ready

  Week 14 - (Nov 27)	Final testing / documentation	Everything done

  Week 15 - (Dec 4)	Present project	Presentation day

Resources Needed (compute, cost, APIs)

  Google Colab T4 GPU for primary platform to conduct initial testing. Kaggle for backup or more time if needed.​

  UCF-Crime datasets for actual footage of criminalbehaviors with a "normal" baseline to compare against. UCF requires a request form at no cost. ​

  COCO datasets to provide a baseline for detecting people near museum exhibits. Human pose gestures dataset from MPI.​

  PyTorch framework with YOLOv8 for object detection to handle desired 30 fps​

Risks & Mitigation Table

  Risk - Low accuracy, Missing data 
  Probability - Medium
  Mitigation - Use data augmentation, High Switch to Roboflow dataset

Used Claude AI for insight on what models Veesion and other top companies are using for retail prevention with AI. Claude provided a breakdown of the models used, ML domains, architectures and examples of real world use cases outside of retail theft prevention.
Copilot was used to design powerpoint slides. ChatGPT was utilized to provide information on the best datasets and how/when to implement them into training, testing or fine-tuning stages.
