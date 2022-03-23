## SD Payment Gateway Releases

### 2.4.2

#### Bug Fixes

- Fixed an issue where users on a site had reported instances of an error raised in Payment Gateway with the CVN number. The transaction did not reach the actual payment gateway and this is an error raised on the NAV side. The issue was due to the CVN number being passed as an INT.

### 2.4.1

#### Enhancements

- The code in Ad Hoc Action on Demo Sales Order was updated.

- The Caption and the Caption ML for ENU and ENG was updated on the SD-UG Demo Sales Order Ad Hoc page.

- Fixed an issue where in the On Ad Hoc transactions functionality to bundle Authorise, create Payment Journal and Post Payment Journal in one step was not working.

- A change was made to the code to handle the setup of the Default Currency correctly on the SD-UG Currency Bank Link page. If an entry on the mapping table is not found for the blank currency, code will ultimately revert to the Default Bank Account No. of the Payment Gateway Setup Card.

- A change was made to the Setup and Auto Posting of the Journal to allow for Default Bank Accounts per currency.

- The SD-UG Demo Sales Order Ad Hoc page was reworked and actions factboxes etc were stripped out and the caption ML on the page was updated to SD-UG Demo Sales Order Ad Hoc.

- Functionality to was added to the Ad Hoc transactions to bundle Authorise, create Payment Journal and Post Payment Journal in one step.

- The Payment not Posted Cue on the Role Centre was reinstated as this cue applies to situations when the automatic posting of the journal payment fails. This allows the users to tell if the journal has not auto-posted when the credit card transaction has been approved.

- A confirmation message is now displayed when putting through an ad-hoc payment from within a Sales Order or from the Role Centre.

- The Allocate Card Payments control action in the SD-UG Activity Cue CC Active was renamed.

- The group in the Ribbon on Payment Gateway Setup page was renamed from General to Related.

#### Bug Fixes

- The system was hanging when an error was raised on the Credit Card page.

### 2.4.0

#### Enhancements

- Added the Customer No. and the Customer Name to the SD-UG Awaiting Action

- Updated the Originated From field in the Awaiting CC Present postings entries for Invoices Posted off a Sales Order.

- A change was made not to allow users to delete actions without a warning in the Awaiting Actions List.

- The Allocate Card Payments Action was renamed to "Create/Allocate NAV Payment".

- Different icons were assigned to each cue on the Role Centre Activity Cues.

- Updated Payment Gateway objects to reference a new public key token for the dll.

- Code was reworked for the try function create and post payment in the SD-UG Integration Manager for NAV2018 testing.

- Code and logic for the Ad Hoc Transaction functionality was reworked.

- Fixed an issue where users could not drill down on the Awaiting CC Present cue on the Credit Card Active activity page.

- The Date Caption on the Credit Card page was updated.

- A batch number was added to the Payment Setup.

- A Demo Sales Order page was created and the AD Hoc Credit Card action was surfaced on the page.

- Visual changes were made to the Payment Gateway Setup Card.

- All field captions were reviewed and updated.

- Changes were made to the functionality and logic in the Transaction table.

- Removed show filters action from the SD-UG Transaction List.

- Standard NAV OneNote and Links were removed from the SD Payment Gateway pages.

- Changes were made to the Role Centre - activity pages were redesigned and new cues were created.

- The Ad Hoc transaction functionality was changed to bundle Authorise, create Payment Journal and Post Payment Journal into one step.

- Visual changes were made to the SD-UG Transaction List. Actions were removed and other actions were recaptioned.

- Visual changes were made to the Ad Hoc Card - a caption was placed beside the date field for ease of input and users prevented from inputting a negative amount and a message displayed that refunds cannot be processed through SD Payment Gateway if a negative amount is entered.

#### Bug Fixes

- Fixed an issue where the Customer Name was not displaying on the Card Transaction page when called from the Awaiting Card Action List.

- Fixed an issue with the Journal Lines created when a Card Card Transaction with no customer was put through the payment gateway.

- A compile error in the in the SD-UG Demo Sales Order Ad Hoc page in NAV 2018 and BC365 databases was fixed.

- An overflow error of the CLE Description on the CLE Description stamp was fixed.

### 2.3.4

#### Enhancements

- Transactions with a State of Error were filtered out from the Unallocated Transactions Cue. 

- Added an Unallocated Transactions Cue to the Payment Gateway Service Activity Group.

- Added an Allocated field to the Transactions List Page to make it easier to see what Credit Card Transactions have been allocated.

- Made a change to the functionality on posting a pre-paid Sales Order. A Credit Card Action should not be created if the Invoice Value is 0.

- Added an Alert on posting prepayments or invoices if the transaction is being tracked in the Recurring Payment Tracking Table. Allow users to view the Orders and the Invoices that are being tracked by the Recurring Payment.

- Added our standard About Action to the SD Payment Gateway Setup Card.

