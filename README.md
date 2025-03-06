# ISTQB
## Testing Principles
<details>
  
1. **Testing shows the presence, not the absence of defects**. Testing can show that defects are present
in the test object, but cannot prove that there are no defects (Buxton 1970). Testing reduces the
probability of defects remaining undiscovered in the test object, but even if no defects are found, testing
cannot prove test object correctness.
2. **Exhaustive testing is impossible.** Testing everything is not feasible except in trivial cases (Manna
1978). Rather than attempting to test exhaustively, test techniques, test case prioritization, and risk-based testing, should be used to focus test efforts.
3. **Early testing saves time and money.** Defects that are removed early in the process will not cause
subsequent defects in derived work products. The cost of quality will be reduced since fewer failures will
occur later in the SDLC (Boehm 1981). To find defects early, both static testing and
dynamic testing (see chapter 4) should be started as early as possible.
4. **Defects cluster together.** A small number of system components usually contain most of the defects
discovered or are responsible for most of the operational failures (Enders 1975). This phenomenon is an
illustration of the Pareto principle. Predicted defect clusters, and actual defect clusters observed during
testing or in operation, are an important input for risk-based testing.
5. **Tests wear out.** If the same tests are repeated many times, they become increasingly ineffective in
detecting new defects (Beizer 1990). To overcome this effect, existing tests and test data may need to be
modified, and new tests may need to be written. However, in some cases, repeating the same tests can
have a beneficial outcome, e.g., in automated regression testing.
6. **Testing is context dependent.** There is no single universally applicable approach to testing. Testing is
done differently in different contexts (Kaner 2011).
7. **Absence-of-defects fallacy.** It is a fallacy (i.e., a misconception) to expect that software verification
will ensure the success of a system. Thoroughly testing all the specified requirements and fixing all the
defects found could still produce a system that does not fulfill the users’ needs and expectations, that
does not help in achieving the customer’s business goals, and that is inferior compared to other
competing systems. In addition to verification, validation should also be carried out (Boehm 1981)

</details>

## Test Activities and Tasks
<details>

- **Test planning** consists of defining the test objectives and then selecting an approach that best achieves
the objectives within the constraints imposed by the overall context. 
- **Test monitoring and test control.** Test monitoring involves the ongoing checking of all test activities and
the comparison of actual progress against the plan. Test control involves taking the actions necessary to
meet the test objectives. 
- **Test analysis** includes analyzing the test basis to identify testable features. Associated test conditions
are defined and prioritized, taking the related risks and risk levels into account. The test
basis and the test object are also evaluated to identify defects they may contain and to assess their
testability. Test analysis is often supported by the use of test techniques. Test analysis
answers the question “what to test?” in terms of measurable coverage criteria.
- **Test design** includes elaborating the test conditions into test cases and other testware (e.g., test
charters). This activity often involves the identification of coverage items, which serve as a guide to
specify test case inputs. Test techniques can be used to support this activity. Test design
also includes defining the test data requirements, designing the test environment and identifying the
necessary infrastructure and tools. Test design answers the question “how to test?”.
- **Test implementation** includes creating or acquiring the testware necessary for test execution (e.g., test
data). Test cases can be organized into test procedures, which are often assembled into test suites.
Manual and automated test scripts are created. Test procedures are prioritized and arranged within a test
execution schedule for efficient test execution. The test environment is built and
verified to be set up correctly.
- **Test execution** includes running the tests in accordance with the test execution schedule (test runs).
Test execution may be manual or automated. Test execution can take many forms, including continuous
testing or pair testing sessions. Actual test results are compared with the expected results. The test
results are logged. Anomalies are analyzed to identify their likely causes. This analysis allows us to report
the anomalies based on the failures observed.
- **Test completion** usually occurs at project milestones (e.g., release, end of iteration, test level
completion). For any unresolved defects, change requests or product backlog items are created. Any
testware that may be useful in the future is identified and archived or handed over to the appropriate
teams. The test environment is shut down to an agreed state. The test activities are analyzed to identify
lessons learned and improvements for future iterations, releases, or projects. A test
completion report is created and communicated to the stakeholders

</details>

## Generic Skills Required for Testing
<details>
  
- Testing knowledge (to increase effectiveness of testing, e.g., by using test techniques)
- Thoroughness, carefulness, curiosity, attention to details, being methodical (to identify defects,
especially the ones that are difficult to find)
- Good communication skills, active listening, being a team player (to interact effectively with all
stakeholders, to convey information to others, to be understood, and to report and discuss
defects)
- Analytical thinking, critical thinking, creativity (to increase effectiveness of testing)
- Technical knowledge (to increase efficiency of testing, e.g., by using appropriate test tools)
- Domain knowledge (to be able to understand and to communicate with end users/business
representatives)

</details>

## Software Development Lifecycle (SDLC) and Good Testing Practices
<details>

- For every software development activity, there is a corresponding test activity, so that all
development activities are subject to quality control
- Different test levels have specific and different test objectives, which allows
for testing to be appropriately comprehensive while avoiding redundancy
- Test analysis and design for a given test level begins during the corresponding development
phase of the SDLC, so that testing can adhere to the principle of early testing 
- Testers are involved in reviewing work products as soon as drafts of these work products are
available, so that this earlier testing and defect detection can support shift left
  
</details>

## TDD, ATDD and BDD
<details>

these approaches implements the principle of early testing and follows shift left, since the tests are defined before the code is written. They
support an iterative development model.

**Test-Driven Development (TDD):**

- Directs the coding through test cases (instead of extensive software design) (Beck 2003)
- Tests are written first, then the code is written to satisfy the tests, and then the tests and code are
refactored

**Acceptance Test-Driven Development (ATDD):**

- Derives tests from acceptance criteria as part of the system design process (Gärtner 2011)
- Tests are written before the part of the application is developed to satisfy the tests

**Behavior-Driven Development (BDD):**
  
- Expresses the desired behavior of an application with test cases written in a simple form of
natural language, which is easy to understand by stakeholders – usually using the
Given/When/Then format (Chelimsky 2010)
- Test cases should then automatically be translated into executable tests
  
</details>

## Shift Left testing
<details>

The principle of early testing is sometimes referred to as shift left because it is an
approach where testing is performed earlier in the SDLC. Shift left basically suggests that testing should
be done earlier (e.g., not waiting for code to be implemented or for components to be integrated), but it
does not mean that testing later in the SDLC should be neglected.
There are some good practices that illustrate how to achieve a “shift left” in testing, which include:
- Reviewing the specification from the perspective of testers. These review activities on
specifications often find potential defects, such as ambiguities, incompleteness, and
inconsistencies
- Writing test cases before the code is written and have the code run in a test harness during code
implementation
- Using CI and even better CD as it comes with fast feedback and automated component tests to
accompany source code when it is submitted to the code repository
- Completing static analysis of source code prior to dynamic testing, or as part of an automated
process
- Performing non-functional testing starting at the component test level, where possible. This is a
form of shift left as these non-functional test types tend to be performed later in the SDLC when a
complete system and a representative test environment are available

Shift left might result in extra training, effort and/or costs earlier in the process but is expected to save
efforts and/or costs later in the process.
For shift left it is important that stakeholders are convinced and bought into this concept.
  
</details>

## Test Levels
<details>

- **Component testing** (also known as **unit testing**) focuses on testing components in isolation. It
often requires specific support, such as test harnesses or unit test frameworks. Component
testing is normally *performed by developers* in their development environments.
- **Component integration testing** (also known as **unit integration testing**) focuses on testing the
interfaces and interactions between components. Component integration testing is heavily
dependent on the integration strategy like bottom-up, top-down or big-bang.
- **System testing** focuses on the overall behavior and capabilities of an entire system or product,
often including functional testing of end-to-end tasks and the non-functional testing of quality
characteristics. For some non-functional quality characteristics, it is preferable to test them on a
complete system in a representative test environment (e.g., usability). Using simulations of sub-
systems is also possible. System testing may be *performed by an independent test team*, and is
related to specifications for the system.
- **System integration testing** focuses on testing the interfaces of the system under test and other
systems and external services. System integration testing requires suitable test environments
preferably similar to the operational environment.
- **Acceptance testing** focuses on validation and on demonstrating readiness for deployment,
which means that the system fulfills the user’s business needs. Ideally, acceptance testing should
be performed by the intended users. The main forms of acceptance testing are: user acceptance
testing (UAT), operational acceptance testing, contractual acceptance testing and regulatory
acceptance testing, alpha testing and beta testing
  
