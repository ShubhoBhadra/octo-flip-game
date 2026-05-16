# Add to do here.
# TODO_ID: 1
1. Title: 🚀 Implement Dynamic Build Numbering for Feature Branches and Main
Summary:
We need to implement an automated versioning system that distinguishes between development builds and production-ready builds. The versioning logic should branch based on the target environment:

A.1. Non-Main Branches
Triggered on every push or pull_request to any branch except main..

Format: Major-alpha.<build_number/github.run_number>

Example: 1-alpha.1, 1-alpha.2

Logic: The -alpha suffix tells everyone that this is a work-in-progress. The <build_number/github.run_number> should increment every time a developer pushes code to their feature branch.

A.2. Main Branch
Triggered when changes are merged into or pushed directly to the main branch.

Format: Major-main.<build_number/github.run_number>

Example: 1-main.1, 1-main.45

Logic: This is the "Stable" version. By removing the -alpha tag, you signal that this build has passed code review and is ready for deployment.

# TODO_ID: 2
2. Title: 🚀 Automate Synchronization of TODO Number and TODO_ID in TODO.md file.

Summary:
Ensure that every task added to the TODO.md file maintains a strict 1-to-1 relationship between its "Generated TODO Number: *****" and its unique identifier (TODO_ID). This will prevent ID mismatches when tasks are reordered

For Generated TODO Number reference https://github.com/ShubhoBhadra/octo-flip-game/actions/runs/25885028863