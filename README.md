# DBL-ProcessMining - Group 6

The tool in this project is meant to predict the time to the next event, as well as the next event for a process database that has columns named, and in the same nature as the bpi_2017 challenge (the database contains the processes of a bank for loan admission). Given a train database, the tool uses LSTM to make a model that can be used predict the next event in a sequence of events for a specific case, as well as the time until that event. It is also able to predict the suffix given a prefix of events. 

The tool creates and saves a .csv file from a .xes file (in this case 'BPI Challenge 2017.xes').

Requirements:
- 5GB of RAM storage

How to use:
1. Have python 3.10 installed, as well as the following modules installed:
   - sklearn
   - pandas
   - tensorflow
   - matplotlib
   - ipywidgets
2. Have a file called 'BPI Challenge 2017.xes' in the tool folder or change the 'input_file_path' variable to your file path 
3. Have 'datautil.py' and tool 'ToolSprint4.ipynb' from the 'tool' folder
4. Run ToolSprint4.ipynb
5. If you want to use the suffix predictions, you need to enter in the second to last cell the row when the prefix ends and run the cell. The output comes as an array of form 'name_of_event, number of times, time from last group of events'.

Note: 
1. The tool can take quite a bit of time to run (up to 20-25 minutes). Usually progress bars are displayed when building the models with time estimations
2. Restart the kernel after installing ipywidgets to make sure that the last cell runs properly (begins to loop if the kernel is not restarted)
3. The train and test datasets have been minimized to just a 10th of their original size to make the tool possible to run and finish running during the presentation.
