import requests
import random
import json

def pick_a_pokemon():
  user_input = input("What is your favorite pokemon?")
  if user_input.lower() == "ditto":
    print("Ditto is my favorite too!")
  else:
    pass
  
pokemon_data = requests.get("https://pokeapi.co/api/v2/pokemon")
  
if pokemon_data.status_code != 200:
    print("Error")
else:
    pass
  
total_pokemon = pokemon_data.json()
random_pokemon = random.randint(1, total_pokemon['count'])
  
pokemon_url = (f"https://pokeapi.co/api/v2/pokemon/{random_pokemon}/")
pokemon = requests.get(pokemon_url)

if pokemon.status_code != 200:
  print("Error")
else:
 pokemon_data = pokemon.json()#Prebacujemo u dictionary#
 pokemon_name = pokemon_data["name"]
 pokemon_id = pokemon_data["id"]
 pokemon_height = pokemon_data["height"]


print(f"Random Pokemon:{pokemon_name}, ID:{pokemon_id}, Height:{pokemon_height}")

pick_a_pokemon()
  
  
  
  
  
  
