from selenium import webdriver


"""
Purpose:

This program navigates to a specific website and votes for a particular group using a checkbox to select the
group you want to win. The website allows multiple votes from the same user, making several submissions possible.

Note: This project was inspired by a survey I was asked to help build. Due to personal morals I did not use this
program to allow my friends to win the survey. I did use the survey as a tester to see if my program does work properly.
"""


# Input the number of times you wish to vote
Vote_how_many_times = 48


def vote():

    """
    Opens desired website and clicks on box wanted. Then submits vote by clicking 'finish'. The action is repeated
    however many times chosen in 'Vote_how_many_times'.
    """

    for i in range(0, Vote_how_many_times):
        driver = webdriver.Chrome("C:\\Python34\selenium\\webdriver\\chromedriver.exe")
        driver.get("http://survey.constantcontact.com/survey/a07edl1e0deiwnmonqc/start")
        driver.implicitly_wait(15)

        """
        The xpath below explicitly finds the desired checkbox based on the name and value of checkbox wanted.
        Due to design of the survey's naming and id on the website the value of the checkbox needs to be known
        The next line of code needs to be fixed to specify which picture specifically wanted
        INSTRUCTIONS:
            In next line change the number value in "@value='3' " to the input of the number that corresponds
            to the picture you wish to select (1, 2, 3, or 4)
        """
        driver.find_element_by_xpath("//*[@name='currentResponsePageQuestions[0].currentResponseSelected'][@value='3']"
                                     ).click()
        driver.implicitly_wait(15)
        driver.find_element_by_id("submitBtn").click()
        driver.implicitly_wait(15)
        driver.close()

    driver.quit()

# executes vote function
vote()
