from selenium import webdriver
from getpass import getpass

username = input("Enter in your username")
password = getpass("Enter your password on screen: ")
#here getpass enables us to enter the password on the screen but noone will be able to see that
driver = webdriver.Chrome("C:\\Users\\pc\\Downloads\\chromedriver_win32\\chromedriver.exe")
driver.get("https://www.facebook.com/")
#find the id by right clicking on the tab of username and then click on Inspect element code and then find the value written in id
username_textbox = driver.find_element_by_id("email")
username_textbox.send_keys(username)

password_textbox = driver.find_element_by_id("pass")
password_textbox.send_keys(password)

login_button = driver.find_element_by_id("xxxxx")
login_button.submit()

