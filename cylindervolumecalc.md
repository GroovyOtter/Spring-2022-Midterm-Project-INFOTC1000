###This program was written in python.  

Back to [ReadMe](README.md)



```import math

def input_error_from_user(prompt):
    while (True):
        try:
            input_value = float(input(prompt))
            if (input_value < 0):
                print("Negative numbers are not accepted.  Please enter a positive number.")
                continue
            break
        except ValueError:
            print("Only numbers are accepted.  Please enter a number.")
            continue
    return input_value
        
def calculate_volume_of_cylinder():
        radius = input_error_from_user("What is the radius of the cylinder? ")
        height = input_error_from_user("What is the height of the cylinder? ")
    
        volume = math.pi * radius ** 2 * height
        print("The volume of the cylinder is", volume)

def main():
    print("This program calculates the volume of a cylinder.")
    while True:
        calculate_volume_of_cylinder()
        repeat = input("Would you like to perform another calculation? enter y/n ")
        if (repeat == "y"):
            print("")
            continue
        else:
            break
main()
```
            


