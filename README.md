# iris
testing fast api with a simple sklearn regressor on iris data set


# some notes
docker build . -t iris #to builde the image

docker run -i -d -p 8080:5000 iris #to generate the container

http://localhost:8080/healthcheck #to get healthcheck

curl 'http://localhost:8080/iris/classify_iris' -X POST -H 'Content-Type: application/json' -d '{"sepal_l": 5, "sepal_w": 2, "petal_l": 3, "petal_w": 4}' #to get a prediction

localhost:8080/docs #for fastapi's swagger UI to test requests 





# to dos
- save a pickle file of the trained model to be loaded for predictions
- make a "health bar" interface with prediction probability