# Google Summer of Code 2024 Final Report

## **Project**: [Automated Regression Testing Tool for Checkstyle](https://github.com/checkstyle/checkstyle/wiki/Checkstyle-GSoC-2024-Project-Ideas#project-name-internal-tooling-for-regression-testing)

## **Student**: [Piyush Kumar Sadangi](https://github.com/relentless-pursuit)**

## **Organisation**: [Checkstyle](https://github.com/checkstyle)

## **Mentor**: [Roman Ivanov](https://github.com/romani)

---
### Project Goals

The goal of my Google Summer of Code project was to modernize Checkstyle's regression-testing and reporting capabilities by creating and improving several key components:

1. **Extractor Application** – a Gradle-based tool for extracting Checkstyle module configurations and documentation, facilitating the generation of configuration files for various checks.
   
2. **DiffTool.java** – a fully rewritten Java tool that replaces the older `diff.groovy`, providing improved maintainability and better predictability, while moving away from scripting languages like Groovy.

3. **Workflows** – a new GitHub Actions workflow (`regression-report.yml`) for Checkstyle, which automates the generation of regression reports, adding user-friendly functionalities and improving ease of use.

4. **CI/CD Pipelines** – Implemented CI/CD pipelines for the newly created `checkstyle/test-configs` repository, ensuring automated builds, testing, and report generation for continuous integration and delivery.

5. **Code Quality Enforcement** – Ensured adherence to basic code standards provided by tools like PMD, Checkstyle, and SpotBugs, enforcing best practices and maintaining code quality across all developed components.


---

### What I Did During GSoC

1. **Scratch-pad development in checkstyle/test-configs**:
   - Designed and implemented a Gradle application from scratch that automates the extraction of Checkstyle configurations and example inputs.
   - This application serializes configurations and automatically generates README files, enhancing both testability and documentation within the Checkstyle project.

2. **Conversion of `diff.groovy` into `DiffTool.java`**:
   - Translated the complex logic of `diff.groovy` into a more maintainable and structured Java program (`DiffTool.java`).
   - Improved error handling, command-line interface, and integration with Checkstyle's regression testing workflow.

3. **GitHub Actions Workflow (`regression-report.yml`)**:
   - Created a GitHub Actions workflow to automate regression testing when pull requests are made.
   - Integrated AWS S3 for report uploads, configured caching mechanisms, and optimized the workflow for large-scale testing.
   
4. **Code Contributions to Checkstyle**:
   - Contributed several updates to the Checkstyle repositories (`checkstyle/test-config` and `checkstyle/checkstyle`) to align with these new tools and improve overall functionality.

---

### Code Contributions

Below is a summary of the contributions I made as part of my Google Summer of Code project with Checkstyle:

- **All Pull Requests (PRs) related to the `checkstyle/test-config`** can be found [here](https://github.com/checkstyle/test-configs/pulls?q=is%3Apr+is%3Amerged+author%3Arelentless-pursuit+created%3A%3E%3D2024-05-01+merged%3A%3C%3D2024-10-16).
- **All Pull Requests (PRs) related to the `checkstyle/checkstyle`** can be found [here](https://github.com/checkstyle/checkstyle/pulls?q=is%3Apr+is%3Amerged+author%3Arelentless-pursuit+created%3A%3E%3D2024-05-01+merged%3A%3C%3D2024-10-16).
- **All Issues associated with the project** are tracked on the **[GitHub project board](https://github.com/orgs/checkstyle/projects/8)**.

---

### Skills Acquired

During the project, I gained several technical skills:
- **Java**, **Groovy**, **Bash**, **Gradle**: Deepened my understanding of these technologies while working on the conversion and development of tools.
- **GitHub Actions**: Implemented and optimized CI/CD workflows for testing and regression reporting.
- **Code Quality Tools**: Worked extensively with tools like Checkstyle, PMD, and SpotBugs, learning how they enforce coding standards, prevent bugs, and ensure code consistency
  
---

### Current Status and Future Work

The project is almost complete, with the tools in a stable state, integrated into Checkstyle’s workflow. The next steps include:
- Addressing regression-testing failure of some checks
- Integrating projects.yml feature into regression-report.yml
- Improving code quality to the highest standards, the final polishing of DiffTool and Extractor.

---

### What I Learned

Throughout GSoC, I gained a deeper understanding of several key aspects of software development:

1. **Collaboration and Communication**: One of the most valuable lessons I learned was how to collaborate effectively with mentors and the wider open-source community. As we worked asynchronously across different time zones, I improved my ability to communicate clearly, both in terms of asking questions and providing updates. This ensured that the project moved forward smoothly and that feedback loops were efficient.

2. **Brainstorming and Designing an Application**: A significant portion of this project involved not just coding, but also brainstorming and designing the architecture for the `Extractor` and `DiffTool`. I learned how to break down complex requirements into smaller, manageable tasks, and how to architect a solution that balanced flexibility with maintainability. This experience honed my ability to think critically about design decisions and to weigh trade-offs between different approaches.

3. **Code Quality and Best Practices**: Working on a widely used tool like Checkstyle made me realize the importance of adhering to strict code quality standards. I gained hands-on experience with code quality tools such as Checkstyle, PMD, and SpotBugs, learning how they can enforce good coding practices, detect bugs early, and ensure consistency across the codebase. These tools helped ensure that the new Java applications (`Extractor` and `DiffTool`) met high standards of quality, readability, and maintainability.

4. **Working with Deadlines**: Contributing to GSoC taught me how to work with deadlines and prioritize tasks effectively. I learned how to break down a long-term goal into smaller milestones and ensure that I made steady progress each week. This skill of time management will be invaluable in future projects, both in open-source and industry.

5. **CI/CD Pipelines**: A critical part of this project involved setting up continuous integration and continuous deployment (CI/CD) pipelines for `checkstyle/test-config` and automating workflows. I learned why CI/CD pipelines are essential—ensuring that code changes are tested, validated, and deployed consistently and efficiently. Writing these pipelines not only reduced manual effort but also minimized errors, ensuring that regression tests ran automatically and reported results reliably.

6. **Optimizing GitHub Actions for Large-Scale Testing**: As part of my work on the GitHub Actions workflow (`regression-report.yml`), I gained experience in optimizing CI workflows for large-scale testing scenarios. This included configuring caching mechanisms to speed up builds, integrating AWS S3 for storing large test reports, and handling edge cases that might occur during regression tests.

These experiences gave me a comprehensive understanding of building, testing, and maintaining high-quality software, preparing me for future endeavors in both open-source and professional projects.

---

### Acknowledgments

I’d like to express my gratitude to my mentors, Roman Ivanov, for their invaluable guidance. A special thanks to the Checkstyle community for their support throughout the summer. I look forward to continuing my contributions to Checkstyle and applying what I’ve learned to future projects.

--- 
