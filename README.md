# TRIADEC Frontend — Backend-connected update

React + Vite interface. The workspace reads its metrics, ledger records, risk signals, audit events, and health status from the FastAPI backend.

## Run
1. Install Node.js LTS.
2. In this folder run `npm install` then `npm run dev`.
3. Set `VITE_API_BASE_URL=http://127.0.0.1:8001` in `.env` if your API runs elsewhere.

## Functional in this update
- API health status and refresh.
- Database-backed metrics and ledger list, search, and verified-status filter.
- Ledger record detail with audit trail.
- Create record via `POST /api/records`; new records are explicitly user-submitted and start Under review.
- Mark a record for review via backend and store the audit event.
- Risk signal list from the backend's transparent heuristic endpoint.
- Audit event list.
- Profile panel for local UI preferences (not real authentication; values are not persisted server-side).

## Important data limitations
The backend seeds synthetic examples when its database is empty. These are not real NGO transfers. “Verified” is a stored status label, not proof of real-world delivery. Hashes beginning `demo-` are illustrative markers, not cryptographic signatures. Risk signals are heuristic review prompts, not fraud findings. Real public-source integration and secure user authentication are not implemented in this update.
