## E-commerce cart system

## Overview

This Python program implements a basic E-Commerce Cart System consisting of three classes: `Product`, `CartItem`, and `Cart`. Users can add products to their cart, update quantities, remove items, and calculate the total bill. Each product has attributes such as name, price, availability, and an optional discount percentage.

## Classes

### `Product`

The `Product` class represents a product with the following attributes:

- `name`: The name of the product.
- `price`: The price of the product.
- `available`: Indicates whether the product is in stock (default is `True`).
- `discount_percentage`: The discount percentage for the product (default is `0`).

#### Methods

- `discount()`: Calculates the discounted price based on the discount percentage.
- `display_products()`: Returns a formatted string displaying the product's name, price, availability status, and discount (if applicable).

### `CartItem`

The `CartItem` class represents an item in the shopping cart. It includes the following attributes:

- `product`: A reference to the `Product` object.
- `quantity`: The quantity of the product in the cart.

#### Methods

- `calculate_item_total()`: Calculates the total cost of the item (taking into account the product's discount).
- `cart_items()`: Returns a formatted string displaying the item's name, quantity, and total cost.

### `Cart`

The `Cart` class manages the shopping cart, which contains a list of `CartItem` objects.

#### Methods

- `add_cart(product, quantity)`: Adds a product to the cart with the specified quantity if it is available.
- `update_item(product_name, new_quantity)`: Updates the quantity of a specific product in the cart.
- `remove_item(product_name, quantity_to_remove)`: Removes a specified quantity of a product from the cart.
- `calc_total_bill()`: Calculates the total bill by summing up the total cost of all items in the cart.
- `cart_contents()`: Returns a list of formatted strings, each representing an item in the cart.

## Usage

To use the program, follow these steps:

1. Create `Product` objects with the desired attributes.
2. Create a `Cart` object.
3. Add products to the cart using the `add_cart` method.
4. Update item quantities using the `update_item` method.
5. Remove items using the `remove_item` method.
6. Calculate the total bill using the `calc_total_bill` method.
7. Retrieve and display product information and cart contents.

## Example

Here is an example of how to use the E-Commerce Cart System:

```python
laptop = Product("Laptop", 1000, discount_percentage=10)
headphones = Product("Headphones", 50, discount_percentage=15)
TV = Product("TV", 2000, discount_percentage=5)
mobile_phone = Product("Mobile Phone", 1500, discount_percentage=7)

cart = Cart()

cart.add_cart(laptop, 2)
cart.add_cart(headphones, 2)
cart.add_cart(TV, 1)
cart.add_cart(mobile_phone, 3)

cart.update_item("Laptop", 3)
cart.update_item("TV", 1)
cart.remove_item("Headphones", 1)
cart.remove_item("Mobile Phone", 1)

total_bill = cart.calc_total_bill()

# Display product information and cart contents
# ...

print("Total Bill:", f"Your total bill is INR {total_bill}.")
```

## Customization

You can customize the products, their attributes, and the discount percentages according to your needs. Modify the `Product` objects and the `Cart` operations accordingly.

## Contributions

Contributions to this project are welcome. Feel free to submit pull requests or report any issues on the GitHub repository.

## License

This program is provided under the MIT License. See the [LICENSE](LICENSE) file for details.

Happy shopping! 🛒🎉
