# cc-codepipeline-static-site
Static website deployed to S3 using AWS CodePipeline (CI/CD)

# Static Website CI/CD with AWS CodePipeline + S3

## Objective
Deploy a static website to Amazon S3 using AWS CodePipeline, triggered automatically by GitHub commits.

## Services Used
- GitHub (Source Repository)
- AWS CodePipeline (CI/CD)
- Amazon S3 (Static Website Hosting + Deploy Target)

## Architecture
GitHub Repo + CodePipeline + S3 Static Website Bucket

## Steps Completed
1. Created a GitHub repository and uploaded the provided HTML (`index.html`)
2. Created an S3 bucket configured for static website hosting
3. Created an AWS CodePipeline pipeline
4. Configured GitHub as the Source stage (GitHub via GitHub App connection)
5. Configured S3 as the Deploy stage target
6. Deployed the pipeline and verified the website is reachable
7. Updated the HTML file to confirm the pipeline triggers automatically and redeploys

## Deployment Details
- **S3 Website Bucket:** cc-static-site-coffeecloud-2026
- **Region:** us-east-1
- Webste verification: http://cc-static-site-coffeecloud-2026.s3-website-us-east-1.amazonaws.com (deleted upon completion)

## How to Verify
1. Open the S3 website endpoint in your browser.
2. Edit `index.html` in GitHub (example: add `!!!` to the text).
3. Commit and push to the `main` branch.
4. Confirm CodePipeline runs automatically and succeeds.
5. Refresh the website and confirm the update is visible.

## Result
The static website successfully deploys to S3 and updates automatically on every push to the repository.
