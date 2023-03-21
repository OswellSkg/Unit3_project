# Unit 3: KanjiApp

![sabrina-ellul-PveJaE410_w-unsplash](https://user-images.githubusercontent.com/112055140/224188453-1a1261b9-e431-4897-afab-3d2d6ee956d4.jpg)
Photo by <a href="https://unsplash.com/@sabrinaellul?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Sabrina Ellul</a> on <a href="https://unsplash.com/photos/PveJaE410_w?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
  

# Criteria A: Planning

## Problem definition
My client, Maria Camargo is a student in UWC ISAK Japan. Currently in Grade 11, she is facing challenges with one of her subjects, Japanese ab initio, specifically the acquisition of the Japanese Kanjis. In every class, she is introduced to new Kanjis by the teacher, and is expected to study it on her own outside of class as her homework. In the next class, her acquisition of these Kanjis will be tested on a quiz. However, Maria is having a hard time catching up wtih these Kanjis, 1) because these kanjis are found in a worksheet on google classroom and she feels as though it is very difficult to access it, 2) because these kanjis are scattered amongst a number of different worksheets and learning materials, Maria is not able to properly have a grasp what Kanji she needs to study for each tests, and lastly, 3) Not only because of the flaws and disadvantages of the class materials, but also because Maria herself is taking Computer Science HL, Physics SL, and even Math AA HL, she really does not have the time to be looking around google classroom everyday after school to find these Kanjis. For the given reasons, the client strongly expressed that one place that she could store all the Kanjis that she has learnt would be greatly appreciated.

## Success Criteria
1. The application will have a login and registration system with security methods to enhance privacy, and verification methods for user registration to ensure the applicability of the app.
2. The login and registration system will implement security methods to protect privacy, and also verification methods for user registration.
3. The application will allow the user to input all attributes (Kanji, Hiragana, Katakana, and Meaning) and will be stored into an SQLite database through the interface.
4. The application will allow the user to view all values stored in the database, and also to delete them when necessary.
5. The application will have a screen where the user can do the action above, of inputting all attributes to be stored into an SQLite database.
6. The application will have a screen where all values stored in the database will be compiled into a Table with a button of a deletion function, and is easily accessible for the users.
7. The application will have a screen where all the SQLite database-stored Kanjis are put into a list, where the user can easily access for Kanji acquisition and revision. 

## Design Statement 
The Kanji storage and retrieval system is a software application designed to facilitate efficient, accessible, and effective Kanji learning management for students such as Maria Camargo. It utilizes the Python programming language, Kivymd for the user interface, and SQLite for data storage.

The system's primary objective is to provide a centralized location for students to store, retrieve, and revise all their Kanji data. By doing so, the system will enable students to manage their learning experience more effectively, ensuring enhanced learning outcomes for all Kanji-learning students, regardless of their educational backgrounds.

Additionally, the interface will enable users to input Kanji data attributes such as Kanji, Hiragana, Katakana, and Meaning into the system's SQLite database. Users can also view and delete all values stored in the database when necessary.

Our Kanji storage and retrieval system provides a user-friendly interface with a screen for inputting Kanji data, a screen for viewing and deleting all stored values, and a screen for accessing a list of all stored Kanjis. Through this comprehensive approach, our system streamlines and simplifies the Kanji learning experience, making it easier for students to focus on mastering this challenging subject matter.

## Rationale for Proposed Solution
The primary focus of the application is to provide a centralized platform for Kanji learners such as my client, with the use of Python as the programming language, KivyMD to create the GUI (Graphic User Interface) and SQLite for database management system. By doing so, the application will solve the problem of inefficiency by providing a cautiously-tailored solution to help students manage their Kanji learning more effectively. 

In the light of the client's Kanji acquisition issues, I will use a GUI rather than a text-based processor. This is to fulfill the client's satisfaction by allowing the application to become further user-friendly with a visually appealing interface and an organized and easy-to-understand application layout, enhancing the user's experience with the application and furthering their Kanji learnings. Furthermore, as the client's learning is heavily based on visual recognitions of the Kanji, a GUI allows me to maximize the potential of the application by graphical enhancement for the client. 

