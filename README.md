# Introduction
A brief report on the assgnment for the PhD position: READY: Rethinking Monitoring for Large Distributed Systems, using for calculate monitored CPU usage transmission between distributed nodes and clients under different settings.
# Answers
**2.** 1,455,840  
**3.** 743,865  
**4.** **(a)** 73,396; **(b)** 36,305; **(c)** 14,915  
**5.** **(a)** 0.990; **(b)** 1.906; **(c)** 4.182  
**6.**
![pic](https://github.com/xingxingbaobao/CPU-Monitor/blob/main/output.png)
# Structure
* `cpu - csv.csv`: CSV file containing CPU data.  
* `Assignment_for_the_PhD_position_Yixing_Zhang.ipynb`: Python script containing the code.
# Configuration and Setup
* The assignment uses **Python 3.6** or higher.  
* Install required dependencies: **pandas, matplotlib, numpy**.
# Key Features
* Read CPU usage data from a CSV file.
* Calculate the the total number of messages transmitted between nodes and the coordinator during different settings.
* Calculate Mean Absolute Error with different error threshold.   
* Visualize MAE and message transmission information.
# Code Structure
- `read_data(file_path)`: Read data from a CSV file, store it in a DataFrame, and **return** column names, total data size, and the columns of the data as a dictionary.  
- `calculate_diff(columns, column_data)`:  Calculate the count of non-equal values from the last ones in the data and **return** the total message transmission count.  
- `calculate_ε_far_diff(columns, column_data, epsilon_values)`: Calculate message transmission counts and absolute error values for different error threshold and **return** the messages count and error values as a list.  
- `calculate_MAE(error_values)`: Calculate the MAE over all nodes and monitoring rounds and **return** MAE values for different error threshold.  
- `calculate_MAE_at_C(error_values)`: Calculate MAE values at the coordinator with time and **return** a list of MAE values for different error threshold.  
- `calculate_messages_at_C(messages)`: Calculate message transmission counts at the coordinator with time and **return** a list of message transmission counts for different error threshold.  
- `plot_mae_and_messages(epsilon_values, MAE_C, messages_C)`: Visualize MAE and message transmission information in charts.  
- `main()`: Main function to execute the entire functions mentioned above.  
