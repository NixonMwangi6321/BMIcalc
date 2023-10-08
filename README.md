# BMIcalc
Simple BMI calculator
def calculate_bmi(weight_kg, height_m):
    bmi = weight_kg / (height_m ** 2)
    return bmi

def interpret_bmi(bmi):
    if bmi < 18.5:
        return "You are Underweight"
    elif 18.5 <= bmi < 24.9:
        return "Your weight is Normal"
    else:
        return "You are Overweight"

def bmi_calculator():
    print("Welcome to our BMI Calculator")
    
    user_name = input("Enter your name: ")
    weight_kg = float(input("Enter your weight in kilograms (e.g., 56.7): "))
    height_m = float(input("Enter your height in meters (e.g., 2.35): "))

    bmi = calculate_bmi(weight_kg, height_m)
    weight_category = interpret_bmi(bmi)

    print(f"Hello, {user_name}!")
    print(f"Your BMI is: {bmi:.2f}")
    print(f"You are a part of the '{weight_category}' range.")

if __name__ == "__main__":
    bmi_calculator()
