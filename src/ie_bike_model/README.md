## README File containing information on how to run the application runs


## Python Project Requirements 

Having being given the bike-sharing dataset, the main purpose was to predict the the number of bikes being used in a given day, time and with certain climate conditions amongst
other pre-determined parameters.

## Tha available package consists of: 

- ie-bike-sharing-model-lib-ref
- an app.py  (used to launch Flask)
-  ie_bike_model (a library that contains:
        1. model.py
                  a) consists of funtions in order to predict the above mentions bikes
                  b) (Feature Engineering, PreProcessing, Dummify, train_xgboost, train_ridge, train_lasso...Predict)
                  c) the train_xgboost, ridge and lasso are the models that will be used in order to predict the number of bikes in the city.
        2. util.py
                  a) contains the part of the code that allows call back for the model to change to any one you choose, and directs it to the path of the direcory.  
        3. _init_.py.
once the code in each file has been adjusted and set to the standards of the prediction model, on the terminal we run the following

## From the main folder ie_bike_model-lib-ref, run "pip install ." - this is to ensure the package is correct. 
$ pip install .

## install black
$ pip install black 

# inside the file ie_bike_model run black on all the files model to see if all functions well - pie = good, broken heart = bad
$ black model.py

# Once the all the files have been checked and functioning, models have been created in the model.py, and parameters have been properly linked in app.py and util,
# we are now ready to check and get results using Flask.  

$ pip install flask

# with what we created in the app.py, we run:
$ env FLASK_APP=app.py flask run

A web link application will be created and provide us the information of the prediction of bikes according to the given parameters stated. The default model being
used is xgboost, however we have provided 2 other models to use to help in the predicition - Ridge and Lasso.
the parameters are adjustable to suit the users needs, as is the model.


The web application will show us what we programmed in the app.py.

# in a webpage enter the following url:
http://127.0.0.1:5000/predict?date=2012-05-23T18:00:00&weathersit=1&temperature_C=30&feeling_temperature_C=30&humidity=30.0&windspeed=0.0&model=xgboost

 






