## Hi, I'm Rafae

**Software engineer — AI (MCP & RAG) · backend · AWS · automation.**

I build the backend that lets AI work safely with real company data: MCP servers behind an
auth and permissions layer, data pipelines on AWS, and the automation around them.

📍 Kuala Lumpur &nbsp;·&nbsp; 🌐 [rafaegill.com](https://rafaegill.com) &nbsp;·&nbsp;
💼 [LinkedIn](https://www.linkedin.com/in/muhammad-rafae-gill) &nbsp;·&nbsp;
📄 [CV](https://rafaegill.com/assets/Rafae_Gill_CV.pdf)

---

### Featured: [mcp-gatekeeper](https://github.com/rafae-gill/mcp-gatekeeper)

**Let a team's AI agents use company data, but only the parts each person should see.**

Most MCP servers are all-or-nothing: connect, and you get every tool and every table.
mcp-gatekeeper decides it person by person: which tools, which data, which hours, how
many calls a minute, with every call in an audit log. Access lives on each key, so it
changes live with no redeploy. It's the open-source core of the platform I run in
production for about 50 people, including in front of a Redshift warehouse.

<a href="https://github.com/rafae-gill/mcp-gatekeeper"><img src="assets/mcp-gatekeeper-demo.gif" alt="mcp-gatekeeper demo" width="640"></a>

### Now building: RAG for MCP 🔨

- **Semantic tool router.** With dozens of MCP tools, sending every description to the
  model on every call gets slow and expensive. This retrieves only the tools relevant to a
  request, and only the ones the caller's key is allowed to use, measured with a recall@k
  eval.
- **Schema-RAG text-to-SQL.** Retrieves the right tables and columns from a large warehouse
  schema before the model writes SQL.
- **"Ask my portfolio".** A chatbot over my own work, on pgvector.

### Things I've built at work
<sub>Code is private; these are the outcomes.</sub>

- **MCP platform**: 5 MCP servers (BI warehouse, ad platforms, docs, an internal deploy tool)
  behind a central FastAPI auth and permissions gateway, used daily by about 50 colleagues.
  The open-source core is mcp-gatekeeper, above.
- **Data pipeline**: cut an AWS Glue job from **5 hours to 20 minutes**, with about 10× lower
  compute cost.
- **Billing**: rebuilt a daily recurring-subscription billing engine. 20+ telco
  integrations, about 500k transactions a day on the largest.
- **AWS account migration**: moved a live serverless service (Lambda, API Gateway, DynamoDB)
  to a new account, about 90 files, and caught hard-coded references to the old account
  before go-live.

### Side projects

| Project | What it is |
|---|---|
| 🌐 [**rafaegill.com**](https://rafaegill.com) | My portfolio. Next.js + Supabase. |
| 🎟️ [**On The Move**](https://onthemovebh.com) | Freelance: members host events, take bookings and pay by QR. About 70 users. |
| 🐵 [**aura_farm_face_memer**](https://github.com/rafae-gill/aura_farm_face_memer) | Real-time face and hand-gesture tracking (MediaPipe + OpenCV) that mirrors your expressions as memes. Built for a friend. |

### Stack

| Area | Tools |
|---|---|
| **Languages** | Python · Java · TypeScript · JavaScript · PHP · SQL · C/C++ |
| **Backend & AI** | FastAPI · Flask · Node.js · Laravel · MCP · RAG · LangChain · n8n |
| **AWS** | Lambda · API Gateway · DynamoDB · Glue · Redshift · Athena · S3 · SQS/SNS · CloudWatch · EC2 |
| **Frontend** | React · Next.js · Tailwind |
| **Tooling** | Docker · Kubernetes · Supabase · Datadog · Git |

<sub>MEng Electrical & Electronic Engineering, University of Nottingham.</sub>
