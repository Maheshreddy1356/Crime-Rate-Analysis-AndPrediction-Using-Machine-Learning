import matplotlib.pyplot as plt
import numpy as np
import time
from matplotlib.ticker import FuncFormatter
import random
import matplotlib.cm as cm

# List of Indian states
states = [
    "Andhra Pradesh", "Arunachal Pradesh", "Assam", "Bihar", "Chhattisgarh",
    "Goa", "Gujarat", "Haryana", "Himachal Pradesh", "Jharkhand",
    "Karnataka", "Kerala", "Madhya Pradesh", "Maharashtra", "Manipur",
    "Meghalaya", "Mizoram", "Nagaland", "Odisha", "Punjab",
    "Rajasthan", "Sikkim", "Tamil Nadu", "Telangana", "Tripura",
    "Uttar Pradesh", "Uttarakhand", "West Bengal"
]

# Initialize crime rate data (randomly generated for demonstration)
crime_rates = np.random.randint(10, 50, len(states))
years = [2020, 2021, 2019, 2022, 2023]  # Year data for each state (example)
crime_types = ['Murder', 'Robbery', 'Assault', 'Burglary', 'Fraud']
import matplotlib.pyplot as plt
import numpy as np
import time
from matplotlib.ticker import FuncFormatter
import random
import matplotlib.cm as cm

# List of Indian states
states = [
    "Andhra Pradesh", "Arunachal Pradesh", "Assam", "Bihar", "Chhattisgarh",
    "Goa", "Gujarat", "Haryana", "Himachal Pradesh", "Jharkhand",
    "Karnataka", "Kerala", "Madhya Pradesh", "Maharashtra", "Manipur",
    "Meghalaya", "Mizoram", "Nagaland", "Odisha", "Punjab",
    "Rajasthan", "Sikkim", "Tamil Nadu", "Telangana", "Tripura",
    "Uttar Pradesh", "Uttarakhand", "West Bengal"
]

# Initialize crime rate data (randomly generated for demonstration)
crime_rates = np.random.randint(10, 50, len(states))
years = [2020, 2021, 2019, 2022, 2023]  # Year data for each state (example)
crime_types = ['Murder', 'Robbery', 'Assault', 'Burglary', 'Fraud']  # Crime types

# Create a colormap to assign distinct colors to states
colors = cm.rainbow(np.linspace(0, 1, len(states)))

# Create initial bar graph
fig, ax = plt.subplots(figsize=(14, 8))
bars = plt.bar(states, crime_rates, color=colors)
plt.xlabel('States')
plt.ylabel('Crime Rate')
plt.title('Crime Rate Prediction for Indian States')

# Function to format tooltips
def format_tooltip(x, pos):
    ind = int(x + 0.5)  # Round to the nearest bar
    return f'State: {states[ind]}\nYear: {random.choice(years)}\nMonth: {random.choice(["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"])}\nCrime Rate: {crime_rates[ind]}\nCrime Type: {random.choice(crime_types)}'

# Add tooltips to the bars
formatter = FuncFormatter(format_tooltip)
ax.xaxis.set_major_formatter(formatter)

# Function to update the bar graph with new data
def update_graph():
    global crime_rates
    crime_rates = np.random.randint(10, 50, len(states))  # Simulate new crime rate data
    for bar, rate in zip(bars, crime_rates):
        bar.set_height(rate)
    plt.draw()

# Update the graph in real-time
while True:
    update_graph()
    plt.pause(5)  # Update every 5 seconds

# Close the graph when finished
plt.show()
