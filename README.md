# Receipt Drive through management project


## Objective

This project aims to test your knowledge of the data structures and use it to solve real-life problems.


## Problem

A drive-through restaurant has a problem managing the orders. The restaurant manager asked you to implement a system to manage the orders to cover and solve their issues.

Manager requirements:   
1. The restaurant can work on only 3 orders at a time. If the first order is served, we can add and work on a new order.
2. The restaurant should have 2 screens:
- `Order here` screen. 
  * Create a new order.  
  * Switch to the `Receive here` screen.  
- `Receive here` screen.
  * Serve order.
  * Print all pending orders.  
  * Switch to the `Order here` screen.
  * Close the restaurant.



  
## Requirements  

- The system starts with the `Order here` screen (when running the project, the `Order here` screen pops up).     
- The project consists of two main screens, `Order here` and `Receive here`.
- The restaurant serves Burgers, Fries, and Pepsi.
- The restaurant can work on only 3 orders at a time.  If the first order is served, we can add and work on a new order.
- All the created orders should be stored in a data structure.
- When closing the restaurant, the system should perform a "close cash" or "end of day" that produces a receipt that summarizes all transactions for that day and saves it to a file.

  
  
## Implementation  


Screens requirements and details:   


### 1. `Order here` screen.
````
Order here screen
---------------------------
1- Create a new order
2- Switch to (Receive here screen)
````
Option `1` Create a new order:   

1.1. The user should be able to add new orders.

- If the user is taking the order, the user should be able to see and choose the products from the below screen
```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```
   
- If the customer finishes ordering, the system prints the order items with each item's price and the total price.
   
 ```   
Order details:

Burger 25.00
Fries 10.00
Pepsi 5.00
Total: 40.00

1- Create/add the order and go back to the (Order Here) screen
```


- If there are 3 pending orders, the system prints a message informing the user that no orders can be added until at least one order is served.
```
Error message:
3 orders are pending, deliver one order to be able to add a new one.

1- Back to Order here screen.  
```

Option `2` Switch to Order here screen:   

1.2. The user should be able to switch the screen to the (Receive here) screen.   
<br/>
   
### 2. `Receive here` screen.

````
Receive here screen
---------------------------
1- Serve order.  
2- Print all pending orders.  
3- Switch to (Order here screen).
4- Close the restaurant.
````  

Option `1` Serve order:     

2.1. The user should be able to serve orders.   
- If the order is served, the order should be removed from the pending orders queue.   
- If there are no pending orders, the system prints a message informing the user that there are no pending orders.   
```
Error message:
There are no pending orders

1- Back to (Receive here) screen.  
```

Option `2` Print all pending orders:    

2.2. The user should be able to print all the pending orders.   

- Each order has an ID, order items, and total price.

````
All the pending orders:
Order ID: 1
Burger
Total: 25.00
Order ID: 2
Burger
Fries
Total: 35.00
Order ID: 3
Burger
Fries
Pepsi
Total: 40.00

1- Back to Receive here screen.
````

Option `3` Switch to Order here screen:   

2.3. The user should be able to switch the screen to the (Receive here) screen.

````
Order here screen
---------------------------
1- Create a new order
2- Switch to (Receive here screen)
````

Option `4` Close the restaurant:  

2.4. The user should be able to close the restaurant    
Performing this option should create a file containing the following: 
- All the created orders.
- All the transactions (orders prices).
- The total income.
- The most ordered item.

## Test your project  

Below is a test case that should run successfully when running your project:  
   
````
Order here screen
---------------------------
1- Create a new order
2- Switch to (Receive here screen)
````

User choose `1` 

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `1`

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `2`

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `3`

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `4`

```   
Order details:

Burger 25.00
Fries 10.00
Pepsi 5.00
Total: 40.00

1- Create/add the order and go back to the (Order Here) screen
```

User choose `1`

````
Order here screen
---------------------------
1- Create a new order
2- Switch to (Receive here screen)
````

User choose `1` 

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `1`

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `4`

```   
Order details:

Burger 25.00
Total: 25.00

1- Create/add the order and go back to the (Order Here) screen
```

User choose `1`

````
Order here screen
---------------------------
1- Create a new order
2- Switch to (Receive here screen)
````

User choose `1` 

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `3`

```
Take the order:  

1- Burger
2- Fries
3- Pepsi
4- Finish the order and check out
```

User choose `4`

```   
Order details:

Pepsi 5.00
Total: 5.00

1- Create/add the order and go back to the (Order Here) screen
```

User choose `1`

````
Order here screen
---------------------------
1- Create a new order
2- Switch to (Receive here screen)
````

User choose `2`

````
Receive here screen
---------------------------
1- Serve order.  
2- Print all pending orders.  
3- Switch to (Order here screen).
4- Close the restaurant.
````  

User choose `2`

````
All the pending orders:

Order ID: 1
Burger 25.00
Fries 10.00
Pepsi 5.00
Total: 40.00

Order ID: 2
Burger 25.00
Total: 25.00

Order ID: 3
Pepsi 5.00
Total: 5.00

1- Back to Receive here screen.
````

User choose `1`

````
Receive here screen
---------------------------
1- Serve order.  
2- Print all pending orders.  
3- Switch to (Order here screen).
4- Close the restaurant.
````  

User choose `1`

````
Receive here screen
---------------------------
1- Serve order.  
2- Print all pending orders.  
3- Switch to (Order here screen).
4- Close the restaurant.
````  

User choose `2`

````
All the pending orders:

Order ID: 2
Burger 25.00
Total: 25.00

Order ID: 3
Pepsi 5.00
Total: 5.00

1- Back to Receive here screen.
````

User choose `1`

````
Receive here screen
---------------------------
1- Serve order.  
2- Print all pending orders.  
3- Switch to (Order here screen).
4- Close the restaurant.
````

User choose `4`

````
The restaurant is closed successfully.
````
- A file should be created that contains all the required information mentioned in the Implementation section.
- [Receive here screen](#2-receive-here-screen)



## Qualification to pass

- [ ] The code should run successfully.  
- [ ] All requirements must be implemented.
- [ ] Test cases must run successfully.
