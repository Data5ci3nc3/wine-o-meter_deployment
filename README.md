# Wine-o-meter deployment project
Putting a machine learning model into production by building an application programming interface (API), providing a "/predict" endpoint and a succinct documentation for the developer team at the index of the website.

## Technical expectations
- Provide at least a "/predict" endpoint whose full URL should be in the following format: https://your-url.com/predict
- This endpoint accepts POST method with JSON input data and it should return the predictions
- Provide a simple HTML documentation page about the API to the users. This HTML page should be located at the index of the website (https://your-url.com)
- The documentation should include at least an h1 title, a description of the endpoint the user can call with the endpoint name, the HTTP method, the required input and the expected output
- The API should be hosted API online on Heroku or any other hosting provider

## Assumptions
- User inputs will be always well formatted
- Errors do not have to be managed

## Methodology applied to reach the goal
- Code the "/predict" endpoint on a local machine
- Create the HTML documentation
- Test the behaviour of the API on the local machine
- Push the code to Heroku

## Caution
- On Mac or Linux shell, the request using curl should have the following format :
curl -i -H "Content-Type: application/json" -X POST -d '{"input": [[7.0, 0.27, 0.36, 20.7, 0.045, 45.0, 170.0, 1.001, 3.0, 0.45, 8.8], [7.0, 0.27, 0.36, 20.7, 0.045, 45.0, 170.0, 1.001, 3.0, 0.45, 8.8]]}' https://red-red-wine-app.herokuapp.com/predict
            
          
On Windows shell, the request using curl should have the following format :
curl -i -H "Content-Type: application/json" -X POST -d "{\"input\": [[7.0, 0.27, 0.36, 20.7, 0.045, 45.0, 170.0, 1.001, 3.0, 0.45, 8.8], [7.0, 0.27, 0.36, 20.7, 0.045, 45.0, 170.0, 1.001, 3.0, 0.45, 8.8]]}" https://red-red-wine-app.herokuapp.com/predict
