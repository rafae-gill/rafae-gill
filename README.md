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

### Featured: [mcp-tool-rag](https://github.com/rafae-gill/mcp-tool-rag), RAG for AI tools

Give each AI agent only the tools it needs, and only the ones its user is allowed to use.
It filters by permission first, then runs hybrid search (BM25 + embeddings, plus example
requests per tool). Evaluated three ways:

<a href="https://github.com/rafae-gill/mcp-tool-rag"><img src="assets/mcp-tool-rag-demo.gif" alt="mcp-tool-rag demo: same request, two people, different tools" width="640"></a>

| | Result |
|---|---|
| 1,351 real user requests ([BFCL](https://proceedings.mlr.press/v267/patil25a.html), 528 tools) | right tool in the **top 5: 92%**, top 10: 96% |
| [ToolRet](https://arxiv.org/abs/2503.01763) benchmark (44k tools) | hybrid beats keyword and embedding search in every setting |
| Permission-aware vs ordinary search | forbidden tools shown: **0%** vs 63–88% of requests |

The finding I'd most want other people to know: when the same AI writes both your test set
and your enrichment, the measured gain was inflated about 10× (+32 points vs +3 on real
requests).

### Now building 🔨

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
