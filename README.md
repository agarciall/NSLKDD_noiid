0-Create a conda env, Python version: 3.11.6, using requirements.txt
	conda create --name NAME --file requirements.txt


1- First of all, script will ask you to select the client data distribution. You can check it on the pictures in this folders. Basically:
	1: Same distribution for every client, but 3-6 classes are silenced in each client 	(some data is erased). Every client keeps "Normal" class samples.
	2: First, classes are distributed among clients. Every client has a number n of 	classes. Then, samples are distributed among the clients that are choosen to have that 	classes. Again, all clients do have "normal" class samples.

2- Second, you have to choose the total number of global epochs. Please insert and int.
3- Now it's time to choose the DoS attacks. In a normal scenario, every clients is training and sending info to the global model in every round. Please keep in mind that clients and round numbers starts at "0". 
For example, if you want the first client not to train in the first round, you have to input:
0:0

If you want first client and second client not to train in first and third round:
0:0,1;2:0,1
