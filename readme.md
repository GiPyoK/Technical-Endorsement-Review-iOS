# Technical Endorsement Review: iOS Development

The Technical Endorsement Review for iOS Development is similar to the industry interview process and includes a Code Challenge and Live Interviews. This is meant assess your mastery of iOS Development while simulating and preparing you for the interview processes you'll experience during your job hunt. You will receive scores across two components:

1. iOS Interview (Live Interview)
2. Code Challenge (HackerRank) and Code Challenge Interview (Live Interview)

To complete your Technical Endorsement Review, you must receive a passing score across all components.

### 1. iOS Interview

During the iOS Interview, you'll be asked to show your mastery of concepts from each of the iOS Development Sprints:

1. Demonstrate an understanding of Swift concepts through explanations of foundational language features.
    - suits well with OOP
    - automatically managed memory
    - safe (clear object types)
2. Explain basic iOS app architecture as it relates to navigation, data flow, dependency injection, and the MVC design pattern.
    - Navigation:
        - navigation controller,
        - tab bar controller
        - segues
    - Data Flow:
        - segues
        - protocols and delegates
        - notification center (observers)
        - completion block
    - Dependency Injection:
        - protocols and delegates
        - It allows us to provide (or inject) object or data (dependencies) into another object
        - effectively test complex code with one or more dependencies
    - MVC
        - Model:
        - View:
        - Controller:
    - MVP
        - Model:
        - View:
        - Presenter: address all UI events on behalf of the view
    - MVVM
        - Model:
        - View:
        - ViewModel: presenting functions, methods and commands to uphold the state of the view. Operate the model and activate the events in the view itself
3. Explain the importance of data persistence to create a consistent user interface/experience.
    - Data Persistence
        - Property List
        - User Defaults
        - Core Data
4. Explain the difference between synchronous and asynchronous code and show examples of GCD and closures in the context of making network calls.
    - sync: in order
    - async: not in order
    - Grand Central Dispatch
5. Demonstrate practical uses of programmatic constraints for view layout and using the `draw()` method to build custom controls.
    - programmatic constraints
        - NSLayoutConstraint (top, bottom, leading, trailing)
        - Anchor
6. Explain the usefulness of Core Data as a persistence layer, show examples of data modeling/migration using the provided Xcode tools, and discuss the pitfalls and workarounds surrounding using Core Data with a multi-threaded application.
7. Explain the value of generics and provide examples for use cases in app development; explain concurrency in a general computing context, as well as the mechanisms in iOS that allow for concurrent programming.
    - race condition handle
        - lock
        - semaphore
        - Serial Queues
8. Explain the importance of automated testing and performance benchmarking and how they are accomplished in iOS apps.
    - Instruments (automated)
        - time profiler
        - allocations
9. Explain how third party frameworks are integrated into a project with dependency management and how design patterns are used in iOS development.
    - Carthage
    - CocoaPods
10. Demonstrate understanding of various media-related classes (audio, video, images, maps) for creating content rich iOS apps.
11. Demonstrate an understanding of Objective-C concepts through explanations of foundational language features.
    - Based on C programming language
    - C uses pointer and it doesn't have objects (functions and structures)
    - '@' symbol to differentiate from C language
    - .h = header file (functions + classes are declared)
    - .m = implementation file (functions are defined)
    - * pointer for any object
    - - = instance method
    - + = class method
    - (instancetype) = return type

        ```objectivec
        // .h
        @property NSNumber *largeNumber;
        - (instancetype)initWithLargeNumber:(NSNumber *)largeNumber;

        // .m
        - (instancetype)initWithLargeNumber:(NSNumber *)largeNumber {
        			self = [super init];
        			if (self) {
        					// Don't use self.propertyName in init/dealloc methods
        					_largeNumber = largeNumber;
        			}
        			return self;
        }
        ```

    - ARC: Automatic Reference Counting
    - @synthesize = override both setter/getter or disable them, still create instance variable
    - Property Atributes
        - readonly
        - readwrite (default)
        - atomic (default): prevents concurrent access to the object by multiple threads
        - nonatomic: faster than atomic, no guarantees for thread safety
        - nonnull
        - nullable
        - strong (default)
        - weak
        - assign (default for primitive types)
        - copy : use with NSString, NSArray, NSSet

    - Forward class declaration: @class