The selection of the Python programming language for developing the proposed application was based on its widespread use and popularity in the tech industry for its simplicity, readability, and flexibility. According to the latest TIOBE Programming Community Index, Python ranks the most popular programming language as of March 2023 [4]. Python's extensive library support granted by its substantial community of developers, makes it easier to access pre-built code modules with basic syntax as well as its simple syntax rule[3], facilitating faster development of the desired application. Furthermore, from a developer's perspective, the language is highly applicable for the development of applications as it puts heavy emphasis on the adoption of TDD (Test Driven Development)[3], allowing developers to ensure the quality of the application through a series of test drives and assess the program code accordingly. Ultimately, Python is most suitable for the development of this application as it allows swift development(with Python code being shorter than other languages such as Java by 3-5 times, and C++ by 5-10 times[5]), and its extensive library support that eases the development of complex software applications.

For the application interface, the KivyMD library was chosen due to its ease of use and adaptability. Kivy is a free, open-source, multi-platform application development framework that runs on various platforms like Android, iOS, Windows, Linux[7] and it is one of, if not, the only GUI framework that is written in pure Python [6]. It provides pre-built user-interface elements and styles that can be effortlessly customized and integrated into Kivy-based applications [7], which saves time and effort required to develop the interface from scratch. Although there are alternatives to KivyMD, such as Flutter that have a larger community for support and are better at developing native applications, KivyMD was selected due to its easy learning curve, flexibility, and compatibility with the pure state of Python language[7], as well as the proposed application's requirements.

SQLite was chosen as the database management system for this proposed solution due to its efficiency, reliability, and extensive combatibility. SQLite is a free open-source database[8] that does not require a separate server process and licensing, and allows to implement several databases into a single file[9], making it easy to facilitate work on multiple databases on the same session simultaneously, thus enhancing flexibility[8]. SQLite posess various lightweight features such as its capability of storing all kinds of information safely and quickly, without requiring lengthy procedural routines, as compared to other databases like Oracle[10]. SQLite also provides continuous transaction updates and atomic behaviors, so a program crash or even a power outage won’t leave you with a corrupted database[9]. Its cross-platform compatibility further enhances the client's ability to expand the program to other platforms[8]. SQLite is a cost-friendly, reliable, and easy-to-use database and the best option for the proposed application's database management system.


# Criteria B: Design

