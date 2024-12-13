# Step 1

1. Add LR Scheduler
2. Results:
   1. Parameters: 6,832
   2. Best Train Accuracy: 98.18
   3. Best Test Accuracy: 
      - 98.57 (11th Epoch)
      - 98.50 (14th Epoch)
3. Analysis:
   1. Finding a good LR schedule is hard. We have tried to make it effective by reducing LR by the 10th after the 6th epoch.
   2. It did help in getting to 99.4 or faster, but the final accuracy is not more than 98.57. Possibly a good scheduler can do wonders here!


# Step 2

1. Used ReduceLROnPlateau
2. Results:
   1. Parameters: 7,889
   2. Best Train Accuracy: 99.03
   3. Best Test Accuracy: 
      - 99.38 (12th Epoch)
      - 99.36 (14th Epoch)
3. Analysis:
   1. Training accuracy is not reaching to 99%, may be reducing the dropout can help.
   2. Test accuracy is also not improving so may be we need to increase the number of channnels after the first transition conv layer(i.e in the middle where we calculate the textures/Patterns , part of objects and then objects).


# Step 3

1. Used ReduceLROnPlateau and reduced dropout from 0.1 to 0.05 and increased the number of channels in the middle convolution layers
2. Results:
   1. Parameters: 7,952
   2. Best Train Accuracy: 99.27
   3. Best Test Accuracy: 
      - 99.50 (14th Epoch)
      - 99.50 (14th Epoch)
3. Analysis:
   1. The Test accuracy was maintained > 99.4 for last 5 epochs and training and test accuracies were always going up.
