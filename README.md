# attach-dir-to-jira-issue-action
GitHub action for attaching a directory to an existing Jira issue.

Attach-Dir-To-Jira-Issue Action
This GitHub Action allows you to attach a directory (as a ZIP file) to a Jira issue. You can use this action to easily attach logs, reports or any other files to your Jira issue.

## Inputs
 - jira-base-url: Required The base URL of your Jira instance.
 - jira-user-email: Required The email address of the Jira user to use for the attachment.
 - jira-api-token: Required The API token for the Jira user to use for the attachment.
 - jira-issue-id: Required The ID of the Jira issue to attach the directory to.
 - attachment-path: Required The path to the directory that you want to attach to the Jira issue.
 - attachment-name: Required The name of the ZIP file that will be created from the directory.
 - jira-issue-comment: Optional A comment to add to the Jira issue along with the attachment.

## Usage
```yaml

- name: Attach directory to Jira issue
  uses: your-repository/attach-dir-to-jira-issue@v1
  with:
    jira-base-url: 'https://your-jira-instance.com'
    jira-user-email: 'your-jira-email@example.com'
    jira-api-token: ${{ secrets.JIRA_API_TOKEN }}
    jira-issue-id: 'ISSUE-1234'
    attachment-path: './reports'
    attachment-name: 'reports.zip'
    jira-issue-comment: 'Here are the reports from the latest build.'

```