# Group-Assignment-3

Group members & module assignments
Module 1 - Ling Hua Rong 24004492

Module 2 - Wong Pei Rou 24004549

Module 3 - Lew Zhi Xin 24004612

Module 4 - Nam Ke Ni 24004525

Module 5 - Tai Wen Xuan 24004565, Zhang Lingran 22111128

Description of each module’s functionality
Module 1:
This module implements a Binary Search Tree (BST) to manage student records. Each node stores student data: matric ID, name, structured address (street, city, district, state, postcode), programme, CGPA, and a unique userID generated via UUID. The BST supports insert, delete, search, and in-order traversal operations, and each node also tracks the size of its subtree to enable recursive queries. This design ensures efficient data storage and average-case O(log n) performance for core operations.

Module 2:
This module provides multiple search capabilities for student records. It allows users to search by exact matric ID, full name, partial name (prefix match), programme, and address fields like state or district. It also supports range searches based on CGPA values (e.g., between 3.00 and 4.00). These features enable fast, flexible querying across various student attributes.

Module 3:
This module implements two sorting algorithms—Bubble Sort and Merge Sort—to sort student records based on selected fields: matric ID, name, programme, CGPA, or parts of the address (state, district, postcode). Users can choose one or more fields and specify ascending or descending order for each. The module also compares the performance (execution time) of both sorting algorithms to illustrate efficiency differences in practice.

Module 4:
This module uses recursion to compute statistical insights from the student data. It calculates the total number of students, counts of students by programme and state, number of students within a CGPA range, and the average CGPA by programme or state. It also computes the height of the BST and the balance factor of any node, demonstrating understanding of recursive tree operations.

Module 5:
This module integrates all system features through a text-based menu. It loads student data from a CSV file at startup and saves updated records to a new CSV on exit. The module includes input validation (e.g., checking for duplicate records) and provides a basic undo feature using a stack to reverse the last insert or delete operation. It ensures all modules work together smoothly and manages user interaction with the system.

Challenges faced and how ChatGPT helped resolve them
Module 1:
Each node is not just a value, but a full student profile, including:
- Matric ID, Name
- Granular address fields (Street, City, State, District, Postcode)
- Programme, CGPA
- Auto-generated UUID
- subtreeSize for efficient counting
ChatGPT tells me to define a custom Student class or a detailed BSTNode class to encapsulate this.

Module 2:
Names are not unique and not used as the BST key → cannot use BST lookup.
ChatGPT tells me to traverse entire tree (O(n)) and compare names case-insensitively or trimmed.

Module 3:
Each record contains multiple fields:
Simple fields: Matric ID, Name, Programme, CGPA
Nested/Structured fields: Address with subfields (State, District, Postcode)
ChatGPT tells me to extract and compare nested fields from the Address object and require custom comparator functions.

Module 4:
Base case and recursion control must be carefully defined.
Risk of stack overflow if the student array/list is large and tail recursion is not optimized.

Module 5:
Parsing CSV correctly (e.g., handling commas in fields, quoted strings).
Mapping CSV fields to object properties (e.g., Address as a nested structure).
Handling empty or malformed rows.
Avoiding duplicate loading if multiple file imports are allowed.
