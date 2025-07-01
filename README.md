# selenium-py.1
from selenium import webdriver
from selenium.webdriver.chrome.service import service, Service
from webdriver_manager.chrome import ChromeDriverManager
import time

#lunch browser
service = Service(ChromeDriverManager().install())
driver = webdriver.Chrome(service=service)

# open google
print(driver.title)
driver.get("https://www.google.com")
time.sleep(2)

# print the titel of the page
print(driver.title)

# close the browser
driver.quit()

