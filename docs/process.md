# Section 1

**(a) The Model: Incremental Process with Agile Practices**
For our Text Classification & Summarization Service, we will follow an **Incremental** model driven by Agile iterations (Scrum-based). A single cycle (a two-week sprint) runs as follows: 
First, the team selects a subset of features from the backlog (e.g., basic summarization API without queues, or adding RabbitMQ/Redis for asynchronous processing). The tasks are assigned to members handling frontend, backend, or ML ops. During development, developers integrate the NLP model, wrap it in an API, and build the corresponding UI. The cycle ends with a testing phase focusing specifically on AI output stability (verifying summaries are accurate and not hallucinated) and system load. The deliverable at the end of each cycle is a working, deployable version of the service with increasing capabilities.

**(b) The Position: ~80% Agile with 20% Plan-Driven Gates**
Our process sits closer to the Agile end of the spectrum, but heavily incorporates plan-driven milestones dictated by the academic environment. We position ourselves at **80% Agile / 20% Plan-driven**. 
* **Plan-driven elements (Frozen for the semester):** The core technology stack (e.g., Python/FastAPI for ML serving, the specific message queue infrastructure), system architecture, and the four hard deadlines set by the instructor are fixed. 
* **Agile elements (Re-opened every cycle):** The specific LLM/NLP models used, prompt engineering techniques, the queue processing logic (e.g., timeout handling, retry mechanisms), and UI components are continuously refined based on testing feedback. Since AI output is inherently non-deterministic, we must remain agile to adjust our serving strategy if the model proves too slow or inaccurate.

# Section 2

## Q1 Are your requirements stable or volatile? What evidence do you have?

Our requirements are highly volatile. In AI-driven applications like text classification and summarization, stakeholders rarely know the exact output quality, summarization length, or specific taxonomy they need upfront. Our evidence comes from initial discovery workshops, where feature requests and acceptance criteria frequently shifted as soon as stakeholders interacted with early mockups and baseline model outputs.

## Q2 Does the project carry safety or legal impact that would demand formal documentation and change control?

This project carries minimal safety or legal impact. A misclassified document or an imperfect text summary does not pose physical harm, life-threatening risks, or severe compliance violations. Therefore, the heavy, plan-driven documentation and strict change-control procedures required in highly regulated industries (like healthcare or aviation) are unnecessary, allowing us to prioritize rapid feature delivery.

## Q3 Is your team large and distributed, or small and co-located? How does that affect communication cost?

Our team is small and co-located, consisting of four members. Because we study on the same university and collaborate closely, our communication overhead is extremely low. This close proximity allows us to bypass heavy documentation for internal alignment, making agile practices like quick continuous syncs and immediate peer code reviews highly efficient.

## Q4 Can your customer (the instructor, plus any real users you consult) engage continuously, or only at fixed checkpoints?

Our primary user is our instructor, who is available to provide direct, active feedback on a weekly basis during class sessions. This continuous engagement is ideal for an incremental approach, as it allows us to demonstrate small, working pieces of the web app and immediately incorporate the instructor's feedback into the next development cycle rather than waiting until the end of the semester.

## Q5 What do organizational culture and contract constraints allow? For this course: the four fixed milestones and the final demo date.

While we operate with a flexible, agile mindset internally, our academic environment imposes strict structural boundaries via the four fixed course milestones and the final demo date. To balance these constraints, our process operates as a hybrid: we execute our coding and model integration in short, adaptable iterations, but we align our major feature freezes and milestone deliverables strictly with the instructor's plan-driven deadlines.

# Section 3
