# python_hwk

#Import OS and CSV
import os
import csv
cwd = os.getcwd()
file = os.path.join(cwd, 'Resources', 'budget_data.csv')

#Define variables
        totalMonth = 0
        totalRevenue = 0
        previousRevenue = 0
        revenue_change = 0
        revenue_change_list = []
        month_of_change = []
        greatestincrease = ["",0]
        greatestdecrease = ["",9999999999]

#Calculations for total months and total profits/losses
    for row in csv_reader:
        totalMonth = totalMonth + 1
        totalRevenue = totalRevenue + int(row["Revenue"])
        revenue_change = int(row["Revenue"]) - previousRevenue
        previousRevenue = int(row["Revenue"])
        month_of_change = month_of_change + [row["Date"]]

#Average of the changes in the Profits/Losses, Net Total of Profits/losses and greatest increase/decrease in profits/losses
    If (revenue_change<greatestDecrease[1])
    greatestDecrease[0] = row["Date"]
    greatestDecrease[1] = revenue_change
    
    revenue_avg = sum(revenue_change_list)/len(revenue_change_list)
 
    output = (f"Total Months: {totalMonth}\n"
          f"Total Revenue:{totalRevenue}\n"
          f"Average Revenue:${revenue_avg:.2f}\n"
          f"Greatest increase in Revenue: {greatestDecrease[0]} (${greatestDecrease[1]})\n")
    
    print(output)
    with open(pathout,"w") as txt_file:
        txt_file.write(output)
              
              # Print the output (to terminal)
print(output)

# Export the results to text file
with open(file_to_output, "w") as txt_file:
    txt_file.write(output)
