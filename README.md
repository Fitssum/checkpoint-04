# Checkpoint 04

## Instructions

1. Fork this repo
2. Clone your fork
3. Fill in your answers by writing in the appropriate area or, for multiple-choice questions, placing an 'x' in the square brackets
4. Add/Commit/Push your changes to Github
5. Open a pull request

For questions 1-4, you must test your code before filling in an answer. You can do this by creating and running your own `app.rb` file.

> Only place your answer between the backticks provided for you throughout the checkpoint.

## Ruby Basics & Enumerables

### Question 1

Define a method called `offer_rose`, which should take one argument named `person` (String).

When called the method should print "Would you take this rose, `person`, in exchange for giving an old beggar woman shelter from the bitter cold?" to the Terminal.

Demonstrate calling the method, passing in "young prince" as the argument.

```rb
# Your code goes here...
@person = person
def offer_rose(person)
  puts "Would you take this rose, #{person}, in exchange for giving an old beggar woman shelter from the bitter cold?"
end
offer_rose(young prince)

```

### Question 2

Assume the following hash...

```ruby
town = {
  residents: ["Maurice", "Belle", "Gaston"],
  castle: {
    num_rooms: 47,
    residents: "Robby Benson",
    guests: []
  }
}
```

Using Ruby...
- Remove "Belle" from `residents`

- Add "Belle" to the `guests` array
town

```rb
# Your code goes here...
town[:residents].delete("Belle")
town[:castle{:guest}].push("Belle")

```

### Question 3

Assume you have an array of strings representing friends' names...

```rb
friends = ["Chip Potts", "Cogsworth", "Lumière", "Mrs. Potts"]
```

Using `.each` and string interpolation, print the following text to the Terminal...

```
Belle is friends with Chip Potts
Belle is friends with Cogsworth
Belle is friends with Lumière
Belle is friends with Mrs. Potts
```

```rb
# Your code goes here...

get friends.each do |i|
puts "Belle is friends with #{i[:names]}"
end
```

## Ruby OOP

### Question 4

Create Ruby classes for `Animal` and `Lion`. Each `Animal` should have...
- A `name` (String) attribute
- A `greet` instance method
- The ability to "get" and "set" `name`

Create a new `Animal` instance with the name "Pumba".

Make the `Lion` inherit from the `Animal` class. The `Lion` class should have a `pack` class variable that holds references to each instance created.

Each lion should have...
- A `king` (Boolean) attribute
- If the instance's `name` is "Simba", set the `king` attribute to `true`

Create a new lion instance with the name "Simba".

```rb
# Your code goes here...
class Animal(name, greet)
  attr :name
  @@name = name
  @@greet = greet

  get animal do(name)
    if @@name == Simba
      king = true
    end
  end


  class Pack
  end
end
class Lion
  @king = king
  class Pack
  end
end
end
```

## SQL, Databases, and ActiveRecord

### Question 5

Describe what an ERD is and why we create them for applications. Also give an
example what the attributes and relationships might be for the following
entities (no need to draw an ERD)...
- Genie
- Lamp
- Person
- Pet

```
Your answer goes here...
ERD is an entitiy relationship diagram that can give us a visual representation of our data.
Genie
- id
Lamp
- type
- production
Person
- id
- profession
Pet
- animal category

```

### Question 6

Describe what a schema is and how we represent a one-to-many relationship in a
SQL database.

```
Your answer goes here...
Schema is a collection of database objects that can be associated with a particular database username.
```

### Question 7

Consider a class `Person` that inherits from `ActiveRecord::Base` and has the following schema...

```rb
class Person < ActiveRecord::Base
end
```

```sql
CREATE TABLE persons(
  id SERIAL PRIMARY KEY,
  name VARCHAR NOT NULL,
  age INT NOT NULL
);
```

Write Ruby code that will create an instance of a person...

```rb
# Your code goes here...
fitssum = Person.new(name:"Fitssum");
```

### Question 8

Assuming the `Person` class from the previous question, write Ruby code that will query for any person that is 15 years of age...

```rb
# Your code goes here...
select * from person where age > 15;
```

### Question 9

Write a route in Sinatra that will print "Hello world" in the web browser at the following URL: `http://localhost:4567/oh_hello`

```rb
# Your code goes here...
get '/' do
  return '<h1>Hello world!</h1>'
end
```
