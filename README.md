# factory method :

You are provided with a piece of code that exhibits design issues and violates good software design principles. Your task is to identify the design pattern(s) that can be applied to improve the code and refactor it accordingly. Choose one design pattern that you believe will address the design issues effectively.

Code:
```python
# Incorrect Code Snippet

class ShoppingCart:
    def __init__(self):
        self.items = []
        self.total_price = 0

    def add_item(self, item):
        self.items.append(item)
        self.total_price += item.price

    def remove_item(self, item):
        self.items.remove(item)
        self.total_price -= item.price

    def calculate_discount(self):
        if self.total_price > 100:
            return self.total_price * 0.1
        else:
            return 0

    def checkout(self):
        final_price = self.total_price - self.calculate_discount()
        print(f"Total price: {self.total_price}")
        print(f"Discount applied: {self.calculate_discount()}")
        print(f"Final price after discount: {final_price}")
```

Requirements:
1. Identify the design pattern issues in the given code snippet.
2. Choose one design pattern that can be applied to improve the code.
3. Refactor the code by implementing the chosen design pattern.
4. Provide a detailed explanation of the chosen design pattern and how it addresses the design issues in the original code.
5. Submit the refactored code along with the explanation.
