# Tech Stack

## Language

- **Java** is the primary programming language.
- The project will use **Java 21** or the version required by the course.
- **JavaFX CSS** will style the desktop interface.

## Libraries and Tools

- **JavaFX:** Desktop user interface
- **Jackson:** Read and write JSON data
- **Java `HttpClient`:** Communicate with the AI API over HTTPS
- **JUnit 5:** Unit and integration testing
- **Mockito:** Mock the AI service during tests
- **Maven:** Build and dependency management
- **Git and GitHub:** Version control and project hosting

## Data Storage

The MVP will use local JSON files rather than a full database. The files will store projects, members, tasks, dependencies, progress updates, risks, and approved recommendations. Jackson will convert between JSON and Java objects. Sample data may be committed, but personal project data will be ignored by Git.

## External Data Source

The application will access an external language-model API through HTTPS. Java `HttpClient` will send a limited project summary, and Jackson will process the JSON response. The API will generate summaries and recommendations; regular Java code will calculate factual risks such as overdue or blocked tasks.

The API key will be stored in an environment variable and will not be committed to GitHub. If the API is unavailable, the rule-based features will remain usable and the application will report the connection problem.

## Technical Design Principles

- Java code determines project facts and risks.
- AI explains risks and suggests possible actions.
- Users approve recommendations before data changes.
- Storage and AI services are separated from the user interface so they can be tested independently.