## System Diagram
![SystemDiagram](https://user-images.githubusercontent.com/112055140/224467199-91b2e028-3c59-4e94-975f-ad9bdb0c72af.jpg)

<i>Fig. 1</i> This is the system diagram for the proposed solution.

This system diagram shown above is for the application proposed as the solution. It visually represents the system as well as its components. In general, it serves to clarify the relationships between the components, and making it easier to understand overall how it works. The application will use KanjiApp.py from Python and KanjiApp.kv from KivyMD for the GUI and functions, while we use kanji_app.db from SQLite to store any user inputs. This will all be able to be executed through the PyCharm application, and will be displayed using a screen. 

## Wireframe Diagram 
![Wireframe Diagram](https://user-images.githubusercontent.com/112055140/224467201-3422a561-06cd-4b80-951b-5548b7796ad7.jpg)

<i>Fig. 2</i> This is the wireframe for the application. 

The wireframe diagram above is a visual representation of the application GUI structure. It clarifies the functions of each buttons within the GUI, ignoring the python functions. It serves to provide a broad overview of the application as well as a thorough and in-depth understanding of the structure of its GUI. The arrows extending from buttons will represent what screen the button will take you to. For instance, the REGISTRATION button in the LoginScreen will take you to the RegistrationScreen whereas the LOG IN button if the same LoginScreen will take you to the HomeScreen(when correct username and password are entered). 

## ER Diagram
![ERDiagram](https://user-images.githubusercontent.com/112055140/224467205-32d45dc4-d483-4cfe-8375-d80b91c071e4.jpg)

<i>Fig. 3</i> This is the ER Diagram showing the two tables: users, kanji_database.

The users table of the kanji_app.db database of the application will record the registered users for the application. It will record the id of the user in an integer format, the username as a string format, the email as a string format, and finally the password as a string format. However, the password is hashed before recorded into the users table for security reasons. Therefore, neither the developers or data breachers will have access to the original password of the user. The kanji_database table of the same database includes id in an integer format, and user_id, kanji, hiragana, katakana, and meaning as string format. 

## UML Diagram
![UMLDiagram](https://user-images.githubusercontent.com/112055140/224467215-48ffd13d-b67a-4005-a974-73ca24678e59.png)

<i>Fig. 4</i> This is the UML Diagram showing the classes and methods.

The UML diagram shown above provides informations regarding the classes and methods used throughout the development of the app. Parenting classes are MDApp, MDScreen, MDExpansionPanelThreeLine, and finally the MDBoxLayout. Each classes contains methods in each screen necessary for the application to function. Finally, the database_handler contains methods required for the application to connect and modify the kanji_app.db SQLite database. 

## Flow Diagrams
![FlowDiagram1](https://user-images.githubusercontent.com/112055140/224905116-a3f14db6-fb27-43f1-b48b-661413f1b01f.jpg)

<i>Fig. 5</i> This is the flow diagram that details the process of how the try_add method from AddKanjiScreen works. 

This method is used to append the kanji, hiragana, katakana, and meaning inputs from the user into the kanji_database table of the kanji_app.db database. The method first converts the input to local variables, as well as taking the user_id of the user logged in, to make the data exclusive to that specific user. Next, it opens access to the database with the database_handler, and append the local variables with a specially generated query named “add_kanji.” Finally, it runs the query, closes the database, notifies toe user that the Kanji has been added, and empties all the inputs for the next input. And that is the end of the method. 

![FlowDiagram2](https://user-images.githubusercontent.com/112055140/224905145-2c9d069f-a942-49c0-b83a-556d1cba683d.jpg)

<i>Fig. 6</i> This is the flow diagram that details the process of how the update method from DeleteKanjiScreen works. 

This method is used to update a table that lists all the datas from kanji_database table in kanji_app,db database. The method will first take the user_id of the user logged in. It will then open the kanji_app.db database, and SELECT all datas that are specific to the user_id of the user that is logged in. Then, it will append all the results into a local variable “results” and close the database. Following that, it will create a list named “data,” and for every data in the results variable, it will take the kanji, hiragana, katakana variables and convert them into a Japanese font, and add it to a new list variable created earlier, “data.” Then, it will update the table accordingly. This way, all of the datas shown on the table is 1) user exclusive, and 2) converted to a Japanese font, hence preventing any display errors.

![FlowDiagram3](https://user-images.githubusercontent.com/112055140/224905175-9d04bec9-37fe-430b-a9b2-dca62bc911db.jpg)

<i>Fig. 7</i> This is the flow diagram that details the process of how the save method from the DeleteKanjiScreen works.

This method is used to delete any data from the kanji_database table from the kanji_app.db database. The way it works is that, on a table shown on the screen, the user can click on the data that they want to delete. This will be recorded as checked_rows, and will be used later to select the datas to delete in the uniquely generated query. The method will then open the database, and go through a for look that for every data in checked_rows, it will repeat the process of identifying the ID of the selected data, and using that to identify what data to delete from the database in a query, and running the query. This will be repeated until there are no more datas left in the checked_rows, and then will finally move on to close the database. It will then update the table so that the change is reflected upon without the user having to run the whole program again.

## Test Plan

| Test No. | Type of Test                                                                                                                    | Date     | Procedure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Expected Outcome                                                                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1        | Functional: <br>Registration system                                                                                             | 09/03/23 | 1) Run the KanjiApp.py<br>2) Click the REGISTRATION button<br>on the bottom left<br>3) Create an account with all the<br>necessary inputs, but make some mistakes such as<br>putting in the email address in the wrong format.<br>4) Make sure that the screen provides an error.<br>5) Make sure the error is specified to the user.<br>6) Attempt to create an account with proper user<br>inputs.<br>7) Click the REGISTER button<br>8) Confirm that you returned to <br>the LOG IN screen<br>9) Check the users table of the<br>SQLite kanji_app.db database<br>10) Confirm that there is an account<br>with the specified username and email<br>address, and that the password is<br>hashed. | The account is<br>properly registered<br>with all inputs<br>of username, email<br>and password appended<br>into users table in<br>kanji_app.db database.                                  |
| 2        | Non-Functional:<br>Readability/Explicity<br>of the Login/Register<br>system as well as its<br>verification <br>methods/policies | 09/03/23 | 1) Run the KanjiApp.py<br>2) Provide the screen to the user and<br>give the instruction to 1. Create an account<br>and to 2. Login with the account.<br>3) Record the time it takes for the user <br>to finish the process, as well as any mistakes<br>the user makes along the process.<br>4) When done, confirm that the user has reached <br>the home screen with their new account.                                                                                                                                                                                                                                                                                                           | The user successfully <br>registers a user with<br>username, email, and<br>password inputs. These<br>datas are properly seen<br>in the users table of<br>the kanji_app.db <br>database.   |
| 3        | Functional: <br>Login System                                                                                                    | 09/03/23 | 1) Run the KanjiApp.py<br>2) With an already-existing account, attempt<br>log in with the specified credentials but with<br>few mistakes such as a typo<br>3) Confirm that the screen does not let the user<br>access the home screen<br>4) Confirm that the screen specifies the error <br>to the user<br>5) Attempt to login with the correct credentials<br>6) Confirm that the screen gives the user access<br>to the home screen.                                                                                                                                                                                                                                                            | Login is successful, and<br>all the datas that are<br>displayed through <br>DeleteKanjiScreen as well<br>as KanjiList screen are<br>exclusive to the user.                                |
| 4        | Non-Functional:<br>Can the user properly<br>add kanjis through<br>the AddKanjiScreen                                            | 09/03/23 | 1) Run the KanjiApp.py<br>2) Log into the app with an existing account, and<br>go to the AddKanjiScreen. <br>3) Provide the screen to the user and give the <br>instruction to: "use it."<br>4) Record the time taken for the user to figure <br>out how the program works and add a Kanji. <br>5) When done, confirm that they successfully added<br>the kanji through the kanji_database table of the<br>kanji_app.db.                                                                                                                                                                                                                                                                          | The user successfully <br>adds a kanji through the<br>AddKanjiScreen, and this<br>is confirmed through the <br>kanji_database table<br>of the kanji_app.db <br>database.                  |
| 5        | Functional<br>"Add Kanji" function                                                                                              | 09/03/23 | 1) Run the KanjiApp.py<br>2) Log into the app with an existing account, and<br>go to the AddKanjiScreen.<br>3) Fulfill all necessary inputs and click "Add <br>Kanji." button. <br>4) Go to kanji_database table of the kanji_app.db<br>and make sure that the inputs are added as datas. <br>5) Go back to the app, go to KanjiList screen, and<br>confirm if the kanjis are displayed there.                                                                                                                                                                                                                                                                                                    | The "Add Kanji" properly<br>functions and is successful<br>in the sense that all inputs<br>are properly appended into<br>the kanji_database table<br>of the kanji_app.db database.        |
| 6        | Non-Functional:<br>Can the user properly<br>delete kanjis through<br>the DeleteKanjiScreen                                      | 09/03/23 | 1) RUn the KanjiApp.py<br>2) Log into the app with an existing account, and <br>go to the DeleteKanjiScreen.<br>3) Provide the screen to the user and give the <br>instruction to: "use it."<br>4) Record the time taken for the user to figure<br>out how the program works and delete a Kanji. Also<br>take note of any mistakes the user makes. <br>5) When done, confirm that they successfully deleted<br>the kanji through the kanji_database table of the <br>kanji_app.db.                                                                                                                                                                                                                | The user successfully deletes<br>a set of data through the table<br>in the DeleteKanjiScreen. This<br>is confirmed through the <br>kanji_database table of the <br>kanji_app.db database. |


