CS 255 System Analysis and Design — Portfolio README
Jonathan Pineset | Southern New Hampshire University | April 27, 2026

PROJECT SUMMARY: THE DRIVERPASS SYSTEM

The client for this project was Liam, the founder of DriverPass, a startup company that identified a significant gap in how students prepare for their DMV driving test. Research showed that more than 65 percent of students fail their driving exam, largely because they depend on studying previous tests without receiving real structured training. Liam wanted a system that would change that by combining online practice exams, in-person lesson scheduling, and on-the-road training into a single web-based platform accessible from any internet-connected device.

The system I was asked to design needed to serve multiple user types: customers, secretaries, drivers, administrators, and an IT officer - each with different access levels and responsibilities. On the customer side, the system needed to support account registration, package selection, lesson scheduling, online testing, and progress tracking. On the administrative side, it needed to handle reservation management, activity reporting, DMV update integration, and role-based access control. The entire system was to be hosted on a cloud platform to eliminate the need for local server management and ensure 24/7 availability.

WHAT I DID PARTICULARLY WELL

The area where I performed strongest was translating the client’s spoken requirements into structured, actionable system documentation. During the requirements gathering phase, the client expressed needs conversationally, talking about wanting customers to be able to schedule lessons, wanting staff to track who changed what, and wanting the system to stay current with DMV updates. Converting those conversations into clear functional and nonfunctional requirements in the Business Requirements Document required careful interpretation, and I feel I captured the intent accurately.

In the System Design Document, I also did well with the class diagram. Identifying that Customer, Driver, Staff, and Administrator all inherit from a base User class made the data model cleaner and more maintainable. That structural decision reduced redundancy across the model and directly reflected how the system’s role-based access control would work in practice. Inheritance was not just a UML choice, it was a design decision that made the security model simpler to implement.

WHAT I WOULD REVISE

If I could revise one part of my work, it would be the activity diagrams. The two diagrams I created (Schedule Driving Lesson Reservation and Take Practice Test) captured the primary workflows correctly, but they did not go deep enough on the error and exception paths. For example, what happens if a customer’s payment fails during registration? What happens if a scheduled driver becomes unavailable after a reservation is confirmed? Those edge cases exist in the real system and belong in the diagrams. A more complete activity diagram anticipates failure states and shows how the system recovers, not just what happens when everything works correctly.

Improving this would require going back to the interview transcript and specifically identifying every conditional mentioned by the client or the IT officer, then mapping each one to a decision node with both a success and failure path. That level of thoroughness would make the diagrams significantly more useful as a handoff document for a development team.

HOW I INTERPRETED AND IMPLEMENTED USER NEEDS

My approach to interpreting user needs started with the interview transcript. Rather than treating it as a list of features, I read it as a picture of pain points. Liam was not asking for a scheduling system because he liked technology,  he was asking because students were failing their driving tests and he believed better preparation tools would change that outcome. Keeping that goal at the center helped me prioritize the requirements that mattered most: online practice tests that track progress, lesson scheduling that could be done without calling anyone, and reporting tools that gave administrators visibility into how the system was being used.

Considering user needs during system design is not optional. It is the entire point of the work. A system that is technically functional but designed around what is easy to build rather than what users actually need will fail in practice, even if it passes every test. The DriverPass customer is not a technical user. They are a student who wants to pass their driving test. If the scheduling process is confusing, they will not use it. If the test progress dashboard does not clearly show where they stand, it provides no value. Every design decision has to trace back to whether it makes the system easier and more useful for the person who will actually interact with it.

MY APPROACH TO DESIGNING SOFTWARE

My approach to system design follows a consistent sequence: understand the problem before designing the solution, document requirements before drawing diagrams, and validate design decisions against the original user needs before finalizing anything. For DriverPass, this meant starting with the Business Requirements Document and making sure every requirement was grounded in something the client actually said before moving to the UML work in Project Two.

Going forward, the techniques I would continue using are use case analysis to identify all actors and their interactions early, class diagrams to establish the data model before any interface design begins, and sequence diagrams to verify that the object interactions I have designed actually support the workflows I mapped in the activity diagrams. These are not just documentation tools, they are thinking tools. Drawing a sequence diagram forces you to answer questions about the system that you might not have thought to ask otherwise, like exactly what happens between the moment a user clicks Book Lesson and the moment a confirmation appears on screen.

The strategy I would add in future projects is earlier stakeholder validation. For DriverPass, I worked from the interview transcript, but in a real project I would build in a formal review checkpoint after requirements gathering where the client confirms that the documented requirements reflect their actual intent before any design work begins. Catching a misunderstood requirement at the documentation stage costs almost nothing. Catching it after the system is built can cost everything.
