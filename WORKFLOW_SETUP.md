# GitHub Actions Workflow Setup

Your GitHub token needs the `workflow` scope to push GitHub Actions files.

## Option 1: Update Token (Recommended)
1. Go to https://github.com/settings/tokens
2. Find your current token or create new one
3. Add the `workflow` scope
4. Save new token and send to me

## Option 2: Manual Setup
1. Go to https://github.com/NikoClaws/video-renderer
2. Click "Actions" tab
3. Click "New workflow" → "set up a workflow yourself"
4. Paste the workflow from workflow-content.yml
5. Commit

The workflow file content is saved in workflow-content.yml
