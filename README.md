# Discount-Counter
Made a working discount counter that takes in price and a discount as a precentage and outputs a number
def apply_discount(price, discount):
    if not isinstance(price, (int, float)):
        return "The price should be a number"
    if not isinstance(discount, (int, float)):
        return "The discount should be a number"
    if price <= 0:
        return "The price should be greater than 0"

    if discount < 0 or discount > 100:
        return "The discount should be between 0 and 100"

    result = price - (price * (discount / 100))

    if result == float(result):
        return float(result)

print(apply_discount(74.5, 20.0))
