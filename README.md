The program sending machine contains list of 6 food items with its product details like code number and price.
Now to run the program there is a flag variable called run_vend whose value is set to true.
Now there is while loop which contains the main function of the program.

As the run_vend value is set true the while loop run itself and prints the items and its details using a for loop.
Now there is a variable called 'query'   typecasted as integer datatype. This takes the code number of the item as input.
Then it runs a for loop within the items list for code. Then it checks whether the entered code is present or not.
If not present it prints "Invalid Code" else, the process of the vending machine continues and will ask to enter the money for transaction.
If the entered money is lower than the cost price, it prints ("please enter only{item['price']} Rupees") and then it will ask whether to quit or renew a purchase.
If the entered amount of money is more than the item price, it refunds the balance amount and pass on the control to quit or continue portion of the program.
If the amount entered is exact, the machine prints "Thank you for buying, here is your item" and as usual pass on the control to continue or exit portion of the loop.

Again, the query variable is used to take input as q and c for whether to quit or continue the purchase. If value entered is 'c' the flag variable run_vend is true and the
program continues to run. If the value entered is other, the program breaks itself. And if the value entered is 'q' the run_vend is false and the program stops running.

The idea of this entire project was proposed by Souvik Dutta and planned and coded by Roham Maiti and Sneha Khan. To work on this project,
online pdfs(books) on Python was used and the idea about using f-strings was taken from Geeks for Geeks and other relevant websites.