## Record of Tasks
https://docs.google.com/document/d/1xnl3_qt5ToP3yCtgorY-RFfB_ZXItlj07jwOs4aSo-8/edit?usp=sharing

# Criteria C: Development

## Existing Tools
Python
KivyMD
SQLite3
PyCharm
ChatGPT
Font Book
RGB
Re
Logging

## Techniques Used
1. For loops
2. Else statements
3. If statements
4. Variables
5. Database Connection
6. Classes
7. Functions
8. Object Oriented Programming (OOP): Classes, Inheritance 

## Development of User Interface Using KivyMD

### Screen Manager
```.kv
ScreenManager:
    LoginScreen:
        name: "LoginScreen"

    RegistrationScreen:
        name: "RegistrationScreen"

    HomeScreen:
        name: "HomeScreen"

    AddKanjiScreen:
        name:"AddKanjiScreen"

    DeleteKanjiScreen:
        name: "DeleteKanjiScreen"

    KanjiList:
        name: "KanjiList"
```
The client requires an application that allows them to record kanjis accordingly to their kanji learning experiences. The application will therefore consist of 6 screens of two Login and Registration, one Home Screen, and Three screens for Add, Kanji, and View functions. 
The KV code above brings together all 6 screens under one unbrella of a ScreenManager. Each screen can be given a nickname. 

