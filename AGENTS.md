```markdown
# AGENTS.md - Guidelines for AI Coding Agents

These guidelines are designed to ensure the creation of high-quality, maintainable, and effective AI coding agents. Adherence to these principles is mandatory for all development activities within this repository.

## 1. DRY (Don't Repeat Yourself)

*   All code should have a single, well-defined purpose.
*   Avoid duplicating logic or functionality across multiple files.
*   When a concept is reused, clearly document the reuse and potential variations.
*   Favor composition over inheritance whenever possible.

## 2. KISS (Keep It Simple, Stupid)

*   Strive for concise and easily understandable code.
*   Use the simplest solution that meets the current requirements.
*   Avoid overly complex logic or abstractions unless absolutely necessary.
*   Prioritize readability over unnecessary features.

## 3. SOLID Principles

*   **Single Responsibility Principle:** Each class/module should have one well-defined responsibility.
*   **Open/Closed Principle:**  The system should be extensible without modification.
*   **Liskov Substitution Principle:**  Subclasses should be substitutable for their base classes without altering the correctness of the system.
*   **Interface Segregation Principle:**  Clients should not be forced to depend on interfaces they don't use.
*   **Dependency Inversion Principle:**  High-level modules should not depend on low-level modules.

## 4. YAGNI (You Aren't Gonna Need It)

*   Only implement functionality that is currently required.
*   Avoid introducing features or complexities that are not currently needed.
*   Refactor existing code to remove unnecessary details.

## 5. Code Structure & File Management

*   Each file should have a single, focused responsibility.
*   Naming conventions will be strictly enforced:
    *   Classes: `[ClassName]` –  lowercase, with underscores for method names.
    *   Modules: `[ModuleName]` – followed by a single capital letter.
    *   Functions/Methods: `[FunctionName]` – follow a consistent format.
*   File size should be less than 180 lines of code.
*   Code should be well-formatted (indentation, spacing).
*   Include comments explaining complex logic or intent.
*   Use consistent error handling throughout the codebase.

## 6. Test Coverage - Production-Only

*   All tests are for *production* evaluation.
*   Tests should be designed to verify core functionality and edge cases.
*   Tests must be runnable without requiring external dependencies or external resources.
*   Test frameworks should be consistent across all modules.
*   Focus on unit tests for individual components and integration tests for system interactions.
*   Prioritize thorough testing of critical paths.

## 7. Code Complexity & Size

*   Code complexity should be managed to support maintainability.
*   Code should be easily understood and debugged.
*   Maintainability should be prioritized over raw code size.

## 8.  Specific Considerations for AI Agents

*   All agent logic should be encapsulated within classes and modules.
*   Utilize appropriate data structures for agent states and actions.
*   Consider incorporating logging for debugging and monitoring.
*   Implement clear separation of concerns between planning, execution, and evaluation phases.
*   Maintain data consistency and integrity throughout the agent's lifecycle.

## 9.  Example:  A Simple "Check Customer Status" Function

```python
class CustomerStatusChecker:
    def __init__(self, customer_id):
        self.customer_id = customer_id

    def check_status(self):
        # Simulate checking customer data
        print(f"Checking customer {self.customer_id} status...")
        print("Status: Unknown")
        return "Unknown"

# Example Usage (not part of the core agent logic but for illustration)
status = CustomerStatusChecker(123)
result = status.check_status()
print(f"Result: {result}")
```

## 10.  Reporting & Review Process

*   All code changes should be reviewed by at least one other developer.
*   Code should be documented with clear comments and docstrings.
*   Commit messages should concisely describe the changes and their purpose.
*   Regularly review code quality and adherence to guidelines.

## 11.  Tooling

*   Utilize a code formatter (e.g., black) for consistent code style.
*   Employ a linter (e.g., flake8) to catch potential errors.
*   Use a code style guide (e.g., Google Style Guide) to maintain readability.

These guidelines are a living document and will be updated as needed to ensure the continued quality and maintainability of the AGENTS.md repository.
```