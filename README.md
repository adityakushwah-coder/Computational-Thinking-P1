# Computational Thinking - P1

 Task 1: Identity Investigation

Objective:
To understand how memory locations (IDs) change when variables are modified.

Action Performed:
A file named `identity_[yourfirstname].py` was created. Different data types (integer, string, list, tuple) were modified, and their memory IDs were printed before and after using the `id()` function.

Observation:
- Integer → ID changes  
- String → ID changes  
- Tuple → ID changes  
- List → ID remains the same  

Conclusion:
Integers, strings, and tuples are immutable, so new memory is created when they are changed. Lists are mutable, so they are modified in the same memory location.

Task 2: Nature of Commit History

Action Performed:
A repository was created and a file `identity_[yourfirstname].py` was added. Changes were made and committed with messages like "Version 1" and "Version 2".
Question:
Does "Version 2" still exist in the folder?

Answer:
Yes, "Version 2" still exists. Both Version 1 and Version 2 are saved in Git history.
Explanation:
Git follows an immutable storage model, meaning commits cannot be changed once created. Instead of modifying old commits, Git creates new ones for every change.

Conclusion:
All versions are preserved in Git, proving that commits are immutable.

Task 3: Shallow Copy Behavior

Action Performed:
A nested list was created and copied using `list()`. Then an inner value in the copied list was modified.

Observation:
The original list also changed.

 Explanation:
The copy created was a shallow copy, where inner lists still refer to the same memory. So, modifying one affects the other.
 Conclusion:
Deep copy should be used to create completely independent copies.


Task 4: Commit Immutability

Action Performed:
A file `data.py` was committed and its hash was recorded. The commit message was then changed using `git commit --amend`, and the new hash was observed.

Observation:
The commit hash changed after modifying the message.
 Explanation:
A commit hash depends on content, message, and metadata. Changing any of these creates a new commit with a new hash.

 Conclusion:
This shows that Git commits are immutable and cannot be edited once created.