### General Screen Graphical User Interface
```.kv
<LoginScreen>:
    size: 2000, 1000
    FitImage:
        source: "J6HCBQ4.gif"
    MDCard:
        size_hint: .7,.7
        pos_hint: {"center_x": 0.5, "center_y": 0.5}
        orientation: 'vertical'
        md_bg_color: 1, 1, 1, 0.5
```
In the kivy program above, the general layout and design is defined. In this example, the Login Screen has a size of 2000 x 1000 pixel, and has a background of an image named J6HCBQ4.gif. Within the screen, there is a Card the size of 70% x 70% of the entire screen, positioned vertically and horizontally centered. It's orientation is vertical, meaning whatever comes inside the card will be layed in order vertically. The color of the Card is white, with 0.5 transparency. This overall achieves a very professional finish of the design. This design is universal across the applications, and is applied to every single screen available witin the application. 

### MDBoxLayout
```.kv
MDBoxLayout:
    orientation: "vertical"
    size_hint:1,.25
```
In every screen, the MDBoxLayout plays a significant role in creating a cleanly designed and organized screen. The MDBoxLayout was used to distribute the portions of the screen in a decided porportion. For instance, in the example above, the BoxLayout takes up the whole horizontal space times 25% of the vertical space of its parent variable. This way, whatever comes inside the MDBoxLayout is limited within the 25% of the vertical space, hence achieving to organize the entire screen in this manner. Several of the MDBoxLayout is used to fill up all of the space that its parent specifies. 

### MDLabel
```.kv
MDLabel:
    text:""
```
In any MDBoxLayout, in order to ensure that the design is clean and organized, MDLabel was used to fillin unnecessary gaps. For instance, in the case if there are two MDTextField's(which I will introduce later) that is horizontally aligned, and we want to space it equally amongst the screen, we can put MDLabel before the first MDTextField, one in-between the two MDTextField's, and one after the second MDTextField. With this, The MDLabel will automatically take up as much space as it can in the specified parts, hence bringing the two MDTextFields horizontally together with balanced spacing, of three equal spaces. This MDLabel has been used all across the screen to ensure quality design.

### MDRaisedButton
```.kv
MDRaisedButton:
    text: "LOG IN"
    font_size: 20
    pos_hint: {"center_y":.5}
    on_press: root.try_login()
    text_color: "#FFFFFF"  # white text color
    md_bg_color: "#2B2D2F"  # use dark gray as background
    line_color: "#FFFFFF"  # white line color
    elevation_normal: 10  # add shadow effect
```
The program above is an MDRaisedButton, a button that can be connected to the python file for any python-programmed functions through the on_press attribute. In the example, there is a text "LOG IN" inside the button with the font size of 20. The Button is horizontically centered, with its text color being white, background being gray, and with white border lines and a shadow effect. When pressed, it will activate the try_login() function of the respective screen. This design of MDRaisedButton is applied for every single button available in the screen, hence centralizing function as well as the design of the application. 

### MDTextField
```.kv
MDTextField:
    id: uname_in
    hint_text: "username"
    icon_right: "account"
    helper_text_mode: "on_error"
    helper_text:""
    size_hint_x: None
    width: 750
    font_size: 25
    pos_hint: {"center_x": 0.5}
    mode: "rectangle"
```
The program above is an MDTextField, in which clients are able to input information on their keyboard. In the given example, the id of the MDTextField is uname_in which is an abbreviation of username input. it has a hint_text of "username" that slightly displays in the MDTextField to give the user an idea of what they are supposed to input. The MDTextField also has an human designed icon at the right side of it, named "account" in the KivyMD icons library. Furthermore, this textfield has a helper_text that activates when error, and the error as well as the helper text will be defined on the python file, hence enhancing flexibility of the helper_text. The width of the text field isset to 750, the font size to 25, and is vertically centered within its parent. All MDTextFields in the application is centralized with this design. 


## Development of Application Using Python

### Login and Registration System

