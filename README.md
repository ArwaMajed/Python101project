# Python101project
###########
# NumberBook for 2nd Function
###########
NumberBook_name = {
    'amal': '1111111111',
    'mohammed': '2222222222',
    'khadijah': '3333333333',
    'abdullah': '4444444444',
    'rawan': '5555555555',
    'faisal': '6666666666',
    'layla': '7777777777'

}
###########
# NumberBook for 1st Function
###########
NumberBook_num = {
    '1111111111': 'Amal',
    '2222222222': 'Mohammed',
    '3333333333': 'Khadijah',
    '4444444444': 'Abdullah',
    '5555555555': 'Rawan',
    '6666666666': 'Faisal',
    '7777777777': 'Layla'
}
###########
# Functions
###########

# Function: searching by number
###########
def search_bynumber():
    num = input("Enter the phone number: ")
    if num.isdigit() and len(num) == 10:
        num = str(num)
        if num in NumberBook_num:
            print(NumberBook_num[num])
        else:
            print("Sorry, the number is not found")
    else:
        print("This is invalid number")
###########
# Function: searching by name
###########
def search_byname():
    name = str(input("Enter the name: "))
    name = name.lower()
    if name in NumberBook_name:
        print(NumberBook_name[name])
    else:
        print("The name is not found")
###########
# Function: add new number
###########
def add_num():
    name = str(input("Enter the name: "))
    name = name.lower()
    if name in NumberBook_name:
        print("This name exists")
    else:
        num = str(input("Enter the number: "))
        if num in NumberBook_num:
            print("This number exists")
        elif num.isalpha() or len(num) != 10:
            print("This is invalid number")
        else:
            NumberBook_num[num] = name
            NumberBook_name[name] = num
            print("Added successfully")

###########
# The menu
###########


menu = ''
while True:
    menu = input("Welcome to the phone book\n"
                 "Enter 1: to search by number\n"
                 "Enter 2: to search by name\n"
                 "Enter 3: to add new number\n"
                 "Enter 4: to see all users\n"
                 "Enter 5: to exit\n")
    if menu == '1':
        search_bynumber()
    elif menu == '2':
        search_byname()
    elif menu == '3':
        add_num()
    elif menu == '4':
        print(NumberBook_name)
    elif menu == '5':
        break
    else:
        print("This is invalid number")

