# LA-23

class AnimeCharacter:
  LA#23

  def __init__(self, name, ability):
        self.name = name
        self.ability = ability
   
    def introduce(self, func):
        def wrapper():
            print("Introducing..")
            func()
            print("This Character is Amazing!!")
        return wrapper

character = AnimeCharacter("Luffy", "stretch his limbs" )

@character.introduce
def character_intro():
    print(f"I am {character.name} and I can use {character.ability}.")

character_intro()
