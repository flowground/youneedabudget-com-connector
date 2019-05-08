# ![LOGO](logo.png) YNAB API Endpoints **flow**ground Connector

## Description

A generated **flow**ground connector for the YNAB API Endpoints API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/youneedabudget.com/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:45:05+03:00

## API Description

Our API uses a REST based design, leverages the JSON data format, and relies upon HTTPS for transport. We respond with meaningful HTTP response codes and if an error occurs, we include error details in the response body.  API Documentation is at https://api.youneedabudget.com

## Authorization

Supported authorization schemes:
- API Key
## Actions

### List budgets

> Returns budgets list with summary information

*Tags:* `Budgets`

### Single budget

> Returns a single budget with all related entities.  This resource is effectively a full budget export.

*Tags:* `Budgets`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### Account list

> Returns all accounts

*Tags:* `Accounts`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### Single account

> Returns a single account

*Tags:* `Accounts`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `account_id` - _required_ - The id of the account

### List account transactions

> Returns all transactions for a specified account

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `account_id` - _required_ - The id of the account
* `since_date` - _optional_ - If specified, only transactions on or after this date will be included.  The date should be ISO formatted (e.g. 2016-12-30).
* `type` - _optional_ - If specified, only transactions of the specified type will be included. 'uncategorized' and 'unapproved' are currently supported.
    Possible values: uncategorized, unapproved.
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### List categories

> Returns all categories grouped by category group.  Amounts (budgeted, activity, balance, etc.) are specific to the current budget month (UTC).

*Tags:* `Categories`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### Single category

> Returns a single category.  Amounts (budgeted, activity, balance, etc.) are specific to the current budget month (UTC).

*Tags:* `Categories`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `category_id` - _required_ - The id of the category

### List category transactions

> Returns all transactions for a specified category

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `category_id` - _required_ - The id of the category
* `since_date` - _optional_ - If specified, only transactions on or after this date will be included.  The date should be ISO formatted (e.g. 2016-12-30).
* `type` - _optional_ - If specified, only transactions of the specified type will be included. 'uncategorized' and 'unapproved' are currently supported.
    Possible values: uncategorized, unapproved.
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### List budget months

> Returns all budget months

*Tags:* `Months`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### Single budget month

> Returns a single budget month

*Tags:* `Months`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `month` - _required_ - The budget month in ISO format (e.g. 2016-12-01) ("current" can also be used to specify the current calendar month (UTC))

### Single category for a specific budget month

> Returns a single category for a specific budget month.  Amounts (budgeted, activity, balance, etc.) are specific to the current budget month (UTC).

*Tags:* `Categories`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `month` - _required_ - The budget month in ISO format (e.g. 2016-12-01) ("current" can also be used to specify the current calendar month (UTC))
* `category_id` - _required_ - The id of the category

### Update a category for a specific month

*Tags:* `Categories`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `month` - _required_ - The budget month in ISO format (e.g. 2016-12-01) ("current" can also be used to specify the current calendar month (UTC))
* `category_id` - _required_ - The id of the category

### List payee locations

> Returns all payee locations

*Tags:* `Payee Locations`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)

### Single payee location

> Returns a single payee location

*Tags:* `Payee Locations`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `payee_location_id` - _required_ - id of payee location

### List payees

> Returns all payees

*Tags:* `Payees`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### Single payee

> Returns single payee

*Tags:* `Payees`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `payee_id` - _required_ - The id of the payee

### List locations for a payee

> Returns all payee locations for the specified payee

*Tags:* `Payee Locations`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `payee_id` - _required_ - id of payee

### List payee transactions

> Returns all transactions for a specified payee

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `payee_id` - _required_ - The id of the payee
* `since_date` - _optional_ - If specified, only transactions on or after this date will be included.  The date should be ISO formatted (e.g. 2016-12-30).
* `type` - _optional_ - If specified, only transactions of the specified type will be included. 'uncategorized' and 'unapproved' are currently supported.
    Possible values: uncategorized, unapproved.
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### List scheduled transactions

> Returns all scheduled transactions

*Tags:* `Scheduled Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)

### Single scheduled transaction

> Returns a single scheduled transaction

*Tags:* `Scheduled Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `scheduled_transaction_id` - _required_ - The id of the scheduled transaction

### Budget Settings

> Returns settings for a budget

*Tags:* `Budgets`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)

### List transactions

> Returns budget transactions

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `since_date` - _optional_ - If specified, only transactions on or after this date will be included.  The date should be ISO formatted (e.g. 2016-12-30).
* `type` - _optional_ - If specified, only transactions of the specified type will be included. 'uncategorized' and 'unapproved' are currently supported.
    Possible values: uncategorized, unapproved.
* `last_knowledge_of_server` - _optional_ - The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

### Update multiple transactions

> Updates multiple transactions, by 'id' or 'import_id'.

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)

### Create a single transaction or multiple transactions

> Creates a single transaction or multiple transactions.  If you provide a body containing a 'transaction' object, a single transaction will be created and if you provide a body containing a 'transactions' array, multiple transactions will be created.

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)

### Bulk create transactions

> Creates multiple transactions.  Although this endpoint is still supported, it is recommended to use 'POST /budgets/{budget_id}/transactions' to create multiple transactions.

*Tags:* `Deprecated`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)

### Single transaction

> Returns a single transaction

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `transaction_id` - _required_ - The id of the transaction

### Updates an existing transaction

> Updates a transaction

*Tags:* `Transactions`

#### Input Parameters
* `budget_id` - _required_ - The id of the budget ("last-used" can also be used to specify the last used budget)
* `transaction_id` - _required_ - The id of the transaction

### User info

> Returns authenticated user information

*Tags:* `User`

## License

**flow**ground :- Telekom iPaaS / youneedabudget-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
