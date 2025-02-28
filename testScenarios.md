### Test Scenarios


The below three scenarios all represent variants of a user successfully purchasing a single product from the list. 

## User should be able to successfully purchase a single product(Sanity + happy flow)
Login
    - verify landing page is visible
Add the product to cart 
    - verify by checking the button status
    - verify cart count
Goto cart 
    - verify if the product is added
    - verify product value should be same as product selected
Go to checkout step one
    - verify users can enter their details
    - verify user can continue upon filling details
Go to checkout step two
    - verify the total price is available
Complete checkout for a successful Purchase 

## User should be able to successfully purchase a single product via product details screen
Login
    - verify landing page is visible
Go to product details screen
    - verify the details screen is visible    
Add the product to cart 
    - verify by checking the button status
    - verify cart count
Goto cart 
    - verify if the product is added
    - verify product value should be same as product selected
Go to checkout step one
    - verify users can enter their details
    - verify user can continue upon filling details
Go to checkout step two
    - verify the total price is available
Complete checkout for a successful Purchase 

## User should be able to successfully purchase a single product after sorting and changing cart items
Login
    - verify landing page is visible
Sort inventory list
    - verify the list is sorted
Add the product to cart 
    - verify by checking the button status
    - verify cart count
Goto cart 
    - verify if the product is added
    - verify product value should be same as product selected
Remove selected item
    - verify if the item is removed
Continue shopping
Add the product to cart 
    - verify by checking the button status
    - verify cart count
Goto cart 
    - verify if the product is added
    - verify product value should be same as product selected
Go to checkout step one
    - verify users can enter their details
    - verify user can continue upon filling details
Go to checkout step two
    - verify the total price is available
Complete checkout for a successful Purchase 


## User should be able to successfully purchase a single product after relogging
Login
    - verify landing page is visible
Add the product to cart 
    - verify by checking the button status
    - verify cart count
Logout
Login
    - verify landing page is visible
Goto cart 
    - verify if the product is added
    - verify product value should be same as product selected
Go to checkout step one
    - verify users can enter their details
    - verify user can continue upon filling details
Go to checkout step two
    - verify the total price is available
Complete checkout for a successful Purchase 

Based on the behavior of the website, some assumptions are made and some negative scenarios are as below.

## Assumptions
1. If there are no items in the cart, user should not be able to checkout
2. User should be able to purchase more than 1 quantity for a selected product
3. I am testing for the flow and navigation more than the UI values. We use data-test selector instead of what user sees to locate an item. Some places I have used something lik e button:has-text for variation. However, since the developers have given us a dedicated hook data-test, i have used it across the system so that the tests are consistent.

## Verify the checkout when no products are added
Login(landing page is visible)
Goto cart (no products should be added)
Checkout(checkout should fail)
Product purchase is unsuccessful

## Verify whether the user is able to successfully purchase more than one quantity of any product
Login(landing page is visible)
Select the Product- add to cart
Goto cart (verify if the product is added)
Increase the 'Qty' to 2 (User should be able to increase quantity)
Product purchase is unsuccessful

## Reset app not working