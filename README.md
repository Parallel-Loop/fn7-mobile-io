# Guide to Creating a New Platform on GitHub

This comprehensive guide is designed to walk you through the process of creating a new platform using an existing Git project. It outlines a series of manual steps that involve branch creation, file modification, Firebase, Auth0 configuration, and more. Each step is detailed with corresponding images to ensure clarity and ease of understanding.

## Platform Creation

Creating a new platform involves several important steps. Here's a step-by-step guide to ensure a smooth process.

### 1. Create a New Branch

**Task**: Create a new branch from the `dev/deskhub` branch.  
**Files to Modify**:  
- `root_project/lib/app_config.dart`  
- `root_project/config.json`

Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")
Details: Start by creating a new branch. This will be your workspace for making necessary changes without affecting the main codebase.
### 2. Update AppConfig File

**File**: - `root_project/lib/app_config.dart`

Image: 
Details: Modify the `app_config.dart` file with platform-specific details like theme, URLs, and metadata creation rules. Commit these changes.
### 3. Configure Config.json

**File**: - `root_project/config.json`
Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")
Details: Provide necessary information in the config.json file but hold off on committing these changes.
### 4. Add App Icon

**Path**: `root_project/assets/images/`
Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")
Details: Add app_icon.png to the specified path and update config.json with the file name. Do not commit these changes yet.
### 5. Firebase Setup

**Tasks**:
Add an Android app in the Firebase console.
Download `google-services.json`.
Update `config.json` with the AppId.
Convert `google-services.json` to **base64** and update the GitHub secret.
Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")
Details: In Firebase, add your app and get the necessary configuration files. Update your project with these details.
### 6. Auth0 Configuration

**Tasks**:
Add new package name as redirect URLs in Auth0 dashboard.
Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")
Details: Configure Auth0 by adding your new package name as the redirect and logout redirect URLs.
### 7. Finalize Config.json and Create PR

**Task**: Commit changes to config.json in a new branch and create a Pull Request.
Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")
Details: Once all configurations are done, commit your final changes to config.json, create a new branch, and open a Pull Request.
### 8. Build and Test

**Task**: Add the label DeliverToTesters to the PR.

Image: ![Alt text](s3platform_ec.europa.eu.jpg?raw=true "Optional Title")

Details: Trigger a workflow that builds the new app. Testers will receive an invite via email to test the app.
