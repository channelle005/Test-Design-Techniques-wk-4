# Test-Design-Techniques-wk-4

📚 Assignment Questions
1. What is black-box testing, and how does it differ from white-box testing?

   Black-box testing is a software testing method that focuses on testing the functionality of an application without knowing the internal code or structure. Testers provide inputs and observe outputs to verify that the system behaves as expected.

Difference from white-box testing:

| Aspect            | Black-Box Testing                       | White-Box Testing                    |
| ----------------- | --------------------------------------- | ------------------------------------ |
| Knowledge of Code | No knowledge of internal code required  | Requires full knowledge of code      |
| Focus             | Functional behavior                     | Internal logic, structure, and flow  |
| Tester Role       | Performed by QA/testers                 | Often done by developers             |
| Example           | Testing login with valid/invalid inputs | Testing how loops or conditions work |

2. Explain the concept of equivalence partitioning and how it helps in reducing test cases.

Equivalence partitioning is a black-box testing technique where input data is divided into valid and invalid partitions (groups) that are treated as equivalent. The idea is that if one test case from a partition passes, all others in that partition will too.

How it reduces test cases:

Instead of testing every possible input, you test one representative value from each group.

This reduces redundancy and saves time while maintaining test effectiveness.

Example:
For an input field that accepts ages from 18 to 60:

Valid partition: 18–60 → test with 30

Invalid partitions: <18 (e.g., 15), >60 (e.g., 65)
   
3. What is boundary value analysis, and why is it useful in software testing?

   Boundary Value Analysis (BVA) focuses on testing the values at the edge or boundary of input ranges, as errors often occur at these points.

Why it’s useful:

Helps uncover defects that occur at the edges of input domains.

Complements equivalence partitioning by targeting edge cases.

Example:
For an input range 1–100:

Test values: 0, 1, 100, 101 (just outside and inside boundaries)

4. Describe the purpose of decision tables in black-box testing and provide an example scenario where they might be used.

   Decision tables are a structured way of modeling complex business logic or rules by listing possible conditions and actions. They help ensure that all combinations of inputs and their corresponding outputs are tested.

Purpose:

Ensure full coverage of combinations

Clarify complex decision-making logic

Reduce human error in test design

Example Scenario:
Online discount system:

| Condition: Member | Condition: Purchase > \$100 | Action: Apply Discount |
| ----------------- | --------------------------- | ---------------------- |
| No                | No                          | No                     |
| No                | Yes                         | Yes                    |
| Yes               | No                          | Yes                    |
| Yes               | Yes                         | Yes                    |

5. What is state transition testing, and how can it be applied to a user account system

   State Transition Testing is a technique where changes in input cause changes in the system's state. It tests valid and invalid transitions between states.

Application to a User Account System:

Imagine a user account with these states:

Registered → Activated → Logged In → Logged Out → Deactivated

Transitions to test:

Registered → Activated (after email verification)

Activated → Logged In (after successful login)

Logged In → Logged Out (after logout action)

Activated → Deactivated (by admin or user request)

Invalid: Logged Out → Logged In (without activation)

Why it’s useful:

Ensures the system handles correct state flows and prevents invalid transitions, such as logging in before activation.
