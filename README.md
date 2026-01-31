# Action Repository

This repository is configured to send webhook events to a Flask application for monitoring GitHub actions.

## Purpose

This repository demonstrates GitHub webhook integration by sending events for:

- Push actions
- Pull request creation
- Pull request merges

## Webhook Configuration

This repository is configured to send webhooks to the `webhook-repo` Flask application.

**Configured Events:**

- ✅ Pushes
- ✅ Pull Requests

## Testing the Integration

### Test Push Event

```bash
echo "Test" > test.txt
git add test.txt
git commit -m "Test push event"
git push origin main
```

### Test Pull Request Event

```bash
git checkout -b feature-branch
echo "Feature" > feature.txt
git add feature.txt
git commit -m "Add feature"
git push origin feature-branch
```

Then create a Pull Request on GitHub from `feature-branch` to `main`.

### Test Merge Event

Merge the Pull Request using GitHub's "Merge pull request" button.

## View Events

Events can be viewed at the webhook receiver application's dashboard.

## Related Repository

- [webhook-repo](https://github.com/Now-Tiger/webhook-repo) - Flask webhook receiver
