🎓 Learning Path Generator
An AI-powered learning-path automation built with n8n. A user sends a learning request through chat, and the workflow uses an AI Agent to help generate a structured learning journey. It also connects to Google services to create learning documents and calendar events.
Workflow overview

The workflow shown above contains these connected components:
1. When chat message received — starts the workflow when a user sends a message.
2. AI Agent — processes the user's learning request and coordinates the connected tools.
3. Gemini Chat Model — provides the language model used by the AI Agent.
4. Google Search (SerpApi) — gives the agent access to web search.
5. Google Docs — creates and updates a document for the learning content.
6. Google Calendar — creates a calendar event for a learning session.
The screenshot shows an example output for a one-day React JS learning journey.
Built with
- n8n — workflow automation
- Google Gemini — AI chat model
- SerpApi — Google search integration
- Google Docs — learning document creation
- Google Calendar — learning session scheduling
- Google OAuth 2.0 — Google account authorization
How it works
1. The user enters a learning goal in the n8n chat.
2. The AI Agent interprets the request and uses its connected model and tools.
3. Search results can be used to support the learning content.
4. The workflow creates or updates a Google Docs document.
5. The workflow creates a Google Calendar event for the learning session.
6. The workflow returns a response to the user.
The exact learning content and schedule depend on the request and the workflow configuration.
Requirements
- An n8n instance
- Google Gemini credentials (or the model credentials configured in the workflow)
- SerpApi API key
- A Google account
- Google Docs and Google Calendar access configured in n8n
Import and setup
1. Download the workflow JSON file from this repository.
2. Open your n8n instance.
3. Import the JSON workflow.
4. Open each node that uses an external service and select or create your own credentials.
5. Configure Google OAuth for the Google Docs and Google Calendar nodes.
6. Add your own SerpApi credentials.
7. Review the AI Agent instructions and adjust them to your needs.
8. Test the workflow with a sample learning request in the chat trigger.
Note: Importing the JSON does not transfer the original owner's credentials. You must connect your own accounts and provide your own API keys.

Security
- Never commit API keys, OAuth client secrets, access tokens, or passwords.
- Check the exported workflow JSON for sensitive values before publishing.
- Use GitHub Secrets or your deployment platform's secure credential storage for any required secrets.
- Keep the repository private if it contains information you do not intend to share.
Project structure
learning-path-generator/
├── learning-path-generator.json
├── README.md
└── screenshots/
    └── workflow.png

Author
Rushikesh Bodigundla
