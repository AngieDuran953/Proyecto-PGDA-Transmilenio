# Transmilenio Theft Prediction Model

This project aims to develop a model capable of predicting theft incidents in Transmilenio stations and buses to enhance security within the system. The project consists of two stages: object and behavior detection, and theft probability calculation based on variables such as day, time, station congestion, sector, and neighborhood.

## Object and Behavior Detection

Videos from Transmilenio's security cameras were collected from YouTube. The videos were trimmed and classified as normal or containing theft incidents. However, there was an imbalance in the classes, with a majority of theft videos and fewer normal day videos.

Three algorithms were tested for video analysis:
1. YOLO (You Only Look Once) v4: A pre-trained model that detects people in each frame but struggles with overlapping individuals and low-quality videos.
2. Motion filter: Used OpenCV to isolate moving entities, but faced difficulties with multiple people and their overlap.

Additionally, Teachable Machine was employed to identify objects and behaviors in Transmilenio stations. The results showed that Teachable Machine performed better than YOLO.

## Theft Prediction Model

The extracted variables from the videos, along with a structured database of theft incidents, were combined into a dataframe. Six classification models (Decision Tree, Random Forest, Support Vector Regression, Gradient Boosting, Neural Network Regression, and Linear Regression) were trained and evaluated using the Test RMSE metric. The Gradient Boosting model achieved the best performance in predicting theft incidents.

## Contributing

Contributions to the project are welcome. If you wish to contribute, please follow these guidelines:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Make your changes and commit them: `git commit -m "Add new feature"`.
4. Push to the branch: `git push origin feature/new-feature`.
5. Submit a pull request.

For reporting issues or requesting features, please use the issue tracker on the [GitHub repository](https://github.com/AngieDuran953/Proyecto-PGDA-Transmilenio).

## Contact

For any questions or feedback, please contact:

Name: Angie Duran
Email: angieduran953@gmail.com


Repository Link: [https://github.com/AngieDuran953/Proyecto-PGDA-Transmilenio](https://github.com/AngieDuran953/Proyecto-PGDA-Transmilenio)
