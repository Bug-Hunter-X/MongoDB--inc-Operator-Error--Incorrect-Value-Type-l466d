# MongoDB $inc Operator Error: Incorrect Value Type

This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries. The error occurs when a string value is provided to `$inc` instead of a numeric value.

## Bug Description

The bug is caused by the incorrect usage of the `$inc` operator.  The `$inc` operator is used to increment a numeric field by a specified value. If a non-numeric value (such as a string) is provided, MongoDB will fail to properly increment the field. This can lead to unexpected results or errors.

## Solution

The solution involves ensuring that the value provided to `$inc` is a number. 

## How to reproduce

1. Create a MongoDB collection named `myCollection`.
2. Insert a document with the structure `{ _id: 1, field: 0 }`.
3. Run the incorrect update query (found in `bug.js`).
4. Observe that the field 'field' is not incremented as expected. Run the query that is in `bugSolution.js` for a proper update