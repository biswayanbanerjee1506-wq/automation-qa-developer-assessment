Task 2 – Hacker News API Integration

Objective

Build an automated n8n workflow to retrieve, filter and process the top
Hacker News stories.

Workflow Steps

1.  Schedule Trigger: Runs every hour.
2.  HTTP Request: Retrieves the top Hacker News story IDs.
3.  Code Node: Selects the top 5 story IDs.
4.  HTTP Request 1: Fetches story details, including title, author,
    score and URL.
5.  IF Node: Filters stories with a score greater than 100.
6.  Code Node: Generates a structured report of qualifying stories
    inside n8n.

API Used

Hacker News Firebase API: https://hacker-news.firebaseio.com/v0/

Output

The workflow generates a report containing qualifying story titles,
authors, scores and URLs directly in n8n.

Error Handling and Limitations

The workflow currently uses local output inside n8n. No external email
or messaging notification is configured. Error handling branches have
not yet been fully configured and verified.

Testing

The workflow was executed successfully in n8n. The execution output
showed five story details entering the IF condition, with qualifying
stories passing to the final Code node.
