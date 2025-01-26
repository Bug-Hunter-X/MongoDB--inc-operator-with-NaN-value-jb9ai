# MongoDB $inc Operator with NaN Value
This example demonstrates an uncommon error related to the `$inc` operator in MongoDB when used with `NaN` values.  Using `NaN` with `$inc` can lead to unpredictable results, potentially silently corrupting your data.  Always ensure numerical values are used with this operator.

## Bug
The provided JavaScript code attempts to increment a counter field using the `$inc` operator with a `NaN` value. This will likely result in unexpected behavior and is not a valid operation.

## Solution
The solution ensures that only valid numerical values are used with `$inc`.  In this scenario, either a numeric value or 0 should be used if the value is not available or valid. Error handling for invalid values is also recommended in a production setting.