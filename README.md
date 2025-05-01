# Employee-churn-prediction-complete-streamlit-integration
A variation of my previous project, this time refactored to be easier to add to streamlit cloud

## Live Demo
[Streamlit App Link](https://employee-churn-prediction-complete-app-integration-l87w5zem35k.streamlit.app/)

**Important to note.** <br>
When runing the prediction directly it is 0.1% more accurate than running it as a deployable microservice. As is run from the link above. <br>
The way that [this original repository] (https://github.com/MortalWombat-repo/Employee-churn-prediction) was organized was to provide a easy to deploy service <br>
that utilizes best practices at the cost of 0.1% accuracy (negligible in logistic regression tasks), which was later refactored so users could run the project 
directly on Streamlit without needing to set it up specifically, as Streamlit does not allow Dockerized environments and microservices. <br>
The loss of precision occurs in the main repo due to JSON serialization when a POST request is made to the service, which does not occur in the Streamlit app <br>
as everything is dirict and in one file. Even though the difference is negligible it was worth to point out so there is no confusion why the same settings in two projects <br>
give slightly differing results.
