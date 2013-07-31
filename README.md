# Safer Accounting Act

The Safer Accounting Act will enable users to better protect their financial accounts, drastically lower accounting and accounting software costs, and help the United States catch up to its European counterparts in terms of financial techology progress.


Current technical practice is for users to provide their financial accounts and passwords to each program or website that is involved in the accounting process. This is unreliable and extremely dangerous, as those credentials can be used to initiate transactions, not just read them.

This document will define a standard API that all financial institutions must implement in order to be compliant.

In addition, financial institutions are required to make the last 180 days of transaction information available through this API.

## Security 

Financial institutions which offer online banking *must* give users the ability to generate, through their web browser, one or more API keys and passwords for each financial account.  Users must be able to give each key a friendly name so they can effectively manage permissions.

* API key IDs must have at least 120 bits of entropy
* API passwords must have at least 240 bits of entropy
* Users must be able to create multiple API keys per financial account
* It must be possible to generate a separate API key for each financial account, even if the online account has multiple financial accounts associated with it. 
* It is suggested that an API key be offered for all financial accounts accessible to the user, but it is not required.
* If a single financial account holds balances in multiple currencies, they are considered separate accounts for the purpose of this document. 

* All communication must be performed over an SSL connection. 

## Permissions

* Banks may offer additional functionality, but it must remain possible for users to generate a read-only API key that does not provide a third party with the ability to modify any account information or transactions. 


## Data formats

* All responses must be transmitted in valid, conformant XML 1.0 per http://www.w3.org/TR/REC-xml/. 

## API methods

* List accounts
* Get account balance
* Get account transactions


## GetTransactions


### Required fields

* Amount
* Currency
* Date completed
* Description
* State = [Completed, Pending]
* Type = [Debit, Credit]
* ACHClass = http://www.achdirect.com/resources/seccodes.asp


### Optional fields
* Date initiated
* Unique, persistent transaction ID
* 
* 

## List Accounts



## See also

http://openhbci.sourceforge.net/

http://www.ofx.net/AboutOFX/AboutOFX.aspx