#### The Login System with verification process and policies
```.py
    def try_login(self):

        username = self.ids.uname_in.text.strip()
        password = self.ids.passwd_in.text.strip()

        if not username or not password:
            if not username:
                self.ids.uname_in.error = True
                self.ids.uname_in.helper_text = "Please fill in this Field"
                self.ids.error_text.text = "*Please fill all fields"

            if not password:
                self.ids.passwd_in.error = True
                self.ids.passwd_in.helper_text = "Please fill in this Field"
                self.ids.error_text.text = "*Please fill all fields"

        else:
            db = database_handler("kanji_app.db")
            query = f"SELECT * FROM users WHERE username = '{username}'"
            search_result = db.search(query)
            if len(search_result) == 1:
                id, email, uname, hashed = search_result[0]
                # hashed = result[0][2]
                if check_password(password, hashed):
                    logging.info("Login Successful: %s", username)
                    self.user_id = id
                    self.parent.current = "HomeScreen"
                    self.ids.uname_in.text = ""
                    self.ids.passwd_in.text = ""
                    self.ids.error_text.text = ""
                    db.close()
                else:
                    self.ids.error_text.text = "*Password is incorrect"
                    logging.error("Login Unsuccessful: %s", "Incorrect Password")
            else:
                self.ids.error_text.text = "*User not found"
                logging.error("Login Unsuccessful: %s", "User not found")
```
This is a method that takes in the user inputs of username and password, and determine whether there is an account that matches the input or not. If there is, it will allow the user to move on to the Home Screen, and if not, it will become an error. Firstly, it determines whether there is properly an input or not in the first place. If either username or password lacks error, it will activate the error in the MDTextField that will display the error_text, and defines the error_text as "*Please fill all fields.*" This way, the user will be easily notified of the error, and will be able to fix it accordingly. If there is properly an input, the program will then open thedatabase of the application and compare the inputs with the datas in the users table of the database, where all the users credentials are stored. The hapassword will be converted to a hash and compared to the data, while the username will be compared directly. If any data matches with the input, all MDTextField's will be emptied and the user will be allowd into the Home Screen. Otherwise, if the password is incorrect, the error_text will show up saying "Password is incorrect." Furthermore, if a user is not found in the first place, an error_text will also show up saying "User not found."


#### Registration System with verification methods as well as policies
```.py
class RegistrationScreen(MDScreen):
    def try_register(self):
        # Get the values of the input fields
        username = self.ids.username_registration.text.strip()
        email = self.ids.email_registration.text.strip()
        password = self.ids.password_registration.text.strip()
        password_confirm = self.ids.password_confirm_registration.text.strip()

        # Check if any of the input fields are empty
        if not username or not email or not password or not password_confirm:
            self.ids.error_text.text = "*Please fill all fields"

        # Check if the password and confirmation password do not match
        elif password != password_confirm:
            self.ids.password_confirm_registration.error = True
            self.ids.error_text.text = "*Password and confirmation password do not match"
        elif not re.match(r"^[^@]+@([a-zA-Z0-9]+[.])+(com|edu|net|org|gov|mil|biz|info|mobi|name|aero|asia|jobs|museum|coop|jp|[a-zA-Z]{2})$", email):
            self.ids.email_registration.error = True
            self.ids.error_text.text = "*Invalid email address"
        elif database_handler("kanji_app.db").search(f"SELECT * FROM users WHERE username='{username}' OR email='{email}'"):
            # Username or email already exists
            self.ids.username_registration.error = True
            self.ids.email_registration.error = True
            self.ids.error_text.text = "*Username or email already exists"
        else:
            # Register the user
            db = database_handler("kanji_app.db")
            hash = encrypt_password(password)
            query = f"INSERT into users (email, password, username) values('{email}','{hash}','{username}')"
            db.run_save(query)
            db.close()
            logging.info("Registration Completed: %s", f"Credentials are UN:{username}, EM:{email}, and PW:{hash}.")
            self.parent.current = "LoginScreen"
```
This is a method that registers a user with their provided credentials. As shown above, in this method, if/elif/else statements are used often to implement verification steps. The method first takes the input of the user, and translates into a local variable. After that, the method ensures that all fields necessary are filled, and or else it will provide an error text "*Please fill all fields*." Following that procedure, the method checks if the provided password and the password confirmation matches. This is to ensure that the password that the user provided is authentic without any unintended mistakes such as a typo. And then the method also checks if an email provided is properly anemail address. It does this with the re import that provides us with match functions that makes the process easier. And then, it also checks if the provided username or email already exists in the database to avoid overlapping accounts with the same credentials. If not it moves on to register the user. 

### Add&Delete System


