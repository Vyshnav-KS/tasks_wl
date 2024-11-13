# Unit Testing with Pytest: Shopping Cart Example

This project demonstrates how to use **unit testing** in Python using **Pytest**, with a simple Shopping Cart implementation. It includes examples of mocking with `unittest.mock` to simulate dependencies like a database for item pricing.

## Files in the Project

### 1. `shopping_cart.py`
- **Description**: 
  - This file defines the `ShoppingCart` class, which supports basic operations like adding items, checking the cart size, retrieving items, and calculating total prices based on external pricing data.
- **Key Methods**:
  - `add(item: str)`: Adds an item to the cart if the maximum size is not exceeded.
  - `size()`: Returns the current number of items in the cart.
  - `get_items()`: Retrieves a list of items in the cart.
  - `get_total_price(price_map)`: Calculates the total price of items using a given price map.

### 2. `item_database.py`
- **Description**:
  - A simple class representing an external database used to fetch the price of items.
  - The `get(item: str)` method is designed to be mocked during testing to isolate unit tests from actual database calls.

### 3. `test_shopping_cart.py`
- **Description**:
  - This file contains unit tests for the `ShoppingCart` class using **Pytest**.
  - It includes test cases to verify adding items, checking cart contents, handling cart overflow, and calculating total prices with mocked database responses.
- **Key Tests**:
  - `test_can_add_item_to_cart()`: Verifies that an item can be added to the cart.
  - `test_when_item_added_then_cart_contains_item()`: Checks if the cart contains the added item.
  - `test_when_add_more_than_max_items_should_fail()`: Ensures adding more items than the maximum capacity raises an error.
  - `test_can_get_total_price()`: Tests the total price calculation using mocked item prices from `ItemDatabase`.

## How to Run Tests
1. **Install Pytest**:
   ```bash
   pip install pytest
   ```
2. **Run Tests**:
    ```bash
    pytest
    ```
## Presentation
For a detailed explanation and code walkthrough, check out the Figma presentation: [Unit Testing Presentation](https://www.figma.com/deck/4haSXFK7UjzTIjOexeEBdt/unit_test?node-id=16-311&t=9JhOHowcyQHOwgLw-1)

## Contact
- Author: Vyshnav K S
- Email: [vyshnavks85@gmail.com](mailto::vyshnavks85@gmail.com)