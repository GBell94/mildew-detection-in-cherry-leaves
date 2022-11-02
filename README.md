## Dataset Content
* The dataset is sourced from [Kaggle](https://www.kaggle.com/codeinstitute/cherry-leaves). We created a fictitious user story where predictive analytics can be applied in a real project in the workplace.
* The dataset contains +4 thousand images taken from client's crop fields. The images show cherry leaves that are healthy and cherry leaves that contain powdery mildew, which is a fungal disease that affects a wide range of plants. The cherry plantation crop is one of their finest products in the portfolio and the company is concerned about supplying the market with a product of compromised quality.



## Business Requirements
The cherry plantation crop from Farmy & Foods is facing a challenge where their cherry plantations have been presenting powdery mildew. Currently, the process is to manually verify if a given cherry tree contains powdery mildew. An employee spends around 30 minutes in each tree, taking a few samples of tree leaves and verifying visually if the leaf tree is healthy or has powdery mildew. If it has powdery mildew, the employee applies a specific compound to kill the fungus. The time spent applying this compound is 1 minute.  The company has thousands of cherry trees located in multiple farms across the country. As a result, this manual process is not scalable due to time spent in the manual process inspection.

To save time in this process, the IT team suggested an ML system that is capable of detecting instantly, using a leaf tree image, if it is healthy or has powdery mildew. A similar manual process is in place for other crops for detecting pests, and if this initiative is successful, there is a realistic chance to replicate this project to all other crops. The dataset is a collection of cherry leaf images provided by Farmy & Foods, taken from their crops.


* 1 - The client is interested in conducting a study to visually differentiate a cherry leaf that is healthy and that contains powdery mildew.
* 2 - The client is interested to predict if a cherry leaf is healthy or contains powdery mildew.


## Hypothesis and how to validate?
1 - Cherry leaves with powdery mildew display clear markings/signs of the disease to differentiate them from healthy leaves.
* Validate by comparing the 'mean' images of healthy and mildew-infected leaves.


## Rationale to map the business requirements to the Data Visualizations and ML tasks
Business requirement 1: Data Visualization
* The client wants to display the 'mean' and 'standard deviation' images for cherry leaves that are healthy and those that have powdery mildew in order to visually differentiate them.
* The client wants to display the difference between the 'mean' image for a healthy cherry leaf and the 'mean' image of a leaf that has mildew in order to visually differentiate them.
* The client wants to display an image montage of healthy cherry leaves and those which have powdery mildew in order to visually differentiate them.

Business requirement 2: Classification
* The client wants to be able to predict if a given cherry leaf is healthy or has been infected with powdery mildew.
* The client wants to build a binary classification ML model and generate reports.


## ML Business Case
* We want an ML model to predict if a cherry leaf is healthy or has powdery mildew. It is a supervised, two-class, single-label classification model.
* Our ideal outcome is to provide Farmy & Foods with a faster, easier and more accurate way of predicting whether a cherry tree has been infected with powdery mildew which is scalable across their farms.
* The model success metrics are: accuracy of 97% or higher on the test set.
* The model output is a statement indicating whether a cherry leaf is healthy or has powdery mildew, together with the associated probability of being healthy or not. Employees will take images of the leaves and upload them to the app.
* Heuristics: Currently, Farmy & Foods use a manual process to verify if a cherry tree is affected by powdery mildew. An employee is required to take samples of leaves from each tree and visual criteria are used to decide if the tree is healthy or not. This process is open to human error, leading to inaccurate designation of a tree as healthy/infected. In addition, the employee typically needs to spend 30 minutes in each tree for this task, which is not scalable given the number of trees and different locations. 
* The training data is a set of over 4000 cherry tree leaf images supplied by Farmy & Foods and stored in a [Kaggle dataset directory](https://www.kaggle.com/codeinstitute/cherry-leaves).
    * Train data: target - healthy or not; features - all images in dataset.


## Dashboard Design
### Page 1 - Project Summary

* General Information
    * Powdery mildew is a fungal disease affecting a wide range of plants. 
    * Samples of leaves are taken and inspected visually for signs of mildew. 
* Project Dataset
    * The available dataset contains 4208 images of cherry leaves which are healthy and ones which show signs of powdery mildew taken from Farmy & Foods' crops.
* Business Requirements
    * The client is interested in conducting a study to visually differentiate a cherry leaf that is healthy and that contains powdery mildew.
    * The client is interested to predict if a cherry leaf is healthy or contains powdery mildew.    

### Page 2 - Leaf Visualizer
* Business requirement 1: The client wants to be able to predict if a given cherry leaf is healthy or has been infected with powdery mildew.
    * Checkbox - Average and variability images of healthy and powdery mildew cherry leaves
    * Checkbox - Differences between average healthy and average powdery mildew cherry leaves
    * Checkbox - Image montage for healthy and powdery mildew cherry leaves
    
### Page 3 - Mildew Detector
* Business requirement 2: The client would like to predict whether a given cherry leaf is healthy or has powdery mildew.
    * Link to download a set of cherry leaf images for live prediction.
    * User interface with a file uploader widget. The user should upload multiple images. For each image, it will display the image and a prediction statement, indicating if a cherry leaf is healthy or contains powdery mildew, together with the probability associated with the statement. 
    * A table with the image name and image prediction results.
    * A download button to download the table. 

### Page 4 - Project Hypothesis
* A block with a statement of the project hypothesis, the conclusion and how this was validated.

### Page 5 - ML Performance Metrics
* Bar charts of label frequencies for the Train, Validation and Test sets.
* Model history - line plots of the accuracy and loss.
* Model evaluation results - table showing the Test set performance. 


## Unfixed Bugs
* You will need to mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a big variable to consider, paucity of time and difficulty understanding implementation is not a valid reason to leave bugs unfixed.

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly in case all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.


## Main Data Analysis and Machine Learning Libraries
* Here you should list the libraries you used in the project and provide example(s) on how you used these libraries.


## Credits 

* The project was built using the Code Institute pre-prepared template.
* The app style and code are adapted from the Code Institute walkthrough project for the Malaria Detector.
* Additional code has been adapted from the Predictive Analytics course materials: Image Analysis and TensorFlow.


### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign up page are from This Open Source site
- The images used for the gallery page were taken from this other open source site