#### Add function
```.py
def try_add(self):
    kanji = self.ids.add_kanji_input.text.strip()
    hiragana = self.ids.add_hiragana_input.text.strip()
    katakana = self.ids.add_katakana_input.text.strip()
    meaning = self.ids.add_meaning_input.text.strip()
    user_id = self.manager.get_screen("LoginScreen").user_id

    db = database_handler("kanji_app.db")
    add_kanji = f"INSERT into kanji_database (user_id, kanji, hiragana, katakana, meaning) values ('{user_id}','{kanji}','{hiragana}','{katakana}','{meaning}')"
    db.run_save(add_kanji)
    db.close()

    self.ids.add_kanji_text.text = "*Kanji Added"
    self.ids.add_kanji_input.text = ""
    self.ids.add_hiragana_input.text = ""
    self.ids.add_katakana_input.text = ""
    self.ids.add_meaning_input.text = ""
```
In the function above, the user input is translated into a local variable and appended into the kanji_database. This function is introduced in the AddKanjiScreen, and is to add the user's input into the database for future references. After taking the user input and translating it into a local variable, it opens up the database, creates a query to add all the variables to the database, executes it, and closes the database. It then empties all the inputs to make it easier for the user to enter their next kanji inputs. 



#### Python List
```.py
def on_pre_enter(self, *args):
    # before the srceen is created, this code is run
    self.data_table = MDDataTable(
        size_hint=(.5, .56),
        pos_hint={"center_x": .41, "center_y": .445},
        use_pagination=True,
        check=True,
        rows_num=10,
        pagination_menu_pos="center",
        # title of the columns
        column_data=[("ID", 35),
                     ("Kanji", 35),
                     ("Hiragana", 35),
                     ("Katakana", 35)
                     ]
    )
    self.data_table.theme_cls.theme_style = "Dark"
    # add the functions for events of the mouse
    # self.data_table.bind(on_row_press=self.row_pressed)
    self.data_table.bind(on_check_press=self.check_pressed)
    self.add_widget(self.data_table)  # add table to the GUI
    self.update()
```

This program above creates a list for the user with kanji datas exclusive to the user. The list includes columns as follows: ID, Kanji, Hiragana, and Katakana. Checks are available, and pagination is also available to enhance user-friendliness by removing an endless list. The theme is adjusted to dark to accomodate with the overall style. This list will provide a list to all kanji datas, and the user will be able to check on the data that they would like to get rid of. The data of the kanji clicked will be sent to a different method that is connected to a button which executes a generated query for deletion. 


#### Delete Function - Connected to a button
```.py
  def save(self):
      checked_rows = self.data_table.get_row_checks()
      db = database_handler("kanji_app.db")
      for row in checked_rows:
          id = row[0]  # assuming the primary key column is the first column
          query = f"DELETE FROM kanji_database WHERE id={id}"
          db.run_save(query)
      db.close()
      self.update()
```

In the function above, the rows that were checked by the user in the Python list introduced above are put into a local variable, "checked_rows." The function, then, opens the database, and for every row in "checked_rows," it creates an original query using the ID of the data to delete it from the database. It then runs the query. This is repeated until there are no more rows left in "checked_rows," and the database is closed. 


#### Updating the List
```.py
    def update(self):
        user_id = self.manager.get_screen("LoginScreen").user_id
        # read database and update table
        db = database_handler("kanji_app.db")
        query = f"SELECT id, kanji, hiragana, katakana from kanji_database where user_id={user_id}"
        results = db.search(query)
        db.close()
        data = []
        for result in results:
            id = result[0]
            kanji = f"[font=Japanese.ttc]{result[1]}[/font]"
            hiragana = f"[font=Japanese.ttc]{result[2]}[/font]"
            katakana = f"[font=Japanese.ttc]{result[3]}[/font]"
            data.append([id, kanji, hiragana, katakana])
        self.data_table.update_row_data(None, data)
```

The function above is one that collects exclusive data that belongs to the user that is logged in, and put it into the pre-made python list. This function is used after anything is deleted from the database by the user to keep the list up-to-date, as well as when the user opens the DeleteKanjiScreen. In this function, a query to select the ID, Kanji, Hiragana, and Katakana from the kanji_database that belongs to the exclusive user_id is generated, and executed. After that, kanjim hiragana, and katakana data values are translated to a Japanese font, as default Python does not accept fonts from other languages. Then, the data is appeneded into the rows of the list. 

### Kanji List