#### Bug Fixes

- An issue where Realex and Elavon were dropping a trailing 0 when the transaction was passed up to the gateway was fixed.

### 2.3.3

#### Enhancements

- The Credit Card Capture Control was not displaying on the Credit Card Transaction Card.

- Standard NAV OneNote, Notes and Links were removed from the Payment Trigger list page.

- The Routes option was removed from the Options FastTab in the Payment Gateway Card for the Worldnet Gateway Setup.

- Standard NAV OneNote, Notes and Links were removed from Setup Pages.

- If state is set to Complete on SD-UG Recurring Payment Card (43006056) and List page, all fields are disabled so no values can change even in edit mode.

#### Bug Fixes

- Fixed an issue where an error was raised when selecting Edit or View on Recurring Payment List.

- Some of the field captions in the Transaction Detail factbox were out of sync with the field values.

- Fixed a typo in the Gateway Card.

### 2.3.2

#### Enhancements

- Actions on the Transaction List page were renamed.

- On the Payment Gateway Role Centre and on the Transaction List page, renamed the "Ledger Entries" Action to "Allocated Card Payments" and exposed the standard NAV Customer Ledger Entry page.

- On the Card Transaction card a number of changes were made to the captions.

- The Card Payment Action was renamed to Ad hoc Card Payment on the Transaction List.

- A change was made to SimplyD.PaymentGateway.AddIn.Utilities.Decrypt on opening a Payment Gateway Card.

- Made a change to pass the current Customer No. from the Transaction List through to the Allocated Card Payments list when the Allocated Card Payments Action is chosen.

- The Help Files for SD Payment Gateway were generated.

- Changed the formatting of the Expiry Date on the Card Transaction page to MM/YYYY.

- Made a change on the Card Transaction page to default the Customer's Payment Method Code on the Customer Card, into the Payment Method Code field on the Card Transaction page.

- Renamed the Adhoc Card Payment Action on Role Centre Ribbon to Ad hoc Card Payment.

- Made a change to display the Customer Name on the Card Transaction page.

- Implemented a check that when setting the Payment Method Code for the Gateway to track that the Payment Method Code has a "Bal. Account No." set on the card.

- Made a change to allow a Transaction Code of up to 20 chars long on the SD Payment Gateway Transaction table.

- On the Card Transaction page, Is Recurring? was renamed to Recurring.

- Capitalised the caption URL on the Card Transaction page.

- Capitalised the caption ID on the Gateway Card.

- The Activity Cues displayed in the SD Payment Gateway Role Centre were split out onto individual pages.

- Implemented Realex Recurring Payment.

- Implemented Realex Payment Gateway.

- Implemented Elavon Recurring Payments.

- Made a change to setup a Default Balancing Account on the Payment Gateway Setup Card.

- Added a new option to the Recurring Payment Type - "Get From CLE".

- Made a change that when presenting Payment at Gateway we present the Currency Code of the transaction. If the transaction's Currency Code is blank then we will present the Currency Code from the Setup (flowfield to the G/L Setup table LCY Code field).

- Changed spelling of a field in the Transaction Card - Recurring FastTab.

- Changed the Currency Code in the Payment Gateway Setup Card to a flowfield off the G/L Setup table.

- Created a Credit Card Payment Method in NAV 2017 for Realex.

- Created Recurring Payment Transaction functionality for Worldnet.

- Created Recurring Payment Transaction functionality for Elavon.

- Created Payment Transaction functionality for Worldnet.

- Created Payment Transaction functionality for Elavon.

- Created Payment Gateway functionality for Worldnet.

- Created Payment Gateway functionality for Elavon.

- Created the Payment Gateway Framework.

#### Bug Fixes

- In Recurring Credit Card Payments, a change was made to display an error message when a user enters a "Next Transaction on Date" that is earlier than the current Work Date.

- A change was made in the Allocate Card Payments page not to allow the user to amend the credit card Amount when posting the Credit Card Payment as a Payment.

- Removed the Credit Card No. field from the Allocate Card Payments card as this Credit Card No. field on the Gen. Journal Line table is not populated by SD Payment Gateway.

- Fixed an issue on the Allocate Card Payments page where the No. Series were not stamped on all lines generated by the Suggest Payments Action.

- Fixed an issue on the Card Transaction page where the Transaction Currency was not displayed on the page.

- Fixed an issue whereby if the Gateway configuration fails the credit card transaction is left in a state of "Processing" and the error is not reported to the user.

- Fixed an issue where the My Transactions List was not filtering down on the current user.

- Fixed an issue where on Export of Tables, the Payment Gateway tables were not displayed.

- Fixed a NAV 2016/2017 compatibility issue regarding incoming document processing and approval management on the Cash Receipts Journal Page.

- Fixed a display issue with the Amount field on the message that displays on the Sales Order Credit Card Confirmation Window.

