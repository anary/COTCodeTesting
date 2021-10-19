# COTCodeTesting
Congratulations on progressing to the next stage of the interview process and thank you for your time in the process so far. The next stage of the process is our at home coding test. All Capital on Tap Engineers have gone through this test or something similar - it’s how we ensure that we have one of the best engineering teams in the industry!

Instructions
The test will consist of two user stories that we want you to complete. You will find these below These stories have been designed to imitate tasks you might be given to work on if you were a member of one of our teams.

Each story should take around 1 hour to complete, although this is not a hard limit.

You will be provided with a codebase that includes some existing functionality. We want you to build upon this, refactoring it appropriately. This is not a real system, however, it does contain some sample domain objects and concepts that we commonly use at Capital on Tap.

If you have any questions or require clarification, please don’t hesitate to ask us for further information.

Recommended Tools
You can use any IDE, although we would recommend that you use Visual Studio (Community Edition is fine) or Rider for .NET development and Visual Studio Code for React development.

For simplicity, the underlying data is situated in an embedded SQLite database. You can examine the data in this database using the SQLite Browser (https://sqlitebrowser.org/dl/).

What we’re looking for
Appropriate architectural decisions
Application of SOLID principles
A relevant testing strategy
Readability
Consistency
Maintainability
Sensible commits so that we can see your progress
Relevant comments and documentation, where appropriate
Submission
Once you have finished your solution, commit the files to the GitHub repository. Make sure you commit your files to a new branch. Raise one pull request containing your entire submission. Let us know you have completed this step and we will then conduct a code review. If you have notes or comments to make about your submission please add a section to this readme containing these.

Story 1
As a consumer of the API, I would like to receive a customer’s credit card information when I retrieve a customer’s details, so I can easily see the status of their card.

Description
When creating a new customer, the current system also creates a card. We’d like a way to retrieve the details of this card using a customer identifier.

Acceptance Criteria
An endpoint exists that accepts a customer identifier and returns a model representing a card
The card model returned represents the card that belongs to the customer
The properties for the card:
Id
FullName
CompanyName
CardNumber
ExpiryDate must appear in the returned model
Story 2
As a customer I want to be able to freeze and unfreeze my card so that if my card is lost it can't be used, but if I find it again I can enable it.

Description
When creating a new customer, the current system also creates a card. On occasions, customers would like to be able to prevent this card from being used.

Acceptance Criteria
The current endpoint that returns card information must include a “Status” property
An endpoint exists that updates a card’s status
A card’s status can be “Frozen” or “Active”, no other statuses are accepted or can be returned
The card’s status is updated appropriately in persistent data storage
