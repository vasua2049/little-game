# little-game
#it is tle little game to work out with functions. this is one of the task  in the book of Zed Shaw that i read

from sys import exit

def white_rose():
    print('u are in the dark room.')
    print('what color?red or purple?')

    choice = input("> ")
    if choice == "red":
        print("hello it is our new world")
        exit(0)
    elif choice == "purple":
        apolap()
    else:
        good("stupid white man.")

def game_of_trhones():
    print('There is the Iron Throne.')
    print('Daynerys Targarien sits on it.')
    print('She wants kill u.')
    print('ur action? fight or talk?')
    she_moved = False
    
    while True:
        choice = input("> ")

        if choice == 'fight':
            good('Her dragon burns u.')
        elif choice == 'talk' and not she_moved:
            print('she likes u.')
            print('u can leave or kiss she.')
            she_moved = True
        elif choice == 'leave' and she_moved:
            white_rose()
        elif choice == 'kiss' or 'kiss she' and she_moved:
            good("She loves u!!!!")
        else:
            print('choice!!!')

def legion():
    print("u are see the David Legion")
    print("He looks u")
    print("leave or joke")

    choice = input("> ")

    if "leave" in choice:
        start()
    elif "talk" in choice:
        print("he answer u: do u have time to die?yes or no.")
        while True:
            x = input("> ")
            if "yes" in x:
                exit(0)
            elif "no" in x:
                game_of_trhones()
            else:
                print("CHOICE!!!")
    else:
        apolap()

def apolap():
    print("all is bad.")
    print("u can dead or fight with robots")
    choice = input("> ")
    if choice == "dead":
        white_rose()
    elif choice == "fight" or "fight with robots":
        good("u are president of all countries.")

def good(hey):
    print(hey,"fantastic!")
    exit(0)

def start():
    print("u are in the dark room.")
    print("there is two doors- left and right")
    print("ur action?")
    choice = input("> ")

    if "left" in choice:
        legion()
    elif "right" in choice:
        game_of_trhones()
    else:
        print("u dead")
    

start()
