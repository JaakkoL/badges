# badges
> Testing code coverage badge creation via GH Actions

![Coverage](https://raw.githubusercontent.com/JaakkoL/badges/refs/heads/badges/coverage.svg)

## Instructions

This project demonstrates how to automatically generate a code coverage badge using GitHub Actions and store it in a dedicated branch (`badges`). The badge image (`coverage.svg`) is then referenced directly in the README.

### How it works

1. **CI Workflow**: On each push to main branch, GitHub Actions runs your tests and generates a coverage report.
2. **Badge Generation**: The workflow creates or updates a `coverage.svg` badge based on the latest coverage results.
3. **Badge Storage**: The badge is committed to the `badges` branch, which is a protected, long-lived branch.
4. **Badge Reference**: The README links to the badge image in the `badges` branch using a raw GitHub URL.

### Notes

- This method works for public repositories. For private repositories, the badge image will not be accessible without an access token, which is typically short-lived and not suitable for embedding in a public README.
- As an alternative, you could use GitHub Pages to host the badge image, which would work for both public and private repositories (with appropriate access controls).
