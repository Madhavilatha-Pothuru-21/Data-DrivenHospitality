# Data-DrivenHospitality
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

def load_data(file_path):
    # Load data from the CSV file into a Pandas DataFrame
    data = pd.read_csv(file_path)
    return data

def preprocess_data(data):
    # Data preprocessing steps (if required)
    # For example, converting date columns to proper datetime format, handling missing values, etc.
    # ...

    return data

def visualize_ratings(data):
    # Visualize the ratings of Radisson hotels using a bar plot
    plt.figure(figsize=(10, 6))
    sns.barplot(x='Hotel Name', y='Rating', data=data)
    plt.xlabel('Hotel Name')
    plt.ylabel('Rating')
    plt.title('Ratings of Radisson Hotels')
    plt.xticks(rotation=45, ha='right')
    plt.tight_layout()
    plt.show()

def main():
    # Provide the path to the CSV file containing the hotel data
    file_path = 'path/to/your/radisson_hotels_data.csv'

    # Load the data from the CSV file
    data = load_data(file_path)

    # Preprocess the data if required
    data = preprocess_data(data)

    # Visualize the ratings of Radisson hotels
    visualize_ratings(data)

if __name__ == "__main__":
    main()
