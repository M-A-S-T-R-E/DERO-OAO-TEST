# DERO_OAO

Optimal Autonomous Organization on Dero

# What We Are Doing Here

We are building a UI for governing any contract that uses apollo's OAO standard. The standard is included in the contracts folder.

To use our website, a user will enter the SCID for their OAO-compliant contract into a search field.

The website will then read the contract data. It will find the the SCIDs for the governance tokens, and check the user's balance for those tokens. If the user's wallet contains any of those tokens, the website will make note of the user's role in the OAO accordingly. For example, if it sees that the user holds the key for Seat #1 in the board, the website will know that the user is member #1.

If there is an active proposal, the website will display this to the user. Going with the member #1 example, the website would display a button that says "Approve" and when the user clicks this button, the Approve function would be called and the UI would know to include Seat #1 in that call without the user needing to worry about inputting those details.

If the proposal is for an update to the contract code, there should also be a large text area in which the user can put in code to make sure it matches with the actual proposal. Here, in the background our app will be taking the sha256 hash of the code and comparing it with the stored HASH variable.
