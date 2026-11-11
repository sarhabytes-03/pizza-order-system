# Pizza Order System

A small restaurant ordering project that I built in two forms:

- `c-console/`: the original C console program (SE132 lab final), later fixed and tidied with AI help
- `web-app/`: a single-file web app version with accounts, a calculator, staff shifts and a 7-day order history

Author: Samia Sharha Bintay Kamal, Software Engineering, Daffodil International University.

## Web app

Open `web-app/index.html` in any modern browser (double-click, no install, works offline).

### What it does
- **Accounts:** one account per restaurant. Passwords are hashed in the browser. Accounts and data are stored only in this browser (localStorage); nothing is sent anywhere.
- **Menu:** the four pizzas from my C program: New York Style (400 tk), Detroit Pizza (400 tk), Neapolitan (500 tk), Vegan Pizza (300 tk). Each has a "What's on it" description and a drawn picture. The Detroit pizza is square.
- **Customise:** choose size (S, M, L, XL) and crust (Thin, Medium, Thick). Regular pizzas can take paid extra add-ons. **Create your own** builds a pizza from toppings (up to 5), the picture changes with the toppings, and it can be saved to the account's menu.
- **Calculator:** subtotal, optional promo code, 5% VAT and total. There is no delivery option because this is a restaurant system.
- **Place order:** the cart empties and a receipt shows who served the order.
- **Staff and shifts:** employees are added on the Staff tab (the first one becomes the Manager; other posts are Cashier, Waiter and Chef). An employee checks in to take over the shift, and every order is credited to whoever is checked in. Only a checked-in Manager can add or remove employees. A leaderboard shows who sold the most pizzas, and each employee has a sales history.
- **7-day history:** orders older than 7 days are deleted automatically. A banner warns when orders will be cleared within 24 hours, and **Download summary** saves a CSV file first.

### Limits (please read)
- Everything lives in one browser on one computer. Clearing browser data, or opening the file in another browser, shows an empty system. Download the summary to keep a copy.
- Login is only a convenience for this project, not real security: there is no server, and staff check-in has no PIN.
- Topping, size and crust prices, the 5% VAT and the promo code `DIU10` are sample values I chose with the AI, not real restaurant prices. Only the four pizza names and prices come from my C program. They can be changed in the constants at the top of the script.
- Sales totals per employee are kept for all time, but the order list behind the sales history only covers the last 7 days.
- Tested by hand in: _(write your browser here, for example Chrome on Windows)_.

## How AI was used
I decided what the app should do: accounts, saving pizza choices, the calculator, the 7-day log with a download, a custom pizza option, and the employee check-in and shift idea. AI (Claude) helped design and write the code, and I reviewed and changed it in several rounds. Examples of my decisions: removing the delivery option, asking for pizza pictures that show the real toppings, adding ingredient descriptions and paid add-ons, and making the Detroit pizza square.

The look was inspired by three pizza-app design references I picked; no artwork was copied (the pizzas are drawn in code).

## Original C version
The C program uses a queue for pending orders and a stack for completed orders. The fixed version in `c-console/` is described in its own README.
