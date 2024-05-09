# Instacart 

In this project, I was tasked with uncovering additional information about Instacart's sales patterns. This was achieved using Python to conduct an exploratory analysis of various customer datasets. Presented here is the project brief, scripts used, visualizations and my report summarizing my findings for the client. 


## Key Objectives

The sales team needs to know what the busiest days of the week and hours of the day are in order to schedule ads at times when there are fewer orders.

They would also like to know whether there are particular times of the day when people spend the most money, as this might inform the type of products they advertise at these times.

Instacart has a lot of products with different price tages. Marketing and sales want to use simpler price range groupings to help direct their efforts.

Are there certain types of products that are more popular than others? The marketing and sales teams want to know which departments have the highest frequency of product orders.

The marketing and sales teams are particularly interested in the different types of customers in their system and how their ordering behaviors differ. For example:
    
    What's the distribution among users in regards to their brand loyalty?

    Are there differences in ordering habits based on a customer's loyalty status?

    Are there differences in ordering habits based on a customer's region?

    Is there a connection between age and family status in terms of ordering habits?

    What different classifications does the demographic information suggest?
      Age? Income? Certain types of goods? Family status?

    What difference can you find in ordering habits of different customer profiles? Consider the price of orders, frequency of orders, products customers are ordering, and anything else that may be relevant.


### Data Dictionary
orders (3.4m rows, 206k users):

    order_id: order identifier
    user_id: customer identifier
    eval_set: which evaluation set this order belongs in (see set described below)
    order_number: the order sequence number for this user (1 = first, n = nth)
    order_dow: the day of the week the order was placed on
    order_hour_of_day: the hour of the day the order was placed on
    days_since_prior: days since the last order, capped at 30 (with NAs for order_number = 1)

products (50k rows):

    product_id: product identifier
    product_name: name of the product
    aisle_id: foreign key
    department_id: foreign key

aisles (134 rows): 

    aisle_id: aisle identifier
    aisle: the name of the aisle

departments (21 rows):

    department_id: department identifier
    department: the name of the department

order_products__SET (30m+ rows):

    order_id: foreign key
    product_id: foreign key
    add_to_cart_order: order in which each product was added to cart
    reordered: 1 if this product has been ordered by this user in the past, 0 otherwise

where SET is one of the four following evaluation sets (eval_set in orders):

    "prior": orders prior to that users most recent order (~3.2m orders)
    "train": training data supplied to participants (~131k orders)
    "test": test data reserved for machine learning competitions (~75k orders)

#### Tools 
  Pandas
  Numpy
  Seaborn
  Matplotlib
  SciPy

##### Resources


  
