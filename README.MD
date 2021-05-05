# Traffic 

### Usage: 

- git clone https://github.com/prithvijitguha/TrafficSignAI.git
- pip3 install -r requirements.txt
- Usage: python traffic.py "path/to/dataset" optional: "filename to save model"



### Convolution Neutral Network to categorize roadsigns using GTSRB dataset for cs50 AI Project "Traffic"

| Model       | Model Description  | Accuracy |
| :---------  |:-------------: |--------:|
| 1st Iteration   | 1 Convolution(32), 1 Pool(2,2), 1 Hidden Layer(128 neurons) |  0.0584   |
| 2nd Iteration  | 2 Convolution(32), 1 Pool(2,2), 1 Hidden Layer(128 neurons) | 0.9592   |
| 3rd Iteration  | 2 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(128 neurons) | **0.9672**  |
| 4th Iteration  | 1 Convolution(64), 1 Pool(2,2), 1 Hidden Layer(128 neurons) |  0.0535   |
| 5th Iteration  | 2 Convolution(64), 1 Pool(2,2), 1 Hidden Layer(128 neurons) | 0.9470  |
| 6th Iteration  | 3 Convolution(32), 1 Pool(2,2), 1 Hidden Layer(128 neurons) |  **0.9673** |
| 7th Iteration | 1 Convolution(32), 1 Pool(3,3), 1 Hidden Layer(128 neurons) |   0.0553  |
| 8th Iteration | 2 Convolution(32)(Sequential), 1 Pool(5,5), 1 Hidden Layer(128 neurons) |  0.9579  |
| 9th Iteration | 2 Convolution(32), 2 Pool(5,5), 1 Hidden Layer(128 neurons) | 0.7822 |
| 10th Iteration | 2 Convolution(32), 2 Pool(2,2), 2 Hidden Layer(128 neurons) | 0.9310 |
| 11th Iteration | 2 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(256 neurons) | 0.9584 |
| 12th Iteration | 2 Convolution(32), 2 Pool(2,2), 2 Hidden Layer(256 neurons) | 0.9571  |
| 13th Iteration  | 3 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(256 neurons) Dropout(0.2) | 0.9471 |
| 14th Iteration  | 3 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(128 neurons) Dropout(0.2) | 0.9627 |
| 15th Iteration  | 3 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(128 neurons) Dropout(0.75) | 0.9438 |
| 16th Iteration  | 3 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(128 neurons) Dropout(0.4) | **0.9678** |
| 17th Iteration  | 2 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(128 neurons) Dropout(0.4) |  0.9231 |
| 18th Iteration  | 3 Convolution(32), 3 Pool(2,2), 1 Hidden Layer(128 neurons) Dropout(0.4) | 0.9276 |
| 19th Iteration  | 3 Convolution(32), 2 Pool(2,2), 1 Hidden Layer(64 neurons) Dropout(0.4) | 0.9237 |
  
    
      
        
## Conclusion: 

First iteration did not perform well, accuracy only ay 0.0584. Later iterations added another convolution layer increased accuracy to 0.9592. Other iterations tried increasing pool size reduced accuracy to 0.7822. Increasing hidden layers and increasing number of neurons yielded accuracy of 0.9584 and 0.9571. Increasing pool layers and two convolution layers sequentially yielded results above 0.94 accuracy. Reducing dropout to 0.2 resulted in accuracy of 0.9627, however increasing dropout to 0.75 resulted in accuracy of 0.9438. 

Highest results were achieved with a combination of 2/3 convolution layers with 2 pooling layers and 1 hidden layer of 128 neurons. Amongst the 18 iterations, highest peroforming was a combination of 3 convulation layers, 2 pooling layers, 1 hidden layer of 128 neurons and a dropout of 0.4 with a result of 0.9678.  




         
     