# social-media-clone2
def copy_right(nickname):
    while True:
        try:
            input_copy_right = input("want to go back in the previous page? (yes or no):").lower()
            print("Copyright Disclaimer under Section 107 of the copyright act 1976, "
                  "allowance is made for fair use for purposes such as criticism, comment, "
                  "news reporting, scholarship, and research. Fair use is a use permitted by copyright"
                  " statute that might otherwise be infringing. Non-profit, educational or personal use "
                  "tips the balance in favour of fair use. © ℗®™")
            if input_copy_right == "yes":
                info(nickname)
            elif input_copy_right == "no":
                copy_right(nickname)
            else:
                print("wrong credentials,please try again...")
        except ValueError as e:
            print(f"please use the appropriate word/s for this function: {e} ")
def facemash_community(nickname):
    while True:
        try:
            input_facemash_comm = input("want to go back in the previous page? (yes or no):").lower()
            print("Facemash is a website that was created by Mark Zuckerberg during his time at Harvard "
                  "University. He created the website in one evening, whilst drunk, after his girlfriend Erica "
                  "Albright broke up with him but after some insults he took it down The website used pictures of"
                  " female Harvard University students which he stole from the student directories via hacking. "
                  "The website compares the female students against each other using coding, written by Mark and a "
                  "formal provided by subarna When the site was finished Mark sent out a link to a few people who"
                  " sent it out to other, resulting in hundreds of visitors. The website gained so many visitors "
                  "during its short lifespan that it crashed the computer system.")

            if input_facemash_comm == "yes":
                info(nickname)
            elif input_facemash_comm == "no":
                facemash_community(nickname)
            else:
                print("wrong credentials,please try again...")
        except ValueError as e:
            print(f"please use the appropriate word/s for this function: {e} ")

def learn_how_data(nickname):
    while True:
        try:
            input_learn_data = input("want to go back in the previous page? (yes or no): ").lower()
            print("Websites collect data about users to provide them with targeted advertising. A common practice "
                  "is retargeting. This is when websites track which sites you have visited and then show you adverts "
                  "based on this data. It's why you often see adverts for products you have recently viewed while browsing"
                  "the web.")
            if input_learn_data == "yes":
                info(nickname)
            elif input_learn_data == "no":
                learn_how_data(nickname)
            else:
                print("wrong credentials,please try again...")
        except ValueError as e:
            print(f"please use the appropriate word/s for this function: {e} ")
def cookies_privacy(nickname):
    while True:
        try:
            input_cookies = input("want to go back in the previous page? (yes or no):").lower()
            print("Are cookies a risk to your privacy? "
                  "HTTP cookies are essential to the modern Internet but a vulnerability to your privacy. "
                  "As a necessary part of web browsing, HTTP cookies help web developers give you more personal,"
                  " convenient website visits. Cookies let websites remember you, your website logins, shopping carts "
                  "and more.")
            if input_cookies == "yes":
                info(nickname)
            elif input_cookies =="no":
                cookies_privacy(nickname)
            else:
                print("wrong credentials,please try again...")
        except ValueError as e:
            print(f"please use the appropriate word/s for this function: {e} ")
def account_recovery(nickname):
    while True:
        try:
            input_acc_recovery = input("want to go back in the previous page? (yes or no):").lower()
            print("Set up a recovery phone number or email address "
                  "To make sure you can get back into your Google Account if you ever can’t sign in, add recovery"
                  " information.")

            print("How recovery info helps you")
            print("A recovery phone number or email address helps you reset your password if:")

            print("-You forget your password")
            print("-Someone else is using your account")
            print("-You’re locked out of your account for another reason")
            print("Tip: If you change your recovery phone or email, Google may still offer to send verification"
                  " codes to your previous recovery phone number or email address for 7 days. If someone starts to"
                  " use your account without your permission, this allows you to quickly secure your settings.")

            if input_acc_recovery == "yes":
                info(nickname)
            elif input_acc_recovery =="no":
                account_recovery(nickname)
            else:
                print("wrong credentials,please try again...")
        except ValueError as e:
            print(f"please use the appropriate word/s for this function: {e} ")





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
    input_nickname1 = input_nickname_change
    nickname = input_nickname1
    print(f"successfully change the nickname {nickname} to {input_nickname1}")
    print("wish to go back in main page? (yes or no)?")
    while True:
        try:
            change_nickname_func = input("Enter here: ").lower()
            if change_nickname_func == "yes":
                option_profile(nickname)
                return nickname
            else:
                print("wrong credentials, please use (yes or no) only ...")
        except ValueError as e:
            print(f"wrong credentials, please use (yes or no) only ...({e})")


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
                break
            elif profile_input == 3:
                option_profile(nickname)
                break
            else:
                print("wrong credentials, please try again...")
        except ValueError as e:
            print(f"wrong credentials, please try again: {e}")


def bio(nickname):
    print(f"welcome {nickname} to your bio")
    input_bio = input("whats your bio for today?: ")
    print(input_bio)

def info(nickname):
    print(f"welcome {nickname} to info set-up")
    print("===================================================")
    print("||need help?                                     ||")
    print("||1.) copyright system?                          ||")
    print("||2.) facemash community info?                   ||")
    print("||3.) learn how we use your data?                ||")
    print("||4.) cookies privacy?                           ||")
    print("||5.) Account recovery?                          ||")
    print("===================================================")
    while True:
        try:
            input_info = int(input("Enter the number here: "))

            if input_info == 1:
                copy_right(nickname)
            elif input_info == 2:
                facemash_community(nickname)
            elif input_info == 3:
                learn_how_data(nickname)
            elif input_info == 4:
                cookies_privacy(nickname)
            elif input_info == 5:
                account_recovery(nickname)
            else:
                print("wrong credentials, please try again...")
        except ValueError:
            print("please use the appropriate numbers in the column...")
        #functions of this info tmr ASAP

def settings(nickname):
    print(f"welcome {nickname} to settings")



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

