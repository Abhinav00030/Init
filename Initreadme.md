class Car:
# Class variable to keep track of the total number of cars
    total_cars = 0

    def __init__(self, make, model, year, color):
  # Instance variables
        self.make = make
        self.model = model
        self.year = year
        self.color = color
        
  # Initialize the speed to 0
        self.speed = 0
        
  # Increment the total number of cars
        Car.total_cars += 1
    
    def accelerate(self, speed_increase):
  # Method to increase the car's speed
        self.speed += speed_increase
        print(f"{self.make} {self.model} is now going {self.speed} km/h")

# Create an instance of the Car class
my_car = Car("Toyota", "Corolla", 2022, "Blue")

# Access instance variables
print(f"My car is a {my_car.year} {my_car.make} {my_car.model}")

# Call a method on the instance
my_car.accelerate(50)

# Access class variable
print(f"Total number of cars created: {Car.total_cars}")
