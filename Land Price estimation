import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

data = {
    'Square_Feet': [1000, 2000, 3000, 4000, 5000, 6000, 7000, 8000, 9000, 10000],
    'No_of_Rooms': [2, 3, 4, 5, 5, 6, 7, 8, 9, 10],
    # Prices roughly follow: (SqFt * 0.15) + (Rooms * 20)
    'Price_K': [190, 360, 530, 700, 850, 1020, 1190, 1360, 1530, 1700] 
}

df = pd.DataFrame(data)

X = df[['Square_Feet', 'No_of_Rooms']]
y = df['Price_K']
model = LinearRegression().fit(X, y)

def run_app():
    print("----welcome to House Price Predictor----")
    print("advice for properties up to 10,000 sq. feet.")
    print("-" * 50)

    try:
        sq_ft = float(input("Enter Square Footage (e.g., 2000): "))
        rooms = int(input("Enter Number of Rooms (e.g., 4): "))

        existing_price = df[(df['Square_Feet'] == sq_ft) & (df['No_of_Rooms'] == rooms)]

        if not existing_price.empty:
            actual_val = existing_price['Price_K'].values[0]
            print(f"\nMatch Found!,a {sq_ft} sq. ft. house with {rooms} rooms costs: ₹{actual_val:,.2f}k")
        else:
            prediction = model.predict([[sq_ft, rooms]])[0]
            print(f"\nNo exact match found. AI Estimated Market Price: ${prediction:,.2f}k")

        show_visuals(sq_ft, rooms)

    except ValueError:
        print("Please enter numeric values for square footage and rooms.")

def show_visuals(u_sqft, u_rooms):
    plt.figure(figsize=(10, 5))
    plt.scatter(df['Square_Feet'], df['Price_K'], color='green', label='Market Standards')
    plt.axvline(x=u_sqft, color='orange', linestyle='--', alpha=0.5, label='Your Selection')
    
    plt.title(f"Property Value Trend (Current Focus: {u_sqft} sq. ft / {u_rooms} Rooms)")
    plt.xlabel("Square Footage")
    plt.ylabel("Price (in $ Thousands)")
    plt.legend()
    plt.grid(True, alpha=0.3)
    plt.show()

if __name__ == "__main__":
    run_app()
