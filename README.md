# LinkedIn Selenium Automation Project

This project automates LinkedIn login, search, and opening a search result
using Java, Selenium WebDriver, and TestNG.

## Requirements

- Java 17 or later
- Maven
- Google Chrome
- IntelliJ IDEA

## Project setup

1. Open the project in IntelliJ IDEA as a Maven project.
2. Allow Maven to download the dependencies from `pom.xml`.
3. Selenium Manager configures the required ChromeDriver.

## Configure credentials

Use your own LinkedIn account. Configure these environment variables
in the IntelliJ run configuration for the test:

- `LINKEDIN_USERNAME`: LinkedIn email or username
- `LINKEDIN_PASSWORD`: LinkedIn password

To add them:

1. Open the test's run configuration using **Edit Configurations**.
2. Find **Environment variables**.
3. Add the two variables and their values.
4. Click **Apply** and **OK**.

Do not add actual credentials to the source code or share them.

## Run the tests

In IntelliJ, open the test class and click the green Run icon next to
the test method. Configure the environment variables for each run
configuration as needed.

Tests include:

- `LoginTest.validLoginTest`: verifies a valid login.
- `LoginTest.invalidLoginTest`: verifies the error for an invalid password.
- `SearchTest.searchTest`: searches and verifies a visible result.
- `SearchResultTest.openFirstSearchResultTest`: opens a search result.

## Screenshot

The search test saves a browser screenshot to
`screenshots/search-results.png` after a successful search.

## Login security and limitations

LinkedIn may show security checks or CAPTCHA. Do not bypass them.
If needed, complete verification manually and document any interruption.
LinkedIn page layouts and search results may change, so locators or tests
may need updates.