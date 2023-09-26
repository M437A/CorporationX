#CorporationX

Repository for the entire project. Uses git submodule to enable all other services

# How to get started?

`git clone --recurse-submodules https://github.com/CorporationX/CorporationX`

# How to raise the database and other tools locally?

Follow the instructions in the README in the `infra` section. This is a separate repository that contains all infrastructure components (DB, Redis, Docker Compose, etc.)

# How to develop?

Each folder in this repository is a separate subrepository, which is also on GitHub. Those. user_service is a regular Git repository that is simply included in the larger CorporationX repository as a subrepository

The CorporationX repository exists only for convenience: you can immediately clone all the necessary services with just one command `git clone`, which is indicated above.

Each subrepository represents a separate service (Java application) in the CorporationX ecosystem. For example, user_service is an application that contains the logic for working with users, project_service is the logic for working with projects, etc.
Accordingly, depending on the specific task, you will work in either one or another service. Basically, just write code there, as in a regular project in IDEA.

That's why:
1. Download the entire CorporationX project using the clone command above
2. From a specific task in Jira, we determine which service needs to be developed in.
3. Open the folder with this service in IDEA
4. Let's work!
5. 
# Tests

Each PR in this repository must contain unit tests for all your logic. PRs without unit tests will be sent straight back to work without partial verification. When the team adds CI pipelines to GitHub, PRs with failed tests will also be immediately sent back to work without partial verification.

Your PR must be completely green and covered in tests to get a review. This is a mandatory requirement.