12. Explain advanced Objective-C concepts like memory management and KVO/KVC.
    - Key Value Observing
    - Key value Coding
    - closures (block)
        - returnType (^blockNameVariable)(parametersCommaSeparated) = ^returnType(parameters) { };
        - int (^addNumbers)(int a, int b) = ^int (int a, int b) { };
    - URLSession, NSJasonSerialization
    - MRC vs ARC
        - MRC:
            - creating object with "alloc", "copy", "new", then you own it
            - "retain" an object, then you own it
            - if you own it, must release it
    - objc to swift
        - Name-of-project-Bridging-Header.h
            - #import "GIPClassName.h"
        - GIPClassName.h
            - NS_SWIFT_NAME(ClassName)
    - swift to objc
        - .h
            - @class SwiftClass
        - .m
            - #import "SwiftClass-Swift.h"

**Possible Results**

- A passing score consists of scoring a two or higher across all objectives.
- Receiving a one on any objective(s) will be considered not passing.

---

**iOS Final Endorsement Review - Core (60 mins)**
[https://calendly.com/lambda-ios/final-endorsement-review-core](https://calendly.com/lambda-ios/final-endorsement-review-core)

## FAQ

- **How long will this take me to prep for?**

    It is not expected that you will need to take extra time to review if you are taking your interview right after core track during Labs. If you feel you need a review you can brush up on the topics above by reviewing training kit.

    If you are taking your interview after CS, you may want to review training kit as you have primarily been studying computer science for the past two months!

- **What if I don't pass?**

    You may reattempt the Technical Endorsement Review at any time after independently studying for your reattempt. If you feel you need more help to prepare, please reach out to your TL. 

- **Who will conduct the interview?**

    Your interview will be conducted by a Lambda Staff member.  

# 2. Code Challenge and Code Challenge Interview

You will take the code challenge at the end of Computer Science! 

Your Code Challenge and Code Challenge Interview are treated as one component of the Technical Endorsement Review. You will not be asked to schedule a Code Challenge Interview until you have successfully passed the Code Challenge with a score of 60% or higher. If you pass the Code Challenge and do not pass the Code Challenge Interview, your reattempt will include retaking the Code Challenge as well as the Code Challenge Interview.

### Code Challenge

The code challenge will be administered using HackerRank. You will be asked to solve three or four coding problems (depending on the version of the assessment). 

Each version of the HackerRank assessment has a time limit equal to one hour per problem. For example, if the version of the HackerRank you receive has four problems then you will have four hours to complete the assessment. You do not have to break up the time evenly between problems. You may, for example, choose to spend two hours on one problem and 30 minutes on each of the remaining three. 

HackerRank runs your code for each problem against a large number of test cases (additional to the test cases shown to you during the assessment). Your score is the total percentage of test cases passed. Your score is not affected by the time it takes you to complete each problem.

**Possible Results**

- A passing score is considered 60% or higher.

### Code Challenge Interview

During the Code Challenge Interview, your HackerRank assessment will be reviewed and you'll be asked to demonstrate that you can coherently explain your problem-solving process by walking through the results of your Code Challenge. You'll be scored on the following:

1. Code readability and parsability
2. Code organization and structure
3. Code syntax and formatting
4. Ability explain the underlying strategy used to solve the problem
5. Ability to assess the time and space complexity of your implementation
6. Ability to explain the rationale behind your analysis.

**Possible Results**

- A passing score consists of scoring a two or higher across all objectives.
- Receiving a one on any objective(s) will not be considered passing.

# FAQ

- **What is the format of the HackerRank challenge?**

    HackerRank is a platform that administrates coding challenges online. You can get familiar with the platform by taking this [sample test](https://www.hackerrank.com/tests/sample). 

    The HackerRank you will be taking as the Code Challenge portion of the Technical Endorsement Review will be time capped at one hour per problem. Each version of the assessment has either three or four problems. If you have a version of the assessment with four problems, you will have four hours to finish the assessment and break up the time between problems how you see fit. You may finish before then, but will not be allowed to use more time. 

- **What language will I have to use on the HackerRank challenge?**

    You can use the language of your choice, but we recommend using the primary language of your core track curriculum for the HackerRank:

    Web → JavaScript

    iOS → Swift

    Android → Java

    DS → Python

- **Are our HackerRank challenges labeled easy, medium or difficult according to HackerRank ratings? If it's a mix of all, how many in each category?**

    The difficulty rating of HackerRank challenges is not standardized. The difficulty of each problem vary, and each will require a combination of concepts learned during CS regarding data structures, critical thinking, and problem solving.
