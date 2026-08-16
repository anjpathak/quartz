Here is a concrete, no-fluff sequence. Each step names exactly what to do and the free resource to use. Follow them in order and build as you go, no fixed timeline.

## Step 1: LLM API basics

Read the Anthropic API documentation directly: docs.claude.com, specifically the Messages API guide and the prompt engineering overview. Do the same for OpenAI at platform.openai.com/docs.

Build: a CLI script in Node or Python that takes a text file and summarizes it using the API. This forces you to handle the request, response parsing, and streaming.

Free resource: Anthropic Cookbook on GitHub (github.com/anthropics/anthropic-cookbook) has working code examples you can copy and modify directly.

## Step 2: Prompt engineering properly

Go through Anthropic's own prompt engineering interactive tutorial, free on GitHub: github.com/anthropics/prompt-eng-interactive-tutorial. It is hands-on with exercises, not just reading.

Build: take your Step 1 summarizer and improve it using few-shot examples and structured JSON output. Compare outputs before and after.

## Step 3: Embeddings and vector search fundamentals

Read the conceptual explainer at OpenAI's embeddings guide (platform.openai.com/docs/guides/embeddings). Then watch the free DeepLearning.AI short course "Building Applications with Vector Databases" at deeplearning.ai (it's free, no paid tier needed for short courses).

Build: take 5 to 10 of your own documents (resume versions, project notes), generate embeddings, and write a script that finds the most relevant document for a query.

Free resource for vector DB: Qdrant has a generous free cloud tier and the best beginner docs (qdrant.tech/documentation). Chroma is also free and runs entirely locally with zero setup, good for first experiments (docs.trychroma.com).

## Step 4: Full RAG pipeline

Follow DeepLearning.AI's free course "LangChain Chat with Your Data" (deeplearning.ai/short-courses). It's free, about 1.5 hours, and walks through chunking, embedding, retrieval, and generation end to end.

Build: a RAG app over a folder of PDFs (use your own resume variants and project docs from past work). Add a simple web UI with your React skills.

## Step 5: Tool use and function calling

Read Anthropic's tool use documentation directly (docs.claude.com, under "Tool use"). It has copy-paste examples.

Build: an agent that decides between two tools, for example a calculator function and a weather API call, based on the user's question.

## Step 6: LangGraph fundamentals

Take the official free DeepLearning.AI course "AI Agents in LangGraph", taught by Harrison Chase, the creator of LangChain himself. It teaches building an agent from scratch using Python and an LLM, then rebuilding it using LangGraph to learn its components, plus agentic search for retrieving multiple answers in an agent-friendly format. Free at deeplearning.ai/short-courses/ai-agents-in-langgraph.

Build: a 2-step research agent (research a topic, then draft a summary) following the course's structure but using your own use case, like an IPL stats research agent.

## Step 7: Multi-agent systems

Look for DeepLearning.AI's other short courses on multi-agent collaboration ("Multi AI Agent Systems with crewAI" is also free on their platform). These are consistently the best free, structured option because they're taught by the framework creators themselves.

Build: a 3-agent pipeline, for example a planner agent, a researcher agent, and a writer agent, coordinated through LangGraph.

## Step 8: MCP (Model Context Protocol)

Go straight to the official source: modelcontextprotocol.io has the full spec, quickstart guides, and example servers. This is maintained by Anthropic and is the most accurate, current resource.

Build: a simple MCP server that exposes one tool (for example, a function that queries a small SQLite database of your project history or cricket stats), then connect it to Claude Desktop or another MCP client to test it live.

## Step 9: Reliability and production patterns

Read LangChain's own blog and docs on LangGraph persistence, error handling, and human-in-the-loop patterns (langchain-ai.github.io/langgraph). The official docs are free and detailed, with working code samples for retries, checkpoints, and approval steps.

Build: add a human-approval checkpoint to your Step 7 multi-agent pipeline so it pauses before taking a final action.

## Step 10: Tie it to your full-stack skills

Use the Vercel AI SDK docs (sdk.vercel.ai/docs), which is free and open source. It's built specifically for streaming AI responses into React apps, showing tool calls in the UI, and handling multi-step agent execution visually.

Build: rebuild your Step 7 or Step 9 agent with a proper React frontend that streams the agent's thinking and tool calls live, this becomes your portfolio centerpiece.

---

A note on the additional Udemy and Coursera courses that show up in searches: most aren't free, so I've left them out and stuck to genuinely free, high-quality sources. If you do want a structured guided course later, there is a free LangGraph-focused course covering agent fundamentals and multi-agent patterns, but the DeepLearning.AI short courses plus official docs above will get you further faster, since they're built by the people who created these frameworks.

One practical tip: host all your build projects on GitHub as you go. By the time you finish Step 10 you'll have a clean commit history showing Gen AI, RAG, agentic orchestration, and MCP, which is exactly the kind of project trail that AI engineering interviewers want to see.