```.py
def on_pre_enter(self):
    user_id = self.manager.get_screen("LoginScreen").user_id
    db = database_handler("kanji_app.db")
    query = f"SELECT kanji, hiragana, katakana, meaning FROM kanji_database WHERE user_id={user_id}"
    results = db.search(query)
    db.close()

    for result in results:
        kanji = f"[font=Japanese.ttc]{result[0]}[/font]"
        hiragana = f"[font=Japanese.ttc]{result[1]}[/font]"
        katakana = f"[font=Japanese.ttc]{result[2]}[/font]"
        meaning = f"[font=Japanese.ttc]{result[3]}[/font]"

        panel = MDExpansionPanel(
            icon=md_icons['book-education'],
            content=Content(),
            panel_cls=MDExpansionPanelThreeLine(
                text=kanji,
                secondary_text=hiragana,
                tertiary_text=katakana
            )
        )

        panel.content.add_widget(
            TwoLineIconListItem(
                text="Meaning",
                secondary_text=meaning
            )
        )

        self.ids.box.add_widget(panel)
```
The function above is used to create a Kanji List with dropdown function to hide/show meanings of the Kanji. It is the ultimate purpose that the whole application exists, and this list assists the user to learn kanji more efficiently with this dropdown function. In this function, all the kanji, hiragana, katakana, and meaning values of the data that exclusively belongs to the user logged in is selected. And then, it is transferred into Japanese font as it is appended into a list. However, initially, only the Kanji, hiragana, and katakana are appended into the list. In order to achieve the drop down, the meaning is appended into the list in the form of a different wiedget. This achieves to provide the user with a new level of experience. 


# Citations
1. OpenAI, https://openai.com/. Accessed 21 March 2023.
2. “Apple Keyboard PNG.” PNG Mart, 21 May 2016, https://www.pngmart.com/image/964. Accessed 21 March 2023.
3. “Apple Mac Computer Screen PNG Transparent Background, Free Download #39887 - FreeIconsPNG.” Freeiconspng, https://www.freeiconspng.com/img/39887. Accessed 21 March 2023.
4. “grayscale photo of man sitting on chair in front of table while writing photo – Free Japan Image on Unsplash.” Unsplash, 9 November 2017, https://unsplash.com/photos/PveJaE410_w. Accessed 21 March 2023.
5. “Kivy vs Flutter | Learn the Key Differences between Kivy and Flutter.” eduCBA, https://www.educba.com/kivy-vs-flutter/. Accessed 21 March 2023.
6. Malik, Ajay. “How Python Is Different From Other Languages.” C# Corner, 6 March 2020, https://www.c-sharpcorner.com/article/how-python-is-different-from-other-languages/. Accessed 21 March 2023.
7. “Oracle vs SQLite | What are the differences?” StackShare, https://stackshare.io/stackups/oracle-vs-sqlite. Accessed 21 March 2023.
8. “Python: 7 Important Reasons Why You Should Use Python | by Mindfire Solutions.” Medium, 3 October 2017, https://medium.com/@mindfiresolutions.usa/python-7-important-reasons-why-you-should-use-python-5801a98a0d0b. Accessed 21 March 2023.
9. “TIOBE Index.” TIOBE, https://www.tiobe.com/tiobe-index/. Accessed 21 March 2023.
10. “Wallpapers Kanji.” Wallpaper Cave, https://wallpapercave.com/wallpaper-kanji. Accessed 21 March 2023.
11. “What is SQLite? And When to Use It?” Simplilearn, 16 February 2023, https://www.simplilearn.com/tutorials/sql-tutorial/what-is-sqlite. Accessed 21 March 2023.
12. “Which Python GUI library should you use in 2023?” Python GUIs, 24 July 2022, https://www.pythonguis.com/faq/which-python-gui-library/. Accessed 21 March 2023.
13. Yegulalp, Serdar. “Why you should use SQLite.” InfoWorld, 13 February 2019, https://www.infoworld.com/article/3331923/why-you-should-use-sqlite.html. Accessed 21 March 2023.


# Appendix

## Evidence of Consultation

### Client approval of proposed success critereas
<img width="1001" alt="Screen Shot 2023-03-06 at 11 19 48 AM" src="https://user-images.githubusercontent.com/111751273/223004760-b79bb2c4-7aa5-4be0-9025-7550eeb5233c.png">

### Client's review of application during development process
<img width="1173" alt="Screen Shot 2023-03-01 at 12 12 44 PM" src="https://user-images.githubusercontent.com/111751273/222035637-e178d390-664c-4789-93bd-48b542e8c634.png">

### Client's review of final product
<img width="1165" alt="Screen Shot 2023-03-05 at 10 34 02 PM" src="https://user-images.githubusercontent.com/111751273/222963697-2049e75d-386d-4b28-b9ff-bf0c1a78d266.png">
