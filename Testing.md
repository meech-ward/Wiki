## Testing

* A test should either be passing or pending, not failing. Unless you're currently writing the test.
* A test should **clearly** communicate it's intent in plain english. It should be readable by anyone.
* A test should be easy to maintain for all developers.
* A test should be reliable, it should only pass if the business logic passes, and it should fail if the business logic fails.

## Testing resources like databases

* Don't access production databases in tests.
* Try to avoid accessing real databases that take a long time to read and write.
* Use the `setup` or `before` methods in the test suite to setup and clean test databases to be used in the test suite. 

## Naming
Use the word 'When' to prefix all test classes.
Use the word 'Should' to prefix all test methods.

```swift
class WhenEarningNewStatusLevel {
    func shouldEarnStatusBasedOnPointsEarned() {
        /// Write your test here
    }
}
```

## Non UI Tests