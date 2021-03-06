# Lesson 3 Practice Hands-On

# Directions

For your Lesson 3 Practice Hands-On, you will be working with your new knowledge on NoSQL. This Hands-On will not be graded, but we encourage you to complete it. The best way to become great at working with databases is to practice! Once you have submitted your project, you will be able to access the solution on the next page.

Requirements
This Hands-On is structured into two parts, and each part may ask you to run multiple queries. After each query, please take a screenshot and add it to a text document (or an equivalent) and name this file NoSQL-HandsOn3. This way, you will be able to submit your answers to each part all at once. You will continue working with the inventory collection in Atlas that you created during the last lessons. Good luck!

Part 1
Within your inventory collection, run queries to accomplish the following:

Update the item of journal to have a height of 16.
Update all items with a status of D to have a quantity of 50.
Update the item paper to include a field rating that has the value of 4 stars and change its status to A.
Update all items to change the h and w fields to be height and width.
Update the item spiral notebook so that the height and width is incremented by 2.
Update the items paper and day planner to multiply the height by 3.
Part 2
For the second part, you will be working through a word problem and you will need a bit more information. Please run the following query to add documents into your inventory collection then complete the below requirements:

db.inventory.insertMany([
  {
    item: 'sticky note pads',
    size: { height: 8.9, width: 9, uom: 'cm' },
    status: 'B',
    quantity: 5
  },
  {
    item: 'pens',
    size: { height: 12, width: 1.3, uom: 'cm' },
    status: 'A',
    quantity: 4
  },
  {
    item: 'pencils',
    size: { height: 13, width: 1.4, uom: 'cm' },
    status: 'D',
    quantity: 10
  },
  {
    item: 'clipboard',
    size: { height: 13, width: 7, uom: 'in' },
    status: 'B',
    quantity: 2
  },
  {
    item: 'printer ink',
    size: { height: 2, width: 3, uom: 'in' },
    status: 'C',
    quantity: 2
  }
]);
The company you are working for wants to update their inventory database. Currently, there are ten pieces of inventory in the database. They want to give each product a rating of 4 stars to start, as well as a field that shows if it has been rated yet using a boolean. They would like this to be reflected in the database as rating with two fields: numberOfStars, and hasBeenRated. Also, they want to double the quantity of every product since the company is rapidly growing. Lastly, they would like you to find all products that are sized using centimeters and give them a status of "B".
