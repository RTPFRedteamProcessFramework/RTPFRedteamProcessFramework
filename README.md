#Redteaming Process Framework: RTPF

![Uploading Screenshot 2024-08-08 at 9.37.08 PM.png…]()


1	Define the process - what are the distinct steps of the process? what are the beginning and end states?
2	Identify the key stakeholders - who are the key stakeholders in the process? who or what are the decision makers that allows each step to move forward?	
3	Identify inputs and outputs - similar to a web application where we talk about "source to sink", who and what is the process input, and what is the process output?
4	Identify impact - if a standard input is provided, what are the impacts of the different potential process outputs? What is the impact of a completed process?
5	Identify "trust boundaries" - similar to a system threat model, which parts of the process rely on others? Start with the process start, working your way to the process end, identifying each potential assumption that a step in the process makes about a prior step
6	Invent attack scenarios - begin asking "what if" questions about the different steps in the process and how you can craft an attack plan that exploits targeted or all steps in a process, and use the operational objective to shape this attack plan
7	Simulate your adversary - carry out the necessary system and social engineering actions to exploit the process and achieve your operational objectives

#Example: applying the framework to the employee transfer process

1	Define the process - Susan submits an employee transfer request for her employee Jim to Tom in HR - Tom validates that the target team has headcount using the Team Tracker tool and then verifies that Jim is a full-time employee - Tom then submits the transfer in the Transfer Helper tool and Susan confirms this when she receives an automated confirmation email
2	Identify the key stakeholders- The manager, the employee, HR, and the service teams that power the Team Tracker and Transfer Helper tools
3	Identify inputs and outputs - input is a Google form with all of the employee's information and the output is a successful employee transfer
4	Identify impact - transferring an employee changes the salary budgeting from one team to another and potentially gives an employee access to the resources of the other team
5	Identify "trust boundaries" - Tom in HR trusts that Susan submitted the form, and that this is a desired employee transfer. Jim trusts Susan to submit the transfer on his behalf. Tom trusts that the information displayed by the tools is accurate and that when they click transfer, the desired transfer will go through. Susan trusts that the confirmation email comes from the automated transfer tooling
6	Ask questions and plan - What if Susan submits a request about an employee who she doesn't manage? What if Jim submits a transfer for himself? What if an adversary submitted a transfer request instead of Susan? What if an adversary compromised the Team Tracker tool and Transfer Helper tool?
7	Simulate your adversary - social engineer Jim into changing the targeted employee that Susan submitted to a malicious contractor at the company, allowing the malicious contractor to be moved to a target team and gain access to their resources
