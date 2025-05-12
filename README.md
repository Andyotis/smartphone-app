# Class 1: Smartphone
class Smartphone:
    # Constructor to initialize the smartphone with unique values
    def __init__(self, brand, model, price, color):
        self.brand = brand
        self.model = model
        self.price = price
        self.color = color

    # Method to display the smartphone details
    def display_info(self):
        return f"{self.brand} {self.model} ({self.color}) - KES {self.price}"

    # Method to make a call
    def make_call(self, number):
        return f"Calling {number} from {self.brand} {self.model}..."

    # Method to send a text
    def send_text(self, number, message):
        return f"Sending message to {number}: {message}"

    # Method to play a song
    def play_song(self, song_title):
        return f"Playing '{song_title}' on {self.brand} {self.model}"


# Class 2: Animal with Polymorphism
# Base class: Animal
class Animal:
    def move(self):
        pass  # This will be overridden by subclasses


# Derived class: Dog
class Dog(Animal):
    def move(self):
        return "Running 🐕"


# Derived class: Bird
class Bird(Animal):
    def move(self):
        return "Flying 🐦"


# Derived class: Fish
class Fish(Animal):
    def move(self):
        return "Swimming 🐟"


# Derived class: Snake
class Snake(Animal):
    def move(self):
        return "Slithering 🐍"


# Main execution
if __name__ == "__main__":
    # Example of creating a Smartphone object
    phone = Smartphone("Samsung", "Galaxy S22", 75000, "Phantom Black")
    print("Smartphone Info:")
    print(phone.display_info())  # Display phone info
    print(phone.make_call("+254712345678"))  # Make a call
    print(phone.send_text("+254712345678", "Hello, how are you?"))  # Send a text
    print(phone.play_song("Blinding Lights"))  # Play a song
    print("\n")

    # Polymorphism with Animals
    print("Animal Movements:")
    animals = [Dog(), Bird(), Fish(), Snake()]

    for animal in animals:
        print(animal.move())  # Calls the move() method of each animal
