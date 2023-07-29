# Overview
This is my repository for the second project of the Azure Machine Learning Engineer Nanodegree.<br>
<br>
The goal of this project is to train a machine learning model for production with automl, deploy it and consume it.<br>
This same process is also done via Azure Pipelines. <br>
# Youtube screencast
I have made a short video going through the below steps, so you can have an even better understanding of the complete workflow.
I hope it helps!<br>
[![Watch the video](https://img.youtube.com/vi/u1ShrRVKxbQ/maxresdefault.jpg)](https://studio.youtube.com/video/u1ShrRVKxbQ/edit)
# Architectural diagram
[!image](https://github.com/hualcosa/nd00333_AZMLND_C2/assets/46836901/6ddefd9d-69a9-44d5-9daa-efd719556ab5)

1. Authentication
  <div style="text-align: justify"> 
  In this step, you will need to install the Azure Machine Learning Extension which allows you to interact with Azure Machine Learning
  Studio, part of the az command. After having the Azure machine Learning Extension, you will create a Service Principal account and
  associate it with your specific workspace.
  <br>
 </div>
 Service principal creation:<br><br>
 <img align="center" src="sample_screenshots/service_principal_creation.png">
 I'm using azure cli V2. In this version, the "az ml workspace share" was replaced by the following one:<br><br>
 <img align="center" src="sample_screenshots/az_role_assignment.png">
 
2. Automated ML Experiment
  <div style="text-align: justify"> 
  In this step, you will create an experiment using Automated ML, configure a compute cluster, and use that cluster to run the experiment.
  <br><br>
 </div>
 <p align="center">Registered dataset</p>
 <img align="center" src="sample_screenshots/registered_dataset.png">
 <p align="center">Automl experiment completed</p>
 <img align="center" src="sample_screenshots/automl_completed.png">
 <p align="center">best model found</p>
 <img align="center" src="sample_screenshots/best_model_summary.png">
3. Deploy the best model
  <div style="text-align: justify"> 
  In this step, we deploy the model. This will allow us to interact with it as a REST API sending POST requests.
  <br><br>
 </div>
4. Enable logging
<div style="text-align: justify"> 
  Now that the Best Model is deployed, I enabled Application Insights, so I can monitor and retrieve logs about the endpoints.
  <br><br>
 </div>
 <p align="center">Application insights enabled</p>
 <img align="center" src="sample_screenshots/application_insights_enabled.png">
 <p align="center">Logs after running logs.py</p>
 <img align="center" src="sample_screenshots/logs_py.png">
5. Swagger Documentation
<div style="text-align: justify"> 
  In this step, you will consume the deployed model using Swagger.
  <br><br>
 </div>
 <p align="center">Setting up swagger locally</p>
 <img align="center" src="sample_screenshots/swagger_sh.png">
 <p align="center">Running serve.py to enable CORS</p>
 <img align="center" src="sample_screenshots/serve_py.png">
 <p align="center">Using swagger api to submit a request</p>
 <img align="center" src="sample_screenshots/swagger_api.png">
 <p align="center">Score endpoint</p>
 <img align="center" src="sample_screenshots/score_endpoint.png">
6. consume model endpoints
<div style="text-align: justify"> 
  In this step, I ran the endpoints.py script after modifying the "scoring_uri" and "key" variables to match the values generated after
deploying the model.
  <br><br>
 </div>
 <p align="center">Running endpoints.py</p>
 <img align="center" src="sample_screenshots//consuming_endpoint.png">
  <p align="center">Benchmarking endpoint</p>
 <img align="center" src="sample_screenshots/apache_bench.png">

8. Create and publish a pipeline
  <div style="text-align: justify"> 
  In this part of the project, I used the jupyter notebook provided in the starter_files folder to create, publish and consume a pipeline. The pipeline will consume the bank marketing dataset, and run an automl experiment, just like the one done previously in this project, but now using the sdk. You can check the completed notebook in this repo.
  <br><br>
 </div>

<p align="center">Pipeline created and Active</p>
<img align="center" src="sample_screenshots/published_pipeline_active.png">
<p align="center">Pipeline endpoint active</p>
<img align="center" src="sample_screenshots/pipeline_rest_endpoint_active.png">
<p align="center">bankmarketing dataset being consumed by the pipeline</p>
<img align="center" src="sample_screenshots/pipeline_consuming_bankmarketing.png">
<p align="center">Monitoring the pipeline in the notebook with the runDetails widget</p>
<img align="center" src="sample_screenshots/published_pipeline_runDetails.png">
<p align="center">Schedule run job completed</p>
<img align="center" src="sample_screenshots/scheduled_run_job.png">

9. writing this documentation - CHECK

# Future improvements
All the work done in the project used version 1 of azureml Python SDK, but Python SDK version 2 is already available. A good experiment would be to repeat the steps outlined above using the newest version of the API and document the differences.
# screenshots along the way
# link to screencast video
