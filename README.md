# overview
This is my repository for the second project of the Azure Machine Learning Engineer Nanodegree.<br>
<br>
The goal of this project is to train a machine learning model for production with automl, deploy it and consume it.<br>
This same process is also done via Azure Pipelines. <br>
# architectural diagram
[!image](https://github.com/hualcosa/nd00333_AZMLND_C2/assets/46836901/6ddefd9d-69a9-44d5-9daa-efd719556ab5)

1. Authentication
  <div style="text-align: right"> 
  In this step, you will need to install the Azure Machine Learning Extension which allows you to interact with Azure Machine Learning
  Studio, part of the az command. After having the Azure machine Learning Extension, you will create a Service Principal account and
  associate it with your specific workspace.
  <br>
 </div>
 Service principal creation:<br>
[!service_principal.png](https://github.com/hualcosa/nd00333_AZMLND_C2/blob/master/sample_screenshots/service_principal_creation.png)

2. Automated ML Experiment
4. Deploy the best model
5. Enable logging
6. Swagger Documentation
7. consume model endpoints
8. Create and publish a pipeline
9. writing this documentation :)

# Youtube screencast
I have made a short video going through the above steps, so you can have an even better understanding of the complete workflow.
I hope it helps!<br>
[![Watch the video](https://img.youtube.com/vi/u1ShrRVKxbQ/maxresdefault.jpg)](https://studio.youtube.com/video/u1ShrRVKxbQ/edit)

# future improvements
All the work done in the project used version 1 of azureml Python SDK, but Python SDK version 2 is already available. A good experiment would be to repeat the steps outlined above using the newest version of the API and document the differences.
# screenshots along the way
# link to screencast video
