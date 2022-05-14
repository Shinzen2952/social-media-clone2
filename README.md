# social-media-clone2
def new_welcome_page(nickname):
    print("========================= < FACEMASH > ============================")
    print(f" hello!, {nickname}, hopefully you would enjoy staying with us again!")
    print("====================================================================")
    print("||A.)Profile                                                      ||")
    print("||B.)Bio                                                          ||")
    print("||C.)Info                                                         ||")
    print("||D.)Settings                                                     ||")
    print("====================================================================")
    while True:
        try:
            functionality = input("Enter the letter of the page you want to enter: (A,B,C or D): ").upper()
            if functionality == "A":
                option_profile(input_nickname)
                break
            elif functionality == "B":
                bio(input_nickname)
                break
            elif functionality == "C":
                info(input_nickname)
                break
            elif functionality == "D":
                settings(input_nickname)
                break
            else:
                print("wrong credentials, please try again...")
        except ValueError:
            print("please use the appropriate functions available...")


def change_nickname(nickname):
    input_nickname_change = input("Enter the exchange name for the current used: ").lower()
    input_nickname = input_nickname_change
    print(f"successfully change the nickname {nickname} to {input_nickname}")
    print("wish to go back in main page? (yes or no)?")
    while True:
        try:
            change_nickname_func = input("Enter here: ").lower()
            if change_nickname_func == "yes":
                option_profile(nickname)
                return input_nickname
            else:
                print("wrong credentials, please use (yes or no) only ...")
        except ValueError as e:
            print("wrong credentials, please use (yes or no) only ...")


def option_profile(nickname):
    print(f"welcome {nickname} to profile")
    print("=========== < Profile > ==============")
    nickname = nickname
    print("1.) change nickname?")
    print("go back?  ")
    print("2.) yes ")
    print("3.) no ")
    while True:
        try:
            profile_input = int(input("Enter the number of function: "))

            if profile_input == 1:
                change_nickname(nickname)
                break
            elif profile_input == 2:
                new_welcome_page(nickname)
            elif profile_input == 3:
                option_profile(nickname)
            else:
                print("wrong credentials, please try again...")
        except ValueError as e:
            print(f"wrong credentials, please try again: {e}")


def bio(nickname):
    print(f"welcome {nickname} to your bio")
def info(nickname):
    print(f"welcome {nickname} to info set-up")
def settings(nickname):
    print(f"welcome {nickname} to profile")



class Account:
    def __init__(self,email,nickname,password):
        self.email = input_email
        self.nickname = input_nickname
        self.password = input_password


    def profile(self):
        print(f"your email is: {self.email}")
        print(f"your nickname is: {self.nickname}")
        print(f"your password is encrypted as: {self.password} ")



    def welcome_page(self):
        print("========================= < FACEMASH > ============================" )
        print(f" hello!, {self.nickname}, hopefully you would enjoy staying with us again!")
        print("====================================================================")
        print("||A.)Profile                                                      ||")
        print("||B.)Bio                                                          ||")
        print("||C.)Info                                                         ||")
        print("||D.)Settings                                                     ||")
        print("====================================================================")
        #adding input for the function TMR ASAP(2)
        while True:
            try:
                functionality = input("Enter the letter of the page you want to enter: (A,B,C or D): ").upper()
                if functionality == "A":
                    option_profile(input_nickname)
                    break
                elif functionality == "B":
                    bio(input_nickname)
                    break
                elif functionality == "C":
                    info(input_nickname)
                    break
                elif functionality == "D":
                    settings(input_nickname)
                    break
                else:
                    print("wrong credentials, please try again...")
            except ValueError:
                print("please use the appropriate functions available...")
while True:
    try:
        input_email = input("Enter your email here: ").lower()
        input_nickname = input("Enter your nickname here: ").lower()
        #encryption
        input_password = input("enter your password : ").lower()
        if input_email == 'shikisenri@gmail.com':
            if input_password == "makui":
                password_value = input_password.replace("a", "9010")
                password_value = password_value.replace("m", "21")
                input_password = password_value[::-1]
                p = Account(input_email,input_nickname,input_password)
                p.profile()
                p.welcome_page()
                break
            else:
                print("password credentials is incorrect, please try again...")
        else:
            print("email credentials is incorrect, please try again...")

    except ValueError as e:
        print(f"wrong credentials, please try again:{e}")