</details>

## Test Types
<details>

**Functional testing** evaluates the functions that a component or system should perform. The functions
are “what” the test object should do. The main objective of functional testing is *checking the functional
completeness, functional correctness and functional appropriateness.*

**Non-functional testing** evaluates attributes other than functional characteristics of a component or
system. Non-functional testing is the testing of “how well the system behaves”. The main objective of non-
functional testing is checking the non-functional quality characteristics. The ISO/IEC 25010 standard
provides the following classification of the non-functional quality characteristics:
- Performance efficiency
- Compatibility
- Usability (also known as interaction capability)
- Reliability
- Security
- Maintainability
- Portability (also known as flexibility)
- Safety

It is sometimes appropriate for non-functional testing to start early in the SDLC (e.g., as part of reviews or
component testing). Many non-functional tests are derived from functional tests as they use the same
functional tests, but check that while performing the function, a non-functional constraint is satisfied (e.g.,
checking that a function performs within a specified time, or a function can be ported to a new platform).
The late discovery of non-functional defects can pose a serious threat to the success of a project. Non-
functional testing sometimes needs a very specific test environment, such as a usability lab for usability
testing.

**Black-box testing** is *specification-based* and derives tests from documentation not
related to the internal structure of the test object. The main objective of black-box testing is *checking the
system's behavior against its specifications.*

**White-box testing** is *structure-based* and derives tests from the system's
implementation or internal structure (e.g., code, architecture, work flows, and data flows). The main
objective of white-box testing is to *cover the underlying structure by the tests to an acceptable level*.

All the four above mentioned test types can be applied to all test levels, although the focus will be
different at each level. Different test techniques can be used to derive test conditions and test cases for
all the mentioned test types.

</details>

## Confirmation Testing and Regression Testing
<details>

**Confirmation testing** <mark>confirms that an original defect has been successfully fixed</mark>. Depending on the risk,
one can test the fixed version of the software in several ways, including:
- executing all tests that previously have failed due to the defect, or, also by
- adding new tests to cover any changes that were needed to fix the defect

However, when time or money is short when fixing defects, confirmation testing might be restricted to
simply exercising the test steps that should reproduce the failure caused by the defect and checking that
the failure does not occur.

**Regression testing** <mark>confirms that no adverse consequences have been caused by a change</mark>, including a
fix that has already been confirmation tested. These adverse consequences could affect the same
component where the change was made, other components in the same system, or even other
connected systems. Regression testing may not be restricted to the test object itself but can also be
related to the environment. It is advisable first to <mark>perform an impact analysis to recognize the extent of the
regression testing. Impact analysis shows which parts of the software could be affected.</mark>
Regression test suites are run many times and generally the number of regression test cases will
increase with each iteration or release, so regression testing is a strong candidate for automation. Test
automation should start early in the project. Where CI is used, such as in DevOps, it is
good practice to also include automated regression tests. Depending on the situation, this may include
regression tests on different test levels.

Confirmation testing and/or regression testing for the test object are needed on all test levels if defects
are fixed and/or changes are made on these test levels.  
</details>

## Static Testing and Dynamic Testing
<details>

- Static testing and dynamic testing (with analysis of failures) can <mark>both lead to the detection of
defects</mark>, however there are some defect types that can only be found by either static or dynamic
testing.
- Static testing finds defects directly, while dynamic testing causes failures from which the
associated defects are determined through subsequent analysis
- Static testing may more easily detect defects that lay on paths through the code that are rarely
executed or hard to reach using dynamic testing
- <mark>Static testing can be applied to non-executable work products, while dynamic testing can only be
applied to executable work products</mark>
- Static testing can be used to measure quality characteristics that are not dependent on executing
code (e.g., maintainability), while dynamic testing can be used to measure quality characteristics
that are dependent on executing code (e.g., performance efficiency)

Typical defects that are easier and/or cheaper to find through **static testing** include:

- Defects in requirements (e.g., inconsistencies, ambiguities, contradictions, omissions,
inaccuracies, duplications)
- Design defects (e.g., inefficient database structures, poor modularization)
- Certain types of coding defects (e.g., variables with undefined values, undeclared variables,
unreachable or duplicated code, excessive code complexity)
- Deviations from standards (e.g., lack of adherence to naming conventions in coding standards)
- Incorrect interface specifications (e.g., mismatched number, type or order of parameters)
- Specific types of security vulnerabilities (e.g., buffer overflows)
- Gaps or inaccuracies in test basis coverage (e.g., missing tests for an acceptance criterion)
  
</details>

## Test Techniques
<details>

**Black-Box Test Techniques**

- Equivalence Partitioning:
  - Divides data into partitions (known as equivalence partitions) based on the
expectation that all the elements of a given partition are to be processed in the same way by the test
object. One test for each partition is sufficient
  - In EP, the coverage items are the equivalence partitions. To achieve 100% coverage with this test
technique, test cases must exercise all identified partitions (including valid and invalid partitions) by covering each
partition at least once. Coverage is measured as the number of partitions exercised by at least one test
case, divided by the total number of identified partitions, and is expressed as a percentage.
Many test items include multiple sets of partitions (e.g., test items with more than one input parameter),
which means that a test case will cover partitions from different sets of partitions. The simplest coverage
criterion in the case of multiple sets of partitions is called Each Choice coverage

- Boundary Value Analysis
  -  exercising the boundaries of equivalence partitions as minimum and maximum values of a partition (boundary values)
  -  In *2-value BVA* (Craig 2002, Myers 2011), for each boundary value there are two coverage items: <mark>this
boundary value and its closest neighbor belonging to the adjacent partition</mark>. To achieve 100% coverage
with 2-value BVA, test cases must exercise all coverage items, i.e., all identified boundary values.
Coverage is measured as the number of boundary values that were exercised, divided by the total
number of identified boundary values, and is expressed as a percentage.
  - In *3-value BVA* (Koomen 2006, O’Regan 2019), for each boundary value there are three coverage items:
<mark>this boundary value and both its neighbors</mark>. Therefore, in 3-value BVA some of the coverage items may
not be boundary values. To achieve 100% coverage with 3-value BVA, test cases must exercise all
coverage items, i.e., identified boundary values and their neighbors. Coverage is measured as the
number of boundary values and their neighbors exercised, divided by the total number of identified
boundary values and their neighbors, and is expressed as a percentage.

3-value BVA is more rigorous than 2-value BVA as it may detect defects overlooked by 2-value BVA. For
example, if the decision “if (x ≤ 10) ...” is incorrectly implemented as “if (x = 10) ...”, no test data derived
from the 2-value BVA (x = 10, x = 11) can detect the defect. However, x = 9, derived from the 3-value
BVA, is likely to detect it.

- Decision Table Testing
  - specify how differentcombinations of conditions result in different outcomes. Decision tables are an effective way of recording
complex logic, such as business rules.
  -  the conditions and the resulting actions of the system are defined to rows of the table. table. Each column corresponds to a decision rule that defines a unique combination
of conditions, along with the associated actions.
  - To achieve 100% coverage with this technique, test cases must exercise all these columns.
Coverage is measured as the number of exercised columns, divided by the total number of feasible
columns, and is expressed as a percentage.

