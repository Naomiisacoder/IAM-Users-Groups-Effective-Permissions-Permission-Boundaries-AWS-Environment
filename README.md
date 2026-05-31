# IAM-Users-Groups-Effective-Permissions-Permission-Boundaries-AWS-Environment
AWS IAM Core Permissions Lab — Hands-on walkthrough of IAM users, groups, inline policies, explicit deny rules, and permission boundaries using alice-ops, bob-ops, and charlie-ops test identities in a live AWS environment.

AWS IAM Core Permissions Lab
A hands-on AWS Identity and Access Management (IAM) lab exploring how effective permissions work in a real AWS environment — including group policies, inline policies, explicit deny rules, and permission boundaries.
________________________________________
 What's in This Repo
File	Description
AWS_IAMCore_Permissions_Lab.pdf	Full lab report with console screenshots and observation checkpoints
________________________________________
 What the Lab Covers
This lab walks through IAM permission behavior using three test users — alice-ops, bob-ops, and charlie-ops — each configured differently to demonstrate core IAM concepts.
Key Concepts Demonstrated
•	Group policies vs. inline policies — how they interact and which takes precedence
•	Implicit deny vs. explicit deny — why the absence of a permission behaves differently from an active block
•	Explicit Deny always wins — a Deny on a group policy overrides a personal Allow, no matter what
•	Permission Boundaries — how they act as a hard ceiling that identity policies cannot break through
•	Effective permissions formula — an action is only allowed if permitted by both the identity policy and the boundary
________________________________________ Test User Scenarios
User	Setup	Key Lesson
alice-ops	Group read policy + personal inline policy	Explicit group Deny overrides personal Allow
bob-ops	Action: * identity policy + S3-only boundary	A boundary neutralizes even admin-level policies
charlie-ops	Group policy only, no inline policy	Clean baseline — group inheritance only
________________________________________
Core IAM Rules (TL;DR)
1.	Default deny — everything is blocked unless explicitly allowed.
2.	Explicit Deny wins — always overrides any Allow, from any source.
3.	Implicit deny can be overridden — an Allow elsewhere is enough.
4.	Effective permissions = identity policy ∩ permission boundary — both must allow an action for it to succeed.
________________________________________
AWS Services Used
•	AWS IAM (Users, Groups, Inline Policies, Permission Boundaries)
•	Amazon S3
•	Amazon EC2
________________________________________
Who This Is For
Cloud security learners, AWS certification candidates, or anyone building an understanding of IAM policy evaluation logic from real console behavior.
________________________________________
 License
This lab report is for educational purposes.


