# graphqlrestaurant
In this assignment I created a Graphql localhost that talked with my visual studio code to pull information. Below is what I put in the graphql server. I also inserted an image to show what how the main screen appears, to the right it is showing the ability to pull an individual restaurant. 

mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}
query getrestaurant($iid: Int = 1) {
	restaurant(id: $iid) {
    name
    description
  }
}
<img width="1248" alt="Screen Shot 2022-03-23 at 10 59 55 AM" src="https://user-images.githubusercontent.com/89057459/159754839-3484f57e-c3fe-478b-9c2d-1554d2345c5a.png">
