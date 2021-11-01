# E-commmerce

## Table of Contents

- [About](#about)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Code Sample](#code-sample)
- [Acknowledgement](#acknowledgement)
- [Contributing](#contributing)
- [License](#license)

## About <a name = "about"></a>

E-commerce is a sequalized and Mysql2 based program that is used to  create a database of your companies current inventory 

## Getting Started <a name = "getting-started"></a>

* [Git Hub Pull](https://github.com/nicoguarino/e-commerce-.git)
* [Walkthrough Video](https://watch.screencastify.com/v/cJGWOMP0Eu58T9QEdHDn)

## Installation <a name = "installation"></a>

1. Download Node to be able to run application
2. Download Sequelize by npm i sequelize
3. Download MySQL2 by npm i MySQL2
4. Download Dotenv by npm i dotenv
5. In you Mysql account, source the database
6. In your command line seed your database by writing "npm run seed" 
6. To run application type in the command line "npm start"

## Code Sample <a name = "code-sample"></a>

![Sample Code](https://github.com/nicoguarino/e-commerce-/blob/main/images/sample_code.PNG?raw=true "Sample Code")

### Sample Code
```JavaScript Sample
router.get('/', (req, res) => {
  // find all categories
  // be sure to include its associated Products
  Category.findAll({
    attributes: [
      'id',
      'category_name'
    ],
    include: {
      model: Product,
      attributes: ['id', 'product_name', 'price', 'stock', 'category_id']
    }
  })
    .then(dbCategoryData => res.json(dbCategoryData))
    .catch(err => {
      console.log(err);
      res.status(500).json(err);
    });
});
```

## Authors and acknowledgement <a name = "acknowledgement"></a>

Nico (Filipu) Guarino
E-commerce back end team


## Contributing <a name = "contributing"></a>

E-commerce is open for contrubiting, however check with the creator first before making any permanent changes. The creator is opening to creative ideas and tweeking of design, but it must be approved first.

## License <a name = "license">

(c) 2021 E-commerce