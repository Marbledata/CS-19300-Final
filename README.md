# AI-Powered Group Project Coordinator

A Java desktop application that helps student project managers organize team projects, identify risks, and receive AI-generated recommendations.

## Project Goal

The goal is to help student teams manage assignments, deadlines, blockers, and workloads in one place. Unlike a basic task tracker, the application detects project risks and uses AI to explain those risks and recommend practical next actions. The project manager remains responsible for approving all recommendations.

## MVP Scope

Version 1.0 will allow users to:

- Create projects and add team members
- Create, assign, update, and delete tasks
- Record deadlines, priorities, effort estimates, statuses, and dependencies
- Submit structured progress updates and blockers
- View project progress, overdue tasks, blockers, and team workloads
- Detect risks such as overdue, blocked, unassigned, or unevenly distributed work
- Generate AI project summaries and recommended next actions
- Approve or reject AI recommendations before changing project data
- Save project information locally in JSON files

## Future Plans

Possible Version 2.0 features include:

- Generate meeting agendas from current project risks
- Extract action items and decisions from meeting notes
- Send deadline and blocker notifications
- Suggest workload rebalancing between team members
- Display project-health trends over time
- Export project reports as PDF files
- Integrate with calendars and other project-management tools

## Tech Stack

- **Language:** Java 21, or the Java version required by the course
- **User interface:** JavaFX and JavaFX CSS
- **Build and dependency management:** Maven
- **Data storage:** Local JSON files
- **JSON processing:** Jackson
- **External requests:** Java `HttpClient`
- **AI service:** External language-model API accessed through HTTPS
- **Testing:** JUnit 5 and Mockito
- **Version control:** Git and GitHub

See [docs/Tech-Stack.md](docs/Tech-Stack.md) for more detail.

## Project Structure

```text
ai-project-coordinator/
├── README.md
├── .gitignore
├── docs/
│   ├── Eisenhower-Matrix.md
│   ├── System-Diagram.md
│   └── Tech-Stack.md
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
│       ├── java/
│       └── resources/
└── data/
    └── sample/
```

- `docs/` contains planning and design documents.
- `src/main/java/` will contain application code.
- `src/main/resources/` will contain JavaFX layouts, CSS, and configuration templates.
- `src/test/java/` will contain automated tests.
- `data/sample/` will contain non-sensitive demonstration data.
- Local user data and API keys will not be committed.

## Planned Git Milestones

1. Initialize the application and project structure
2. Implement project and team-member management
3. Implement task creation and progress tracking
4. Add task dependencies and project milestones
5. Create the project-management dashboard
6. Implement structured team progress updates
7. Build the rule-based project risk detector
8. Integrate the AI project-management coach
9. Finalize testing, error handling, and documentation

## Design Documents

- [Eisenhower Matrix](docs/Eisenhower-Matrix.md)
- [System Diagram](docs/System-Diagram.md)
- [Tech Stack](docs/Tech-Stack.md)

## Security

The AI API key will be read from an environment variable and will never be stored in the repository. Only project information required for a requested AI analysis will be sent to the external service.
