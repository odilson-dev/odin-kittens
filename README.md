# Kittens API 🐱

Kitten application to set up Rails to render data instead of HTML from The Odin Project. 
[Link to lesson](https://www.theodinproject.com/lessons/ruby-on-rails-kittens-api#assignment-2)

## Table of Content

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)

## Features

- RESTful API: Able to request index and show actions of Kitten as json.
- Functional html interface that allows create, edit, and delete actions.

## Installation

clone repository
```
git clone git@github.com:odilsoncode/odin-kittens.git
```

install gems
```
bundle install
```

migrate data
```
rails db:migrate
```

## Usage

start server
```
rails s
```

open in browser
```
localhost:3000
```

### API interface
Before you continue, make sure you create a new kitten through the html page
```
require 'rest-client'
```

To get index json response
```
json_response = RestClient.get("http://localhost:3000/kittens", accept: :json)
puts json_response.body
```

To get show json response
```
show_json_response = RestClient.get("http://localhost:3000/kittens/1", accept: :json)
puts show_json_response.body
```