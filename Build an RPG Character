full_dot = '●'
empty_dot = '○'
def create_character(character_name, strength, intelligence, charisma):
    if not isinstance(character_name, str):
        return 'The character name should be a string' 
    if character_name == '':
        return 'The character should have a name'
    if ' ' in character_name:
        return 'The character name should not contain spaces'
    if len(character_name) > 10:
        return 'The character name is too long'

    
    stats = [strength,intelligence,charisma]
    for stat in stats:
        if not isinstance(stat, int):
            return 'All stats should be integers'

    for stat in stats:
        if stat < 1:
            return 'All stats should be no less than 1'
    for stat in stats:
        if stat > 4:
            return 'All stats should be no more than 4'

    if sum(stats) != 7:
        return 'The character should start with 7 points'

    def render_stat(value):
        return full_dot * value + empty_dot * (10 - value)
    return (
        f"{character_name}\n"
        f"STR {render_stat(strength)}\n"
        f"INT {render_stat(intelligence)}\n"
        f"CHA {render_stat(charisma)}"
    )