![image](https://github.com/user-attachments/assets/2932af59-e87f-485a-b3be-332b5ec1e9e7)

- State Transition Testing
  - A state diagram models the behavior of a system by showing its possible states and valid state
transitions. A transition is initiated by an event
  - A state table is a model equivalent to a state diagram. Its rows represent states, and its columns
represent events (together with guard conditions if they exist). Table entries (cells) represent transitions,
and contain the target state, as well as the resulting actions, if defined. In contrast to the state diagram,
the state table explicitly shows invalid transitions, which are represented by empty cells
  - A test case based on a state diagram or state table is usually represented as a sequence of events,
which results in a sequence of state changes (and actions, if needed). One test case may, and usually
will, cover several transitions between states.
  - Coverage criterias:
    - In all states coverage (weak), the coverage items are the states. To achieve 100% all states coverage, test
cases must ensure that all the states are exercised. Coverage is measured as the number of exercised
states divided by the total number of states and is expressed as a percentage.
    - In valid transitions coverage (also called 0-switch coverage, more widely), the coverage items are single valid
transitions. To achieve 100% valid transitions coverage, test cases must exercise all the valid transitions.
Coverage is measured as the number of exercised valid transitions divided by the total number of valid
transitions and is expressed as a percentage.
    - In all transitions coverage (complex), the coverage items are all the transitions shown in a state table. To achieve
100% all transitions coverage, test cases must exercise all the valid transitions and attempt to execute
invalid transitions. Testing only one invalid transition in a single test case helps to avoid defect masking,
i.e., a situation in which one defect prevents the detection of another. Coverage is measured as the
number of valid and invalid transitions exercised or attempted to be covered by executed test cases,
divided by the total number of valid and invalid transitions, and is expressed as a percentage

![image](https://github.com/user-attachments/assets/9d279295-aae5-4845-873a-f64b41e9557d)

![image](https://github.com/user-attachments/assets/13657cc5-b92a-409b-a4af-8166d520efc1)

**White-Box Test Techniques**

- Statement testing
  - In statement testing, the coverage items are executable statements. The aim is to design test cases that
exercise statements in the code until an acceptable level of coverage is achieved. Coverage is measured
as the number of statements exercised by the test cases divided by the total number of executable
statements in the code, and is expressed as a percentage. lso, 100%
statement coverage does not ensure that all the decision logic has been tested
- Branch testing
  - A branch is a transfer of control between two nodes in the control flow graph, which shows the possible
sequences in which source code statements are executed in the test object.
  - In branch testing the coverage items are branches and the aim is to design test cases to exercise
branches in the code until an acceptable level of coverage is achieved. Coverage is measured as the
number of branches exercised by the test cases divided by the total number of branches and is
expressed as a percentage
  - Conditional branches typically correspond to a true or false outcome from an
“if...then” decision, an outcome from a switch/case statement, or a decision to exit or continue in a loop.
However, exercising a branch with a test case will not detect defects in all cases.

<mark>Any set of test cases achieving 100% branch coverage also achieves 100% statement coverage (but not vice versa)</mark>

**Experience-based Test Techniques**

- Error guessing: tester design tests that will identify defects
associated with the errors, expose the defects, or cause the failures. These lists can be built based on
experience, defect and failure data, or from common knowledge about why software fails
- Exploratory testing: tests are simultaneously designed, executed, and evaluated while the tester learns
about the test object. Exploratory testing is useful when there are few or inadequate specifications or there is significant time
pressure on the testing
- Checklist-based testing: a tester designs, implements, and executes tests to cover test conditions from
a checklist. Checklists can be built based on experience, knowledge about what is important for the user,
or an understanding of why and how software fails. Checklist items are often phrased in the form of a question in high-level.
These items may refer to requirements, graphical interface properties, quality
characteristics or other forms of test conditions.

</details>

## Estimation Techniques
<details>

The estimate is based on a number of assumptions and is always subject to estimation error. Estimation for small tasks is
usually more accurate than for the large ones.
- **Estimation based on ratios**. In this metrics-based technique, figures are collected from previous projects
within the organization, which makes it possible to derive “standard” ratios for similar projects. The ratios
of an organization’s own projects (e.g., taken from historical data) are generally the best source to use in
the estimation process. <mark>These standard ratios (from historical data of previous projects) can then be used to estimate the test effort for the new
project</mark>. For example, if in the previous project the development-to-test effort ratio was 3:2, and in the
current project the development effort is expected to be 600 person-days, the test effort can be estimated
to be 400 person-days.
- **Extrapolation**. In this metrics-based technique, <mark>measurements are made as early as possible in the
current project to gather the data. Having enough observations, the effort required for the remaining work
can be approximated by extrapolating this data</mark> (usually by applying a mathematical model). This method
is very suitable in *iterative SDLCs*. For example, the team may extrapolate the test effort in the
forthcoming iteration as the averaged effort from the last three iterations.
- **Wideband Delphi**. In this iterative, expert-based technique, experts make experience-based estimations.
Each expert, in isolation, estimates the effort. The results are collected and <mark>if there are deviations of an
expert’s estimate that are out of range of the agreed upon boundaries, the experts discuss their current
estimates. Each expert is then asked to make a new estimation based on that feedback, again in
isolation. This process is repeated until a consensus is reached.</mark> Planning Poker is a variant of Wideband
Delphi, commonly used in Agile software development. In Planning Poker, estimates are usually made
using cards with numbers that represent the effort size.
- **Three-point estimation**. In this expert-based technique, three estimations are made by the experts: the
most optimistic estimation (a), the most likely estimation (m) and the most pessimistic estimation (b). The
final estimate (E) is their weighted arithmetic mean. In the most popular version of this technique, the
estimate is calculated as E = (a + 4*m + b) / 6. The advantage of this technique is that it allows the
experts to calculate the measurement error: SD = (b – a) / 6. For example, if the estimates (in person-
hours) are: a=6, m=9 and b=18, then the final estimation is 10±2 person-hours (i.e., between 8 and 12
person-hours), because E = (6 + 4*9 + 18) / 6 = 10 and SD = (18 – 6) / 6 = 2.

</details>

## Test Case Prioritization
<details>

Defines the order in which test cases are to be run
- **Risk-based prioritization**, where the order of test execution is based on the results of risk analysis. *Test cases covering the most important risks are executed first.*
- **Coverage-based prioritization**, where the order of test execution is based on coverage (e.g.,
statement coverage). Test cases achieving the highest coverage are executed first. In another
variant, called additional coverage prioritization, *the test case achieving the highest coverage is
executed first*; each subsequent test case is the one that achieves the highest additional
coverage.
- **Requirements-based prioritization**, where the order of test execution is based on the priorities of
the requirements traced back to the corresponding test cases. *Requirement priorities are defined
by stakeholders. Test cases related to the most important requirements are executed first*
  
</details>

## Some actions of Test Control
<details>
  
- Reprioritizing tests when an identified risk becomes an issue
- Re-evaluating whether a test item meets entry criteria or exit criteria due to rework
- Adjusting the test schedule to address a delay in the delivery of the test environment
- Adding new resources when and where needed

</details>

## Defect Information
<details>

- Unique identifier
- Title with a short summary of the anomaly being reported
- Date when the anomaly was observed, issuing organization, and author, including their role
- Identification of the test object and test environment
- Context of the defect (e.g., test case being run, test activity being performed, SDLC phase, and
other relevant information such as the test technique, checklist or test data being used)
- Description of the failure to enable reproduction and resolution including the test steps that
detected the anomaly, and any relevant test logs, database dumps, screenshots, or recordings
- Expected results and actual results
- Severity of the defect (degree of impact) on the interests of stakeholders or requirements
- Priority to fix
- Status of the defect (e.g., open, deferred, duplicate, waiting to be fixed, awaiting confirmation
testing, re-opened, closed, rejected)
- References (e.g., to the test case)
  
</details>

## Benefits and Risks of Test Automation
<details>

Potential benefits of using test automation include:

- Time saved by reducing repetitive manual work (e.g., execute regression tests, re-enter the same
test data, compare expected results vs actual results, and check against coding standards)
- Prevention of simple human errors through greater consistency and repeatability (e.g., tests are
consistently derived from requirements, test data is created in a systematic manner, and tests are
executed by a tool in the same order with the same frequency)
- More objective assessment (e.g., coverage) and providing measures that are too complicated for
humans to determine
- Easier access to information about testing to support test management and test reporting (e.g.,
statistics, graphs, and aggregated data about test progress, failure rates, and test execution
duration)
- Reduced test execution times to provide earlier defect detection, faster feedback and faster time
to market
- More time for testers to design new, deeper and more effective tests

Potential risks of using test automation include:

- Unrealistic expectations about the benefits of a tool (including functionality and ease of use).
- Inaccurate estimations of time, costs, effort required to introduce a tool, maintain test scripts and
change the existing manual test process.
- Using a test tool when manual testing is more appropriate.
- Relying on a tool too much, e.g., ignoring the need of human critical thinking.
- The dependency on the tool vendor which may go out of business, retire the tool, sell the tool to a
different vendor or provide poor support (e.g., responses to queries, upgrades, and defect fixes).
- Using an open-source software which may be abandoned, meaning that no further updates are
available, or its internal components may require quite frequent updates as a further
development.
- The automation tool is not compatible with the development platform.
- Choosing an unsuitable tool that did not comply with the regulatory requirements and/or safety
standards
</details>


## Priority vs Severity
<details>
- Severity defines the degree of impact of a bug on a software application to produce detrimental results. Greater the severity, larger would be the impact on the functionalities.

![image](https://github.com/user-attachments/assets/a82b4057-cf17-4615-84df-4a1f0cd6b424)

- Priority defines a bug in the terms of its degree of impact on the user and business & organizational needs and requirements along with the urgency to fix that bug. Higher the priority, sooner the bug will be resolved.

![image](https://github.com/user-attachments/assets/f0782037-d37b-4c84-bc29-fc1951db398c)

</details>
  
## How to calculate test coverage
<details>
Test Coverage is calculated by The number of test cases exercised divided by the total number of executable test cases, and is expressed as a percentage
</details>

## Scrum vs Kanban
<details>

**Scrum** is an Agile management framework wwith instruments and practices
- Sprint: Scrum divides a project into iterations (called sprints) of fixed length (usually two to four
weeks).
- Product Increment: Each sprint results in a potentially releasable/shippable product (called an
increment).
- Product Backlog: The product owner manages a prioritized list of planned product items
(called the product backlog). The product backlog evolves from sprint to sprint (called backlog
refinement).
- Sprint Backlog: At the start of each sprint, the Scrum team selects a set of highest priority
items (called the sprint backlog) from the product backlog. Since the Scrum team, not the
product owner, selects the items to be realized within the sprint, the selection is referred to as
being on the pull principle rather than the push principle.
- Definition of Done: To make sure that there is a potentially releasable product at each sprint’s
end, the Scrum team discusses and defines appropriate criteria for sprint completion. The
discussion deepens the team’s understanding of the backlog items and the product
requirements.
- Timeboxing: Only those tasks, requirements, or features that the team expects to finish within
the sprint are part of the sprint backlog. If the development team cannot finish a task within a
sprint, the associated product features are removed from the sprint and the task is moved
back into the product backlog. Timeboxing applies not only to tasks, but in other situations
(e.g., enforcing meeting start and end times).
- Transparency: The development team reports and updates sprint status on a daily basis at a
meeting called the daily scrum. This makes the content and progress of the current sprint,
including test results, visible to the team, management, and all interested parties. For
example, the development team can show sprint status on a whiteboard.

Scrum defines three roles:

- Scrum Master: ensures that Scrum practices and rules are implemented and followed, and
resolves any violations, resource issues, or other impediments that could prevent the team
from following the practices and rules. This person is not the team lead, but a coach.
- Product Owner: represents the customer, and generates, maintains, and prioritizes the
product backlog. This person is not the team lead.
- Development Team: develop and test the product. The team is self-organized: There is no
team lead, so the team makes the decisions. The team is also cross-functional 

**Kanban**  is a management approach that is sometimes used in Agile projects. The
general objective is to visualize and optimize the flow of work within a value-added chain. Kanban
utilizes three instruments
- Kanban Board: The value chain to be managed is visualized by a Kanban board. Each column
shows a station, which is a set of related activities, e.g., development or testing. The items to
be produced or tasks to be processed are symbolized by tickets moving from left to right
across the board through the stations.
- Work-in-Progress Limit: The amount of parallel active tasks is strictly limited. This is controlled
by the maximum number of tickets allowed for a station and/or globally for the board.
Whenever a station has free capacity, the worker pulls a ticket from the predecessor station.
- Lead Time: Kanban is used to optimize the continuous flow of tasks by minimizing the
(average) lead time for the complete value stream.

<mark>Kanban features some similarities to Scrum. In both frameworks, visualizing the active tasks (e.g., on
a public whiteboard) provides transparency of content and progress of tasks.</mark> Tasks not yet scheduled
are waiting in a backlog and moved onto the Kanban board as soon as there is new space (production
capacity) available.

<mark>Iterations or sprints are optional in Kanban. The Kanban process allows releasing its deliverables item
by item, rather than as part of a release. Timeboxing as a synchronizing mechanism, therefore, is
optional, unlike in Scrum, which synchronizes all tasks within a sprint</mark>

**Summary**

Scrum: Scrum is a framework with defined roles, events, and artifacts. It operates in time-boxed iterations called sprints, usually lasting 2-4 weeks. Scrum teams follow specific roles like Scrum Master, Product Owner, and Development Team, and have fixed ceremonies such as Sprint Planning, Daily Standups, Sprint Reviews, and Sprint Retrospectives.

Kanban: Kanban is a more flexible, continuous flow system that focuses on visualizing work and optimizing the flow of tasks. It doesn’t have specific roles or time-boxed iterations. Instead, it uses a Kanban board to manage the flow of work, with an emphasis on limiting work in progress (WIP) to improve efficiency and reduce bottlenecks.

</details>

## Bug life cycle
<details>

![image](https://github.com/user-attachments/assets/e501c2cb-cdd2-4534-8252-86eac1ac1a4b)


</details>


# MANUAL QUESTIONS
## SQL basics
<details>

```
SELECT (DISTINCT) column_name(s), TOP number|percent column_name(s)|* ,
        MIN(column_name) AS MinCol, MAX(column_name) AS MaxCol, COUNT(column_name), SUM(column_name), AVG(column_name)...
FROM table_name AS table1
(INNER|FULL OUTER|LEFT|RIGHT) JOIN table2
ON table1.column_name = table2.column_name
WHERE condition1
      AND condition2
      OR condition3
      AND NOT condition4
      AND column_name LIKE 'A%'
      AND column_name NOT LIKE 'B%'
      AND column_name BETWEEN 0 AND 100
      AND column_name NOT BETWEEN 10 AND 60
      AND column_name IN (value1, value2, ...)
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s) ASC|DESC;

///// EXAMPLE
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
WHERE LastName = 'Davolio' OR LastName = 'Fuller'
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 25;
```

```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```
 
```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
 
```
DELETE FROM table_name WHERE condition;
```
  
</details>

## How to assign tasks
<details>

1. Break down to clear, small tasks
2. Prioritize test items Based on Risk and Impact and consider the delivery schedule
- Risk-based prioritization: Start with the most critical areas of the application that are most likely to break or have the most impact on the end user.
For example, core functionalities like login, payment processing, or data security should be tested first.
Assign high-priority tasks to experienced testers who can handle complex or high-risk areas.

- Business impact: Consider the business impact when assigning tasks. Features that directly affect user experience or revenue (e.g., payment features, account management) should be prioritized and assigned to testers who understand their significance.

3. Assign Tasks Based on Skill Sets
- Based on volunteer spirit
- Leverage specialized expertise: Assign tasks according to the tester’s skill set and experience.
  - Experience on some functionalities
  - Manual Testing: Assign testers who are detail-oriented and skilled at exploratory and usability testing.
  - Automated Testing: Assign tasks for writing automation scripts to testers with experience in frameworks like Selenium, JUnit, or TestNG.
  - Performance and Security Testing: Assign these tasks to testers with specialized knowledge in tools like JMeter, LoadRunner, or penetration testing tools.
- Skill development: Use testing task assignments as an opportunity for team members to build on new skills. For example, if someone is interested in automation, allow them to take on some basic automation tasks with guidance.

</details>

## How to train new member about project technologies
<details>
  
1. Setup/config environment: install tool, clone repo..
2. Self-study: guideline/document in projects if available, basic concepts of new technologies on official site
3. Conduct structured hands-on training
- Key concepts: An overview of essential components (e.g., test scripts, test data, reporting, etc.).
- Step-by-step guides: Instructions on how to write, run, and troubleshoot test scripts.
- Advanced features: Detailed explanations of advanced functionality like integrations with CI/CD tools, data-driven testing, or test parallelization.
- Best practices: Coding standards, organizing test suites, and handling test data.
4. Create Practice Exercises: Design exercises that allow trainees to:
- Write scripts from simple to complex test scenario.
- Peer review for them raise question and give your feedback

</details>

## What is incident management?
<details>
  
Incidents are events of any kind that disrupt or reduce the quality of service (or threaten to do so) which requires an emergency response. A business application going down is an incident. A crawling-but-not-yet-dead web server can be an incident, too. It’s running slowly and interfering with productivity. Worse yet, it poses the even-greater risk of complete failure. Incidents can vary widely in severity, ranging from an entire global web service crashing to a small number of users having intermittent errors.

An incident is resolved when the affected service resumes functioning in its intended state. This includes only those tasks required to mitigate impact and restore functionality.

Incident management is the process used by development and IT Operations teams to respond to an unplanned event or service interruption and restore the service to its operational state.

When teams are facing an incident they need a plan that helps them:

- Respond effectively so they can recover fast.
- Communicate clearly to customers, stakeholders, service owners, and others in the organization.
- Collaborate effectively to solve the issue faster as a team and remove barriers that prevent them from resolving the issue.
- Continuously improve to learn from these outages and apply lessons to improve a service and refine their process for the future.

</details>

## Actions for Production bugs
<details>
  
1. Reproduce the defect
2. Collaborative Root-Cause Analysis
3. Fix, Verify, and Deploy Strategically
4. Lession learn and improvements to prevent defect

Possible Reasons for Bugs in Production

- Environment Differences => push the creation of a staging environment that mimics the production environment as closely as possible. Thorough testing in this environment should be performed before releasing to production.
- Data Discrepancies => Try to use realistic and diverse datasets during testing that reflect real-world scenarios, but review with sensitive data
- Insufficient Load Testing => Perform rigorous load and stress testing to identify performance bottlenecks on staging env.
- Third-Party Integration Problems
- Test Coverage Gaps (defect leakage) => review testing process (test design to get highest coverage, cross-review, exploratory test..) , add defect to automation and regression suit

</details>

## Test Approach in Time pressure
<details>
  
- Communication about test plan and tasks and schedule. Update progress frequently
- Smoke test e2e critical flows
- Find support by automation testing: Identify tests that you can automate, such as regression tests or smoke tests, which ensure the most critical functions work as expected after code changes.
- Test Prioritization on cases that not covered by automation:
  - Risk Assessment: evaluate which parts of the software are most critical to its operation and which areas have the highest likelihood of containing defects.
  - Focus on new features and changes that have been made since the last release. These areas are more prone to bugs than stable, unchanged parts of the software. 
  - Also, prioritize tests that have historically uncovered defects.
  - Exploratory/Adhoc Testing: Dive into the application with a critical eye, trying to emulate real-world user behavior and scenarios to find out uncovered/unforeseen cases.

</details>

## How to test without document
<details>

- Apply exploratory testing to understand the existing product
- Discuss to PO/Seniors to get business knowledge
- Go through production bugs to identify the edge cases
  
</details>

## How to make sure enough test cases
<details>

- Understand and analyze requirement carefully to list out test scenarios
- Apply test types/ techniques to identify positive/negative test cases in each scenario/functionality
- test cases must exercise to achieve all 100% coverage items in each technique, e.g: For complex flows, using decision table testing, the coverage items are the columns containing feasible combinations of
conditions (all columns). to cover all business rules and requirement specifications
  
</details>

## API schema
<details>

An API schema defines the structure of the data exchanged between a client and an API. It acts as a blueprint or contract that outlines how the data is formatted, what fields are expected, and the relationships between different data entities.

There are several ways to define API schemas depending on the type of API, such as REST, GraphQL, or others. Below are a few common ways to describe an API schema:

- OpenAPI Specification (formerly Swagger)
  - The OpenAPI Specification (OAS) is a widely used standard for describing RESTful APIs. It provides a comprehensive way to document API endpoints, request/response formats, authentication methods, and more.
- GraphQL Schema
  - For GraphQL APIs, the schema defines types, queries, mutations, and subscriptions that the API supports. It allows clients to request only the data they need, in contrast to REST APIs.
- JSON Schema
  - A JSON schema defines the structure of JSON data, typically used to validate and document data formats for API requests and responses.

</details>

## Actions if bug is not reproducible
<details>

- Provide evidence seenshot
- Give timestamp to check Application logs
- Provide test data

Actions when app throws the weird errors:

- Open Developer tools in browsers
  - Check Console for Javascript errors
  - Check Network for Request/Response failed
- check Application logs if possible
  
</details>

#  AUTOMATION QUESTIONS
## Design your tests for parallelization
<details>
  
Make your tests independent, atomic, and stateless. Independent tests do not depend on each other or on external factors, such as data, order, or environment. Atomic tests focus on one functionality or scenario, and do not have multiple steps or assertions. Stateless tests do not share or modify any global or static variables, and do not rely on any previous or subsequent tests. These characteristics make your tests more reliable, maintainable, and scalable when running in parallel.

</details>

## Challenges in automation
<details>
  
- Common Selenium errors (NoSuchElementException, StaleElementReferenceException, ClickElementInterceptException..)
- Run scripts cause high resource usage (e.g., memory leaks or high CPU usage).
  - Select the suitable concurrency tests in paralell
  - Use the browser option (e.g: no-sandbox) when initialize webdriver
  - Make sure to Close and quit all driver instances after each run
- Not give same outcome in local and pipeline
  - Network issues: The pipeline could be attempting to access remote resources (like an API or database) and fail due to network issues (timeouts, DNS problems, or security groups, IP whitelist).
  - Unstable Environment
- Flaky tests
- Technical issues: captcha, 2FA with authentication, get code from restricted mailbox..
- External dependency: using mock
- Write Test case is not suitable for automation: need to communicate with author to modify test case
  - write test cases more details, e.g: assession in each step, check UI..

</details>

## How do you handle flaky tests in your test automation framework?
<details>

1. Identify the root cause
  - Concurrency Issues:	Tests running in parallel that interfere with each other can lead to unpredictable outcomes.
    - Implement setup/teardown hook for reset db, delete cookie
    - Apply Dependence Injection to avoid leak states between concurrent tests
  - External Dependencies:	Reliance on third-party services, APIs, or databases that may not always behave consistently or are subject to network variability.
    - Using mock as possible
  - Timing and Synchronization Problems:	Tests that fail or pass depending on how quickly certain operations are completed, often due to inadequate wait conditions or assumptions about execution time.
    - observe application behavior carefully to find out the way to improve wait strategy
    - use tools or libraries that support **retry** mechanisms attempts to run only the failed steps at the time that they fail, thus avoiding the necessity to re-run whole scenarios (Java-based failsafe library, .NET-based Polly Retry library)
  - Non-deterministic Behavior:	Using random test data or relying on system states that may change between test runs can introduce variability in test outcomes.
  - Test Environment Instability:	Differences or changes in the test environment, such as software versions, configuration, or available resources, can cause tests to behave flakily.
2. Retry the failed tests
  -  Use framework capabilities to rerun flaky tests automatically when they fail, but it can increase the test execution time
3. Prioritize the stable tests
  - use tags, categories, or annotations to mark the stable and flaky tests and run them accordingly. prioritize the stable tests over the flaky ones and run the stable tests more frequently
4. Monitor and report the flaky tests
5. Refactor or remove the flaky tests
  
</details>

## Retry Approach
<details>

**Java-based failsafe library**

```
package stepDefinitions;

import dev.failsafe.Failsafe;
import dev.failsafe.RetryPolicy;
import dev.failsafe.RetryPolicyBuilder;
import dev.failsafe.function.CheckedRunnable;
import dev.failsafe.function.CheckedSupplier;
import java.time.Duration;
import java.util.Arrays;
import java.util.List;
import org.apache.logging.log4j.Logger;
import org.apache.logging.log4j.LogManager;
import org.openqa.selenium.NoSuchElementException;
import org.openqa.selenium.StaleElementReferenceException;
import org.openqa.selenium.ElementClickInterceptedException;

public interface RetryUtilitySteps {

    Logger log = LogManager.getLogger();
    int MAX_RETRIES_DEFAULT = 2;
    int MAX_DELAY_SECONDS_DEFAULT = 5;
    RetryPolicyBuilder<Object> policyBuilder = RetryPolicy.builder();
    List<Class<? extends Throwable>> exceptionsList = Arrays.asList(
            NoSuchElementException.class,
            ElementClickInterceptedException.class,
            StaleElementReferenceException.class,
            AssertionError.class
    );

    default void retryStep(CheckedRunnable runnable, int maxRetry, int delaySeconds) {
        RetryPolicy<Object> policy = policyBuilder.withMaxRetries(maxRetry)
                .withDelay(Duration.ofSeconds(delaySeconds))
                .handle(exceptionsList)
                .onRetry(e -> log.warn(String.format("attempting retry#: %d", e.getAttemptCount())))
                .onFailure(
                        e -> log.error(String.format("attempts: %d have failed", e.getExecutionCount())))
                .build();
        Failsafe.with(policy).run(runnable);
    }

    default Object getWithRetryStep(CheckedSupplier<Object> supplier, int maxRetry,
                                    int delaySeconds) {
        RetryPolicy<Object> policy = policyBuilder.withMaxRetries(maxRetry)
                .withDelay(Duration.ofSeconds(delaySeconds))
                .handle(exceptionsList)
                .handleResult(null)
                .onRetry(e -> log.warn(String.format("attempting retry#: %d", e.getAttemptCount())))
                .onFailure(
                        e -> log.error(String.format("attempts: %d have failed", e.getExecutionCount())))
                .build();
        return Failsafe.with(policy).get(supplier);
    }

}

```

```
public class HomePageSteps implements RetryUtilitySteps {
  @When("User navigates to create new customer account")
  public void userNavigatesToCreateNewCustomerAccount() {
    retryStep(() -> homePage.navigateToNewAccountPage(),
        MAX_RETRIES_DEFAULT,
        MAX_DELAY_SECONDS_DEFAULT);
  }
  
  @Then("User creates an account and verifies the message: {string}")
  public void userCreatesAnAccountAndVerifiesTheMessage(String alertText) {
    boolean IsAlertMessageDisplayed = (boolean) getWithRetryStep(() -> {
          createNewAccountPage.createAnAccount();
          return createNewAccountPage.IsAlertMessageDisplayed(alertText);
        },
        MAX_RETRIES_DEFAULT,
        MAX_DELAY_SECONDS_DEFAULT
    );
    Assertions.assertThat(IsAlertMessageDisplayed)
        .as("Assert that alert is displayed")
        .isTrue();
  }
}
```

**.NET-based PollyRetry library**


</details>

## Cases cannot be done by automation
<details>

- Unstable features
- One time test cases
- Adhoc cases
- Exploratory testing
- UI/GUI
- Technical challenges (Capcha, ActiveMQ, Azure storage..)
  
</details>

## How to select the right automation tool/framework
<details>

- Analyze a System Under Test to Determine the Appropriate Test Automation Solution
  - Gather requirements considering its scope and given capabilities. Different kinds of applications(e.g., web service, mobile, and web) need different kinds of test automation from a technical point of view.
  - collaboration with other stakeholders (e.g. manual testers, business stakeholders, and business analysts) to identify as many risks and their mitigations as possible
- Many test automation tools that meet these requirements that can be considered.
  - the comparison table is to allow stakeholders to see the differences between the tools based on specific requirements such as langualge/technology, configuration, data-driven, reporting, ci/cd..
- Pilot project for selected tool


1. Technical Info: 
  - Technologies ussed to develop application
  - Kinds of platforms: window, linux, macOS, android, ios
  - Kinds of application: web, desktop (win32, wpf, .net, java), mobile (wweb, native, hybrid), API, database
  - have existing fw?
  - source control
2. Automation Ability: able to run auto in the system
  - Go through main workflow of application
  - How often is the application updated? (stable enough)
  - Complicated controls: canvas, captcha, pdf, image
  - Challenges: missing info of API/DB for prepare/cleanup data
3. Test quantity: number of test cases/ browsers/ devices/ environments, test types, test levels
4. Test management: test process, testcase/defect/test result management, pipeline
5. Application Deployment: how/how often deploy application, testing env, tool for CICD
6. Automation coverage: number of automation test case/ number of manual test case, smoke/regression/e2e test
7. Tool selection / Table comparision
  - Support platform/app/language/testing approaches
  - usability, maintainability
  - Test runner
  - Cost/community
8. POC: demo/implement complicated test cases

**Automation quality**

- Coverage
- Script quality
- stability (number of flaky tests)*

</details>

## How setup the full process of CI/CD
<details>

![image](https://github.com/user-attachments/assets/4c9cc0f1-649c-4f1c-9af5-31cdd2401b1b)

Continuous Integration (CI):

- CI is the practice of frequently integrating code changes into a shared repository, often multiple times a day. The goal is to detect integration issues early by automatically running tests and validating code whenever changes are made.
Developers push their code to a central repository, where automated build and testing pipelines run, ensuring that new changes don’t break the existing codebase. The automation includes steps like code compilation, running unit tests, and other types of checks (static analysis, linting, etc.).

Continuous Delivery (CD):

- CD is the practice of automatically deploying code changes to production (or a staging environment) once they pass the automated tests in the CI process. It ensures that software is always in a deployable state, with the ability to release changes to end-users quickly and safely. CD involves automating not only the build and test processes but also the deployment, making it easy to release software at any time with minimal manual intervention. After CI checks pass, the code is automatically deployed to an environment (typically staging or production) where further tests and user acceptance tests (UAT) can be performed.

Key concepts overview

![image](https://github.com/user-attachments/assets/2423cf9c-32db-4f99-93ea-0bcbb22c024e)

- Prerequisites: Store your source code in a version control system that supported to setup CI/CD
- A trigger tells when a pipeline to run.
- A pipeline is made up of one or more stages. A pipeline can deploy to one or more environments.
- A stage is a way of organizing jobs in a pipeline and each stage can have one or more jobs.
- Each job runs on one agent. A job can also be agentless.
- Each agent runs a job that contains one or more steps.
- A step can be a task or script and is the smallest building block of a pipeline.
- A task is a prepackaged script that performs an action, such as runing automation tests, invoking a REST API or publishing a build artifact.
- An artifact is a collection of files or packages published by a run.

Example: .github/workflows/test.yml
```
name: Run Automated Tests

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

      - name: Upload test results
        uses: actions/upload-artifact@v2
        with:
          name: test-results
          path: ./test-reports
```

</details>

## Code review ?
<details>

Some common areas I will address include:

- Code organization: The structure of your test (e.g., how tests are grouped and arranged).
- Use of page object model (POM): If you're not already using it, I may recommend adopting it to improve maintainability.
- Selector strategies: Ensuring you're using reliable and efficient ways of finding elements.
- Reusability: How reusable your code is (e.g., common actions like login or clicking links).
- Error handling and waits: Best practices for dealing with dynamic content and ensuring tests don't break due to timing issues.
- Test data handling: Whether the test can be easily adapted to different scenarios with minimal changes.
- Logging and reporting: Making sure there’s adequate logging and proper assertions.

Clean code principles emphasize the following points:

- Use a common naming convention for the classes, methods, and variables for meaningful names
- Use a logical and common project structure
- Avoid hardcoding
- Avoid too many input parameters for methods
- Avoid long and complex methods
- Use logging
- Use design patterns where they are beneficial and required
- Focus on testability

</details>

## What is data-driven testing?
<details>

Data-driven testing is a way of testing the same functionality with different sets of input data and expected results. This allows you to cover more scenarios, reduce redundancy, and improve maintainability of your test cases. Data-driven testing can also help you to identify edge cases, boundary values, and invalid inputs that might cause errors or bugs in your application.

How to apply data driven in cucumber and specflow: parameterization for data values to scenario steps

1. Use regular expressions and capture groups to define flexible and dynamic steps that can accept various inputs or outputs. Regular expressions are patterns that match specific strings or characters in your step text. Capture groups are parts of the regular expressions that are enclosed in parentheses and can be extracted as parameters for your step definitions. To access the data from the capture groups, you can use the arguments or parameters in step definitions.
2. Use data tables in cucumber step to specify multiple data rows for your step, step will be repeated when have multiple data rows (e.g: add multiple address for user). You can also use data tables to define key-value pairs or lists of values for your steps. To access the data from the data tables, you can use the Table or List objects in your step definitions. Data tables from Gherkin can be accessed by using the DataTable object as the last parameter in a step definition. Depending on the table shape, it can also be accessed as one of the following collections:
  -  List<List<String>> table
  -  List<Map<String, String>> table
  -  Map<String, String> table
  -  Map<String, List<String>> table
  -  Map<String, Map<String, String>> table

![image](https://github.com/user-attachments/assets/093912d7-3daa-4d35-b78a-10d76c8399cd)

3. Use scenario outlines and examples. Examples are tables that provide data in the scenario outline, each line corresponding to one data set of scenario run. To access the data from the examples, you can use the `<placeholder>` syntax in scenario steps (placeholder is the name of table column headers). 
4. User external data source like json, csv, excel..., it's suitable to store large amounts of data or data that changes frequently. To access the data from the external files, you can use libraries or methods that can read and parse the file format in your step definitions.

**Transformers** : expression values, data tables into arbitrary objects.
- **Cucumber** expression parameters, data tables, and doc strings can be transformed into arbitrary Java objects.
  - @ParameterType

```

public class StepDefinitions {

    @ParameterType("([0-9]{4})-([0-9]{2})-([0-9]{2})")
    public LocalDate iso8601Date(String year, String month, String day) {
        return LocalDate.of(Integer.parseInt(year), Integer.parseInt(month), Integer.parseInt(day));
    }

    @Given("today is {iso8601Date}")
    public void today_is(LocalDate date) {

    }
}

```

  - @DataTableType

```
public class StepDefinitions {

    @DataTableType
    public Author authorEntryTransformer(Map<String, String> entry) {
        return new Author(
            entry.get("firstName"),
            entry.get("lastName"),
            entry.get("birthDate"));
    }

    @Given("a list of authors in a table")
    public void aListOfAuthorsInATable(List<Author> authors) {
        
    }
}
```

- **Specflow**:
  - Create simple class to model your specific object. Applying the attribute `TableAliases` if have properties in your objects that are known by different terms within the business domain

```
public class Employee
{
    public string FirstName { get; set; }
    public string MiddleName { get; set; }

    [TableAliases("Last[]?Name", "Family[]?Name")]
    public string Surname { get; set; }
}
```

  - Use `CreateInstance<T>` or `CreateSet<T>` convert a table in your scenario to a single/list instance of a specified class `table.CreateInstance<Person>()`
  
</details>

## Compare data source json, csv, excel
<details>
  
**CSV (Comma-Separated Values)**

- Pros:
  - Simplicity: storing data in a tabular format that’s easy to understand and manipulate.
  - Wide Compatibility: Supported by many tools
  - Lightweight: smaller file sizes, making them efficient for transferring large datasets.
- Cons:
  - Limited Structure: CSVs can only handle flat, two-dimensional data, making them unsuitable for complex or hierarchical datasets.
  - No Metadata: They lack built-in support for data types, units, or schema, requiring external documentation.
  - Error-Prone for Large Datasets: Handling large datasets in CSV can lead to issues with formatting and readability, especially when fields contain commas or line breaks.
 
**JSON (JavaScript Object Notation)**

- Pros:
  - Flexibility: JSON supports nested and hierarchical data, making it ideal for representing complex relationships.
  - Readability: Both human-readable and machine-readable
  - Popularity in APIs: JSON is widely used in modern APIs and web applications, ensuring seamless integration.
- Cons:
  - Larger File Sizes: compared to CSV or binary formats.
  - Parsing Overhead: Requires specialized libraries or tools for processing, which can introduce complexity.
  
**Excel (XLS/XLSX)**

- Pros:
  - User-Friendly: Designed for non-technical users, Excel files are easy to open, edit, and share.
  - Rich Features: Built-in tools for charts, formulas, and pivot tables make data exploration straightforward. Can manage multile data to one file using sheets
  - Widely Used: Familiarity across industries ensures compatibility with business workflows.
- Cons:
  - Limited Scalability: Excel struggles with very large datasets, with performance issues for files over a few hundred thousand rows.
  - Error-Prone: Manual editing can introduce errors, especially in collaborative environments, easy to make conflict
   
**XML/HTML**

- Pros:
  - Rich Metadata/Context: XML includes schema and attributes, making it highly descriptive and self-contained.
  - Interoperability: Widely supported across industries, especially in legacy systems.
  - Scalability: Handles complex and hierarchical data with ease.
- Cons:
  - Verbose Format: XML files tend to be large due to extensive tagging, leading to slower transmission and storage challenges.
  - Complex Parsing: Processing/parsing XML/HTML requires robust tools and expertise, increasing overhead.
   
</details>

## Data Management in Automation
<details>
  
1. Fixed data
- Store data separatedly for maintenance perspective as data may change in future and that should not affect our code and change data one place is applied everywhere, Data file based on specific purposes:
  - configuration in .properties
  - API URI
  - Enums for environments, browsers..

2. Generate unique prerequisite data through automation for each automation run, wherever possible

3. Test Data by environments
Most of the projects have multiple test environments(e.g. Dev, Test, Sandbox, etc.). if there are multiple test environments, split data into two categories:

- Common for all environments: Some data would be common to all environments
- Specific to a particular environment: Data that changes from environment to environment

4. Localisation

</details>

## Actions when automation failed a lot of case
<details>
  
- Identify the problem: check report (sceenshot, exception, logs)/debug to identify where to failed and reason
- Reproduce the failure: Try to manually reproduce the failure or rerun automation test. 
- Analyze causes and corresponding actions:
  - Application bugs => raise to development team to fix
  - Code Changes functionalities but automation haven't been updated yet => update automation scripts
  - UI Changes => update locators
  - Check for recent changes: See if there are any recent changes that could be causing the issue. => revert
  - Flaky tests (timeout by inconsistent env)
- Rerun the test: After making changes, rerun the test. 

Depending on the factor that affects your test reliability, you may need to apply different strategies for fixing failed tests: 

- For example, flaky tests can be fixed by isolating and eliminating the source of randomness or instability in your tests, such as using stable test data, mocking external dependencies, adding proper waits or retries, or simplifying your test logic.
- To fix test environment issues, you should ensure that your test environment is as similar as possible to your production environment and is stable and controlled. This can be done by using containers, virtual machines, or cloud services to create and manage your test environment and by using configuration management tools to automate and document your environment setup.
- To fix test data issues, you need to ensure that your test data is up-to-date, complete, and correct. This can be done by using data generators, data refreshers, or data sanitizers to create and maintain your test data and by using data validation tools to verify and monitor your data quality.
- Lastly, to fix test code issues you should make sure that your code is well-written, simple, and easy to maintain. This can be done by following coding standards, best practices, and design patterns as well as by using code quality tools to check and improve code readability, performance, and security.

</details>

## Strategy to manage the large number of test cases, for business or test results
<details>
  
</details>

## Implement a parser to detect incorrectly formatted data and correct it ?
<details>

we'll break the task into a few logical steps:

1. Read the data: We'll read the data line by line.
2. Identify formatting issues: Detect common issues like:
  - Incorrect number of columns in rows.
  - Quoted fields with misplaced quotes or extra commas.
  - Missing values in columns.
  - Values contains special characters
3. Correct the formatting: Attempt to fix common issues like:
  - Filling in missing values.
  - Balancing quotes and commas in quoted fields.
  - Normalizing row lengths to match the expected column count.
  - Remove/replace special characters

</details>


# PERFORMANCE QUESTIONS

## when execute performance test, how to determine the system throughput
<details>

To determine system throughput during a performance test, follow these steps:

- Define the appropriate throughput metric (RPS, TPS, etc.).
- Run the load test, simulating real-world traffic.
- Calculate throughput using the formula (Total Requests / Test Duration).
- Monitor system resources (CPU, memory, network) to identify potential bottlenecks.
- Assess throughput vs. latency to find the optimal balance. As the system handles more requests (higher throughput), the response time (latency) may increase, especially if the system approaches its capacity limits. Ideally, throughput should be high while maintaining acceptable latency levels.
- Adjust the test parameters and rerun the tests as needed.
- Analyze and report the results, identifying areas for improvement.
  
</details>

# BEHAVIOUR QUESTIONS

## Conflict resolution
<details>

- respecting diversity and individuality, 
- communicating openly and honestly with each other, 
- focusing on common goals and values, 
- seeking win-win solutions, 
- involving all relevant stakeholders in the decision-making process, 
- embracing change and feedback as opportunities for growth, and learning from the experience.
           
</details>


## Actions when adding new feature in the middle of sprint
<details>

Here’s a step-by-step guide on what you should do when this happens:

1. Assess the Request
  - Clarify the request: Ensure you understand the specifics of the new feature request. Is it a new priority feature, a change in scope, or a quick fix? Ask questions to get clarity.
  - Impact on current work: Evaluate how adding the new feature will affect the ongoing sprint. Does it conflict with existing priorities? Will it require significant resources or time?
  - Urgency: Determine the urgency of the new feature. Is it a critical feature for the sprint or is it something that can wait until the next sprint?
2. Check Sprint Capacity and Priorities
  - Review the sprint backlog: Look at the work your team has already committed to in the current sprint. Is the new request realistic to include without overloading the team?
  - Check team capacity: Evaluate if the team has enough capacity to handle the new request while still completing the planned work. Adding work mid-sprint may result in delays or quality issues if the team is stretched too thin.
  - Reprioritize if necessary: If the new feature is crucial, you may need to revisit the priorities. 
3. Communicate with the Product Owner
Transparent conversation: Have an open discussion with the PO or stakeholders about the impact of adding new work to the sprint. Explain the trade-offs and the consequences of changing the scope.
If the request is important but can’t be completed in the current sprint, suggest moving it to the next sprint or creating a backlog item for future work.

4. Determine the Best Course of Action
Depending on the context of the request and the impact, you have a few options to proceed:

  - Defer the request: If the new feature is not urgent and doesn’t align with the sprint goal, recommend deferring it to the next sprint. This keeps the current sprint stable and avoids overloading the team.
  - Re-prioritize the backlog: If the feature is urgent and critical, work with the PO to re-prioritize the backlog. You may need to remove lower-priority work to make room for the new feature.
  - Re-scope the sprint: If the team has the capacity and the new feature aligns with the sprint goal, you can adjust the scope by removing or deferring lower-priority items and adding the new feature.

**ACTIONS**

- Analyze and review the risks, deliverable items, testing timeline to development team
- Find out test approach and prioritize test efforts accoordingly. Like untilize automation for existing features and create test data, move automation efforts to manual test
- if changes cannot meet release date, open discussion to deal the release date
- if release is must, discuss the opportunity of increasing QA resources or possibility of partial product delivery

</details>

## PO/stackholders have an urgent milestone, they need the quick response about the quality of some features that can be deployed or not. We have UI, some API and datastorage. which testing you prefer?
<details>

Perform the one of Testing types with the opening Devtools to make sure application function to be smooth without any network or console errors:
- Smoke Testing: Perform high-level tests to ensure the most critical features are functioning correctly.
- Sanity Testing: After bug fixes or new feature development, run sanity checks to confirm that the issue has been resolved and the changes haven’t broken other parts of the application.
- Exploratory Testing: Allocate time for exploratory testing, where testers use their knowledge and creativity to identify high-impact issues, especially in areas that may not be fully automated.
- Boundary Value Testing: Focus on testing the boundaries (limits) of inputs, especially where validation is involved, as this is where many bugs often occur.
  
</details>

# PERSONAL QUESTIONS
## What are the main technical skills required for this position?
<details>

The main technical skills required for the Test Engineer position include proficiency in test automation tools such as Selenium and JUnit, strong knowledge of programming languages like Java and Python, and experience in writing test cases and test plans. Based on my previous role, I led the implementation of Selenium automated tests, reducing the test execution time by 40% and improving test coverage by 30%. Utilizing Java, I developed a testing framework that increased the team's productivity by identifying defects early in the development cycle.

Additionally, familiarity with continuous integration tools like Azure and version control systems such as Git is essential. In my previous position, I integrated automated tests into the pipeline, leading to a 50% reduction in the time taken for regression testing. By utilizing Git for version control, I established a streamlined process for tracking changes in test scripts and collaboratively working with team members, resulting in a 20% improvement in code quality. Overall, these technical skills enable me to effectively contribute to the testing process, ensuring high-quality software deliverables.

</details>

## Can you explain how your values align with those of our company?
<details>

My values align closely with company, especially when it comes to innovation and excellence. In my previous role as a Senior Software Test Engineer, I led a team in make sure quality of a software feature that improved system efficiency by 20%, resulting in a cost savings of $50,000 annually. This project exemplified my commitment to innovation, pushing boundaries to create solutions that drive impactful results.

Furthermore, I prioritize collaboration and continuous learning, which are key values at compay. I regularly attended and organized knowledge-sharing sessions within my team to foster a culture of learning and growth. For instance, implementing pair programming practices increased our team's productivity by 15% within 3 months. This aligns with company's emphasis on teamwork and development.

Overall, my track record of delivering innovative solutions, driving measurable results, and fostering a collaborative work environment showcases my alignment with company's values of innovation, excellence, and teamwork.
</details>


## What motivates you in terms of work?
<details>

What motivates me in terms of work is the opportunity to solve complex problems and make a tangible impact through innovative solutions. Throughout my career as a software test engineer, I have always been driven by the challenge of creating efficient and scalable automation test scripts. For example, in my previous role, I led a project to optimize the backend code, resulting in a 30% decrease in test effort and a 20% reduction in test coverage. This not only improved the overall quality of the system but also saved the team efforts.

I find great satisfaction in seeing the direct results of my efforts and knowing that I am contributing to the success of the team and the organization as a whole. As a Senior Software Test Engineer, I am excited about the opportunity to use my skills and experience to drive impactful projects, mentor junior team members, and constantly learn and grow in a dynamic environment. This sense of accomplishment and continuous learning is what fuels my passion for software engineering and motivates me to deliver high-quality work consistently.

</details>

## Can you describe your ideal coworker?
<details>

Here's how I'd describe my ideal coworker:

- Collaborative: Someone who thrives in a team environment, openly shares ideas, and is receptive to others' input. They understand the importance of communication and working together to achieve common goals.
- Problem-Solver: A person who is resourceful and approaches challenges with a positive attitude. Instead of getting stuck, they think critically, come up with creative solutions, and enjoy tackling tough problems.
- Adaptable: Flexible and open to change, whether it's shifting priorities, learning new tools or technologies, or adjusting to new workflows. They embrace challenges and adapt quickly to evolving circumstances.
- Accountable: Someone who takes ownership of their work, follows through on commitments, and takes responsibility for both successes and setbacks. They don’t shy away from admitting mistakes and work to improve.
- Detail-Oriented: A coworker who pays attention to the finer details, ensuring that things are done correctly the first time. Whether it’s testing code, reviewing documents, or managing projects, they understand that small things matter.
- Proactive: Rather than waiting for instructions, they anticipate what’s needed, take initiative, and drive projects forward. They don't hesitate to suggest improvements or find efficiencies in workflows.
- Supportive: They offer help to others when needed, whether it’s providing guidance, mentoring, or simply being a good listener. They’re a team player who wants to see others succeed as well.
- Continuous Learner: Someone who is always looking to improve and grow, whether through formal education, self-study, or learning from others. They actively seek out opportunities for professional development and stay curious.
- Respectful and Empathetic: They value others' perspectives, show empathy in all interactions, and maintain a respectful and positive attitude, even during stressful or challenging situations.
In short, my ideal coworker is someone who is dependable, communicative, and passionate about their work, but also someone who cares about others' growth and success as well.

</details>

## What was your most consequential mistake?
<details>



</details>
