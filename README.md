# AI Proposal Email Generator (n8n Workflow)

Automatically generate and send professional proposal emails using AI and n8n.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This workflow allows small to medium businesses to **automate their proposal email creation**. When a client request is submitted (via a form, Airtable, or email), the workflow triggers an AI agent to generate a professional email subject and body. The email is then sent automatically to the client.  

## Features
- AI-powered email subject and body generation
- Personalized and professional content for each client
- Automatic email delivery
- Easy to customize for any service-based business

## Technologies Used
- **n8n** – Workflow automation
- **OpenAI / AI Agent** – Generate email subject and body
- **SMTP / Gmail / Email Node** – Send emails
- Optional: **Google Forms, Airtable, or Email Trigger** – Input client requests

## Setup & Installation
1. **Install n8n**  
   Follow the [n8n installation guide](https://docs.n8n.io/getting-started/installation/).  

2. **Create your workflow**  
   - Add a trigger (Google Form, Airtable, or Email)  
   - Add the **Gemini/AI Agent node** with your API key  
   - Use structured output parser for JSON (optional):  
     ```json
     {
       "type": "object",
       "properties": {
         "emailSubject": { "type": "string" },
         "emailBody": { "type": "string" }
       },
       "required": ["emailSubject", "emailBody"]
     }
     ```  
   - Add **Email node** to send the generated email  

3. **Set dynamic variables** (optional): company name, email, domain, etc.

## Usage
1. Client submits a request via your chosen trigger method.  
2. AI generates a professional email subject and body.  
3. Email is sent automatically to the client.  

## Contributing
- Feel free to open issues or submit pull requests to improve the workflow.  
- Suggestions for new features like multi-language support or template customization are welcome.

## License
This project is licensed under the MIT License.  
