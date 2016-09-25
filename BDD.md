BDD is discovering and specifying the behavior of the entire app. It is the high level business rules for everyone. BDD tests can be written at a high enough level for everyone to understand [example](example)

TDD is the low level requirements for devs, the behavior of the code and different objects.

## Feature Injection
### Hunt the Value
* Figure out what you need to deliver, what's the business value?
* Determine the features you need for the best outcome. Which features provide the most value?
* There is more value in the outputs than in the inputs. Deliver important features.

## Examples & Acceptance criteria

* These are the notes on the back of your user story cards. This is the minimum requirements for that user story to pass. This is what you use to write tests and then write code to make those tests (acceptence criteria) pass.
* Scenarios are the perfect form of acceptance criteria.
* The more uncertain a team is about a specific implementation, the more discussion around the example & acceptance criteria there should be. Move on when you're starting to state the obvious.
  

## Frameworks

BDD frameworks use describe, context, it, and expect.
scenario = describe  
given = context  
when = describe  
then = it  

For example, if you have the following scenario:  
```
Send Location in Chat  
Given that a user is in chat  
When the user taps to send their location  
Then the user should see a preview of the current location  
```
Then it should look like this in a quick test: 

## Example

```swift
class WhenSendingLocationInChat {

describe("Send Location in Chat") {

    context("a user is in chat") {

        before() {
            // Make sure a user is in chat
        }

       describe("the user taps to send their location") {

           before() {
               // Simulate that user taping to send their location
           }

           it("the user should see a preview of the current location") {
                expect(location).to.equal(currentLocation);
           }
       }
    }
}
}
```

## Personas

* Use personas to make it easier to write tests with a specific user in mind

## Directory Structure

Each directory in the tests folder is a feature folder. Each file should represent a single scenario.