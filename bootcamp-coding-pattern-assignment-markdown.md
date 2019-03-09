# AUT Pattern Name : [Name of the Pattern]

### Title : Coding assignment
- Coding assignment, what is asked in the coding assignment to implement

### Introduction
- Describe what you are trying to implement with the coding task

### Link to Assignment
- Assignment document link

### Previous Jira
- https://jira.devfactory.com/browse/{Previous_Jira}

### Current Jira
- https://jira.devfactory.com/browse/{Current_Jira}

### Previous Subsequent Pull-Request
- {Previous Pull-request}

### Current PR
- {Current Pull-request}

### Add Screenshot (for UI based work)
- Add screenshot and screenshot videos

### Pattern Found History
- What steps taken to find the pattern
- And who found the pattern and how.

### Pattern Business Value
- Write why your pattern is adding new value along with all the existing patterns. It is non-related to coverage gain. Only the business value terms.

### Find Such Block Percentage
- Your assumption on Finding Such Blocks in any given repo. (low to high put an average estimation it should not be based on samplemocking codebase.)

### Confluence Page Link
- Page link

### Demonstrated CodeBase (zip)
- ...(zip and codebase here with package so that running time is slower but we understand the filesize issue)

### AESCIS Running Video
- Video shows that AESCIS runs properly with new pattern. Show from generate UI, record full video.

### Demonstration Video (must)
- Demonstractoipo video means how it works, actual working video (link to googledrive)
- Video should not be related to the coding but the feature.
- Make sure to include all the testcases example in the video.

### Bootcamp Canidate's Check List (must)
- [ ] Appripriate markdown and title is being used (Title doesn't contain `#DocumentLink` but actual link and actual title than Assignment Title)
- [ ] Demonstration video added from google drive.
   - [ ] All test cases are shown in the demonstration video.
   - [ ] Video is conscise.
   - [ ] TestCase shown without implementation and with implementation.
   - [ ] Video length is not more than 10 mins.
- [ ] Updated task's excel sheet with ETA for investigation, development and status changed to Code Review.
- [ ] Already tracked your pull-requests and Jira in a different sheet inside the task workbook (excel).
- [ ] CRN review all green. (Exception to CRN review don't apply - if says const -> static readonly, remove set from interface)
- [ ] Pattern Quality Checking Bars
   - [ ] Is outputted pattern buildable. (Initializer Pattern + NewlyCreated Pattern) Output should be buildable.
   - [ ] Pattern is run against AESCIS project in file mode and generation is okay for new pattern + initializer pattern. Recording added.
  - [ ] Confluence page created for the pattern linked at : ...
  - [ ] Pattern Contains Mocking of Framework (Moq or MsFakes)
  - [ ] Created pattern doesn't contian bug in the static analyzer in the CI.
  - [ ] Used CsharpSyntaxNode over SyntaxNode (must).
  - [ ] Ask for pattern running Json file and commit the pattern running json file.
- [ ] Watched Code review guide for the team from prerequisite section. Apply Code review guide on the pull-request.
   - [ ] Ommited (Your) Author Name from Pattern.
   - [ ] Code doesn't contain magic strings, all are placed in the StaticTypes (CsharpIdentifiers, CommonConstants, AnyIdentifiers)
   - [ ] Linq is used properly.
     - [ ] Avoid using `Select(...).Select(..)` or avoid two or more loops when task can be combined into one.
            
            ```csharp
              doTask.Select(.. does one task...);
              doTask.Select(.. does another task...);
              // you are actually writing two forloop, use one. Avoid two forloops, write a single plain for loop, language has it you know, LINQ is only released around November, 2007
            ```
   - [ ] Don't use two loops together on same collection, if needed create simple for loop for process.
   - [ ] IList creation capacity given.
   - [ ] SOLID principal applied.
   - [ ] Used shouldly instead of throw new Argument Exception, point the argument name in the message. `arg.ShouldNotbeNull(nameof(arg));`
   - [ ] Rule of thums for Clean Code Applied
     - [ ] No method is more than 15 lines.
     - [ ] No method is taking more than three parameters.
     - [ ] Converted more than 3 parameters to an interface.
     - [ ] Avoid more than 2 interfaces parameters delegating to other methods (use one). 
     - [ ] DRY principal applied.
     - [ ] All methods are taking Interface than actual object.
     - [ ] If modified existing method then refactoring applied as per the rule.
   - [ ] Paths are used based on console arguments.
   - [ ] Optimized framework in terms of redundancy.
   - [ ] Created pattern doesn't contian bug in the static analyzer in the CI.
   - [ ] Datatemplate doesn't contain any mix of tabs and spaces, no imbalanced spaces.
   - [ ] Errors are captured with LogHelper or ConsoleLogger.
   - [ ] Any I/O is handled with `Try-Catch` ,plus, `LogHelper` used properly. And also MutexHelper is being used.
- [ ] Jira closed when PR is merged.
- [ ] Assign to reivewer when check-list is all checked except for merge.

### Reviewers's Check List (must)
- [ ] Appripriate markdown and title is being used (Title doesn't contain `#DocumentLink` but actual link and actual title than Assignment Title)
- [ ] Code quality is acceptable.
- [ ] Specific Quality Bars Passed
   - [ ] Is outputted pattern buildable. (Initializer Pattern + NewlyCreated Pattern) Output should be buildable.
   - [ ] Pattern is run against AESCIS project in file mode and generation is okay for new pattern + initializer pattern. Recording added.
   - [ ] Confluence page created for the pattern linked at : ...
   - [ ] Pattern Contains Mocking of Framework (Moq or MsFakes)
   - [ ] Optimized framework in terms of redundancy.
   - [ ] Created pattern doesn't contian bug in the static analyzer in the CI.
   - [ ] Used CsharpSyntaxNode over SyntaxNode (must).
   - [ ] Ask for pattern running Json file and commit the pattern running json file.
- [ ] CRN Review all green.
- [ ] Demonstration video given.
- [ ] Implementation works.
