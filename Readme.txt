U need to run all the cell except the Collecting keypoints for training and testing, Build and Train LSTM Neural Network and evaluating using confusion matrix blocks.



The last cell is bit difficult to run
it throws errors
u need to check the len of res and it should be 3 to run the code perfectly
for that u need to comment this part and run the code::


        if res[np.argmax(res)] > threshold:
            if len(sentence) > 0:
                if actions[np.argmax(res)] != sentence[-1]:
                    sentence.append(actions[np.argmax(res)])
            else:
                sentence.append(actions[np.argmax(res)])
                
after commenting the above code u need to replace 30 with 1 and run the code :
            if len(sequence) == 30:
                        res = model.predict(np.expand_dims(sequence,axis=0))[0]
                        print(actions[np.argmax(res)])

then u need to make sure the len of res becomes 3 

when it becomes 3 then u replace back the 1 with 30

After that u can uncomment the above commented code and run normally