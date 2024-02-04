# Individual Project 2
# Classification with Deep Learning
#### Due Date
* Updated to Tuesday Mar 5, 2024 (23:59), 


#### Total Points
* 100 (One Hundred)

## Goal
In this project, you will be asked to finish a sequence classification task using deep learning. A trajectory data set with five taxi drivers' daily driving trajectories in 6 months will be provided. The primary objective is to predict which driver each 100-step sub-trajectory, extracted from the daily trajectories, belongs to. To evaluate your model, it will be tested on a separate set of data for five additional days, using the same preprocessing steps to ensure consistent data handling. This approach ensures consistency in data preparation across training and testing phases, allowing the model to accurately attribute each sub-trajectory to the correct driver. 

## Guidelines
* Implement required functions in model.py, train.py, and test.py.
* The file extract_feature.py provides a way to preprocess the data before feeding the data to the neural network, you can customize it to get more features but maintain 100 steps as standard for fair comparison.
* This project should be completed in Python 3. Pytorch is highly recommended, but you can decide to use other tools like MxNet.

## How to run :
training model:
* `$ python main.py train`

testing model:
* `$ python main.py test`

## Current Leaderboard
| rank | Name | Accuracy |
|---|---|---|
|**1**   | ... | 90% |
|**2**   | ... | 86% |
|**3**   | ... | 80% |


## Deliverables & Grading
* PDF Report (50%) [template](https://www.acm.org/binaries/content/assets/publications/taps/acm_submission_template.docx)
    * proposal
    * methodology
    * empirical results and evaluation
    * conclusion
    
* Python Code (50%)
    * Code is required to avoid plagiarism.
    * Implement functions in model.py, train.py, and test.py.
    * The submission should contain a folder including “extract_feature.py, model.py, train.py, test.py, main.py" and your latest trained model. 
    * Evaluation criteria.
      | Percentage | Accuracy |
      |---|---|
      | 100 | 0.8 |
      | 90 | 0.75 |
      | 80 | 0.70 |
      | 70 | 0.65|
      | 60 | 0.60 |
* Grading:
  * Total (100):
    * Code (50) + Report (50)

  * Code (50):
    * accuracy >= 0.80: 50
    * accuracy >= 0.75: 45
    * accuracy >= 0.70: 40
    * accuracy >= 0.65: 35
    * accuracy >= 0.60: 30

  * Report (50):
    1. Introduction & Proposal (5)
    2. Methodology (20):
        a. Data processing (5)
        b. Feature generation (5)
        c. Network structure (5)
        d. Training & validation process (5)
    3. Evaluation & Results (20):
        a. Training & validation results (10)
        b. Performance comparing to your baselines (maybe different network structure) (5)
        c. Hyperparameter (learning rate, dropout, activation) (5)
    4. Conclusion (5)

  * Bonus (5):
   
     5 bonus points for the top 3 on the leader board.

## Project Guidelines

#### Dataset Description
| plate | longitute | latitude | time | status |
|---|---|---|---|---|
|4    |114.10437    |22.573433    |2016-07-02 0:08:45    |1|
|1    |114.179665    |22.558701    |2016-07-02 0:08:52    |1|
|0    |114.120682    |22.543751    |2016-07-02 0:08:51    |0|
|3    |113.93055    |22.545834    |2016-07-02 0:08:55    |0|
|4    |114.102051    |22.571966    |2016-07-02 0:09:01    |1|
|0    |114.12072    |22.543716    |2016-07-02 0:09:01    |0|


Above is an example of what the data looks like. In the data/ folder, each .csv file is trajectories for 5 drivers on the same day. Each trajectory step is detailed with features such as longitude, latitude, time, and status. Data can be found at [Google Drive](https://drive.google.com/open?id=1xfyxupoE1C5z7w1Bn5oPRcLgtfon6xeT)
#### Feature Description 
* **Plate**: Plate means the taxi's plate. In this project, we change them to 0~5 to keep anonymity. The same plate means the same driver, so this is the target label for the classification. 
* **Longitude**: The longitude of the taxi.
* **Latitude**: The latitude of the taxi.
* **Time**: Timestamp of the record.
* **Status**: 1 means the taxi is occupied and 0 means a vacant taxi.

#### Problem Definition
Given a full-day trajectory of a taxi, you need to extract the sub-trajectories of each 100 steps and predict which taxi driver it belongs to. 

#### Evaluation 
Five days of trajectories will be used to evaluate your submission. And test trajectories are not in the data/ folder. 

## Some Tips
Setup information could also be found in the [slides](https://docs.google.com/presentation/d/148pBkhw4HqGjkQGkOdsXjJw_B3rzVgi6Brq6fc7r8mE/edit?usp=sharing)
* Anaconda and virtual environment set tup
   * [Download and install anaconda](https://www.anaconda.com/distribution/)
   * [Create a virtual environment with commands](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands)
* Deep learning package
   * [Pytorch](https://pytorch.org/tutorials/)
   * [MxNet](https://mxnet.apache.org/)
* Open source GPU
   * [Turing](https://arc.wpi.edu/cluster-documentation/build/html/index.html)
   * [Using GPU on Google Cloud](https://github.com/yanhuata/DS504CS586-S20/blob/master/project2/keras_tutorial.ipynb)
   * [Cuda set up for Linux](https://docs.google.com/document/d/1rioVwqvZCbn58a_5wqs5aT3YbRsiPXs9KmIuYhmM1gY/edit?usp=sharing)
   * [Google colab](https://colab.research.google.com/notebooks/gpu.ipynb)
   * [Kaggle](https://www.kaggle.com/dansbecker/running-kaggle-kernels-with-a-gpu)
* **Keywords**. 
   * If you are wondering where to start, you can try to search "sequence classification", "sequence to sequence" or "sequence embedding" in Google or Github, this might provide you some insights.
   

