# Simple Sales Chatbot for a Tech Store

def sales_chatbot():
    print("Welcome to Elevate Tech Store 🛒")
    print("We sell Laptops, Mobiles, and Headphones.")
    print("Type 'exit' to leave.\n")

    products = {
        "laptop": 50000,
        "mobile": 20000,
        "headphones": 3000
    }

    cart = 0

    while True:
        user_input = input("You: ").lower()

        if user_input == "exit":
            print("Bot: Thank you for visiting! 🛍️")
            break

        elif "price" in user_input:
            for item, price in products.items():
                print(f"Bot: {item.capitalize()} costs ₹{price}")

        elif "buy" in user_input:
            for item in products:
                if item in user_input:
                    cart += products[item]
                    print(f"Bot: {item.capitalize()} added to cart.")
                    break
            else:
                print("Bot: Please specify a product to buy.")

        elif "total" in user_input:
            print(f"Bot: Your total bill is ₹{cart}")

        else:
            print("Bot: i didnt understand your input.")

# Run chatbot
sales_chatbot()
total
