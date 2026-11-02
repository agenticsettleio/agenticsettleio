# AgenticSettle

Verification and settlement infrastructure for work done by AI agents. When one agent hands work to another,
who checks that the work matches what was agreed? We build that check, and the payment step that follows it.

## What is public here

- **[agenticsettle-mcp](https://github.com/agenticsettleio/agenticsettle-mcp)** - a free, verification-only MCP server.
  Score an agent's output 0-100 and get a PASS / PARTIAL / FAIL verdict. Run it locally, or use the hosted endpoint
  `https://app.agenticsettle.io/mcp`. The repo also has runnable examples for LangGraph and CrewAI.
- **[agenticsettle-test-gated-release](https://github.com/agenticsettleio/agenticsettle-test-gated-release)** - a small demo
  that releases an agent's work only if its tests pass and the verification agrees. The settlement receipt is simulated.
- **[agenticsettle-x402-demo](https://github.com/agenticsettleio/agenticsettle-x402-demo)** - an agent pays per call in USDC
  over the x402 protocol to use verification. Base Sepolia testnet only.

## Try it

- Get a free key (an email is required, no credit card):

  ```bash
  curl -sX POST https://app.agenticsettle.io/v2/signup \
    -H "Content-Type: application/json" -d '{"email":"you@example.com"}'
  ```

- Python SDK: `pip install agentic-settle`
- No-account trial: https://app.agenticsettle.io/try
- Website: https://agenticsettle.io

## Status

A solo-founder project, pre-revenue. Everything public here is free verification or testnet work; no real money moves
in these repositories. A verdict is an automated assessment and can be wrong, so treat it as a check, not a guarantee.

---

## 한국어

AI 에이전트가 한 일을 검증하고, 검증 결과에 따라 정산하는 인프라를 만들고 있습니다. 위 저장소들은 모두
무료 검증 또는 테스트넷 범위이며 실제 돈이 오가지 않습니다. 1인 창업가가 만드는 매출 전 단계의 프로젝트이고,
판정은 자동 평가라서 틀릴 수 있습니다.
