# AI Chatbot Widget

A rule-based chatbot widget for website integration — **zero APIs, zero dependencies, zero backend**. Drop one `<script>` tag into any HTML page and it works instantly.

## How It Works

Keyword matching against a predefined rule set. First matching rule wins. Covers common visitor questions about services, projects, skills, pricing, and contact.

```
Visitor types: "what services do you offer?"
  → keyword match: "service"
  → reply: "Three main service areas: Security, Web Dev, AI/Automation..."
```

## Embed (one line)

```html
<script src="chatbot.js"></script>
```

That's it. The widget injects itself — floating button bottom-right, opens a styled chat window, handles everything client-side.

## Topics Covered

| Topic | Trigger keywords |
|-------|-----------------|
| Greeting | hi, hello, hey, yo |
| Services | service, offer, help with |
| Projects | project, portfolio, github, repo |
| Skills | skill, tech, language, tool |
| Security | pentest, ctf, hack, vuln |
| Pricing/Hire | price, cost, hire, available |
| Contact | contact, email, reach, linkedin |
| Certifications | tryhackme, oscp, comptia, cert |
| GhostFile | ghostfile, encrypt, aes |
| dufo.save | dufo, privesc, bash script |
| Farewells | bye, thanks, cheers |
| Jokes | joke, funny |

## Customising Responses

Edit the `RULES` array in `chatbot.js`:

```js
const RULES = [
  {
    keywords: ['hello', 'hi', 'hey'],
    reply: "Hi! How can I help you today?"
  },
  {
    keywords: ['price', 'cost', 'hire'],
    reply: "Drop me an email and we'll talk."
  },
  // add more rules here...
];
```

Rules are checked top-to-bottom — put more specific rules before general ones.

## Files

```
ai-chatbot/
├── chatbot.js   ← the widget (embed this)
├── demo.html    ← test page (open in browser)
└── README.md
```

## Run Locally

```bash
git clone https://github.com/B-star51/ai-chatbot.git
cd ai-chatbot
# Open demo.html in any browser — no server needed
```

---

*Part of the [B-star51 portfolio](https://github.com/B-star51)*