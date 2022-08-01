# API test checklist
## Data Structure Correctness
## POST requests
* All fields filled with valid data
* Only required fields are filled
* Not all required fields are filled
* No field filled
* Validation of data in the fields (correct and incorrect data)
* Empty JSON
* Object creation date
##  GET requests
* Empty list (if possible)
* Completed list
* Pagination in the list (limit, offset)
* Getting a list with a limit on the number of entries
* Getting a list starting from the specified number
* In case of passing parameters with an incorrect value, 400 is returned with a description of the error in the response body
* With a negative offset, the list of users is returned starting from the first position.
* If offset does not exist, an empty list of users is returned.
* List sorting
* Requesting data by valid ID, checking the return of correct data
* Requesting data by a non-existent ID, but in a valid format
* Requesting data by invalid ID
## PUT requests
* Update with correct data
* Update by non-existent ID
* Update by invalid ID
* Field validation (correct and incorrect data)
* Partial update (not all fields are present in JSON)
## DELETE requests
* Deleting an existing object
* Deleting an object that has already been deleted
* Deleting by non-existent ID
* Deleting by invalid ID
* Removing and re-adding the same entity (if there are unique fields)
- Checking response statuses
- Checking for all possible errors
- Other specific checks in case of complex logic
