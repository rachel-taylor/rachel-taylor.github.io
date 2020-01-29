---
layout: post
title:      "The CLI Project"
date:       2019-10-24 00:50:24 -0400
permalink:  im_no_quitter_am_i_the_cli_project
---


The first project from FlatIron seemed daunting, like most new things it came with it's own challenges and rewards. You are tasked with scraping the information from a website, or using an API to pull the data.

Going into this project you want to stop and make a plan:
1. What are you interested in? (This will make the project easier if it's something you like)
2. Pick a website that isn't dependent on information you haven't learned yet (make sure your website isn't in javascript, etc)
**OR**
Pick an API that interests you
3. Know what you want going in, use pseudocode to make it happen

The hardest part of this project for me was figuring out where to start. After spending hours discussing with my study group, I decided to choose the Pokemon API. 

Beginning the code we use ***Initialize***. Intialize is part of the object-creation process in Ruby and it allows you to set the initial values for an object. 

```
 def initialize(num)
    poke = open("https://pokeapi.co/api/v2/pokemon/#{num}/").read
    @json = JSON.parse(poke)
    @@all.push(self) 
  end 
```

The initial values of this project, is the number of the Pokemon. This allows for the number to be assigned to the Pokemon after the instance creation. Once the number is given we are able to obtain the name of the pokemon. 

```
def get_name
    @json["name"]
  end 
```

Once we've obtained the name of the Pokemon any of the information in the API is now available to us. We are able to obtain the Pokemon's name, and any additional information the API has available for us to choose from.

```
def get_abilities
    @json["abilities"].map do |ability|
      ability["ability"]["name"]
    end 
  end 
```
In the beginning I am choosing to just obtain the abilties of each Pokemon available in the PokeDex. 

Frustration. Confusion. Glee. Take a deep breath, you've got this. You've made it through the first project. 






