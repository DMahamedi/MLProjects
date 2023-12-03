For this report, I analyzed a UC Irvine dataset which captures whether a college student dropped out, gradauted, or is currently enrolled (https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success).

One problem I had with this dataset was that it was 3 way classification, with the third class being whether a student is enrolled or not. This really threw off all of the models I trained on the dataset, and I ended up having to remove the datapoints which corresponded to a currently enrolled student. 

I ended up achieving about 92% accuracy. If I had more time, I would have liked to analyze the decision boundaries behind the models to see what was so confusing about the possibility of a student being enrolled.
