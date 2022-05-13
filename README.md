# CRUD App Backend

## Running the server
Go to
https://replit.com/@hwangso595/crud-backend and press run.

## Usage
##### To experiment with a UI, go to https://replit.com/@hwangso595/crud-frontend and press run
### Create inventory items
```
curl -X POST -d "name=String&quantity=Quantity" https://crud-backend.hwangso595.repl.co/items/create-item
```
#### Example
```
curl -X POST -d "name=cucumber&quantity=43" https://crud-backend.hwangso595.repl.co/items/create-item
```
Response
```
{"name":"cucumber","quantity":43,"deleted":false,"deleteMessage":"","_id":"627dd6acca35f96640287e08","__v":0}
```
### Edit items
```
curl -X PUT -d "name=String&quantity=Number" https://crud-backend.hwangso595.repl.co/items/update-item/:id
```
#### Example
```
curl -X PUT -d "quantity=3" https://crud-backend.hwangso595.repl.co/items/update-item/627dd6acca35f96640287e08
```
Response
```
{"name":"cucumber","quantity":3,"deleted":false,"deleteMessage":"","_id":"627dd6acca35f96640287e08","__v":0}
```
### Delete items
```
curl -X DELETE https://crud-backend.hwangso595.repl.co/items/delete-item/:id
```
```
curl -X DELETE -d "deleteMessage=String" https://crud-backend.hwangso595.repl.co/items/delete-item/:id
```
### View a list of items
```
curl https://crud-backend.hwangso595.repl.co/items
```
Example Response
```
[]
```
### When deleting, allow deletion comments and undeletion
#### View deleted items
```
curl https://crud-backend.hwangso595.repl.co/items/deleted-items
```
#### Undeletion
```
curl -X PUT https://crud-backend.hwangso595.repl.co/items/undelete-item/:id
```
