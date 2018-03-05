
 #Demo:


  # Git Tutorial
  We are learning the basics of Git and Github

  ## What is Git ?
  Git is a version control tool which can help to track changes in a repository.

  ###What Technologies needed:
  *Git
  *Github

  # Author:
  Mohamed
  # License:
  All rights are reserved

  # Javascript

  ```javascript

  const myInventoryList = {
  inventoryList: [
    {
      id: '001',
      name: 'Mango',
      quantity: 100,
      price: 5,
      date: new Date(),
      completed: false
    },
    {
      id: '002',
      name: 'Milk',
      quantity: 150,
      price: 3,
      date: new Date(),
      completed: false
    },
    {
      id: '003',
      name: 'Tomato',
      quantity: 200,
      price: 4,
      date: new Date(),
      completed: false
    }
  ],
  displayInventory() {
    let inventoryLength = this.inventoryList.length;
    console.log(inventoryLength);
    if (inventoryLength === 0) {
      console.log('The array is empty. Add item into the array');
      console.log('To add item use myInventoryList.addInventory() methods');
    }

    this.inventoryList.forEach((item, i) => {
      if (item.completed === true) {
        console.log('(*)', i + 1, item.name, item.quantity, item.price);
      } else {
        console.log('()', i + 1, item.name, item.quantity, item.price);
      }
    });
  },
  addInventory(name, quantity, price) {
    this.inventoryList.push({
      id: 'id',
      name: name,
      quantity: quantity,
      price: price,
      date: new Date()
    });

    this.displayInventory();
  },
  editInventory(position, name, quantity, price) {
    this.inventoryList[position].name = name;
    this.inventoryList[position].quantity = quantity;
    this.inventoryList[position].price = price;
    this.displayInventory();
  },
  deleteInventory(position) {
    this.inventoryList.splice(position, 1);
    this.displayInventory();
  },
  toggleInventory(position) {
    this.inventoryList[position].completed = !this.inventoryList[position]
      .completed;
    this.displayInventory();
  },
  deleteAll() {
    this.inventoryList.splice(0);
    this.displayInventory();
  },
  toggleAll() {
    let totalCompleted = 0;
    let inventoryLength = this.inventoryList.length;
    this.inventoryList.forEach(item => {
      if (item.completed === true) {
        totalCompleted++;
      }
    });

    if (totalCompleted === inventoryLength) {
      for (let i = 0; i < inventoryLength; i++) {
        this.inventoryList[i].completed = false;
      }
    } else {
      for (let i = 0; i < inventoryLength; i++) {
        this.inventoryList[i].completed = true;
      }
    }

    this.displayInventory();
  }
};

myInventoryList.displayInventory();

```
