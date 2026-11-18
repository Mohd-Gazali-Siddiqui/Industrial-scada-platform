# Industrial SCADA Platform

A modular, web-based Industrial SCADA-style monitoring and supervisory control platform.

## Initial use case
The first implementation will model a **simulated water treatment plant**. The architecture allows
future industry modules such as oil & gas and power without duplicating the SCADA core.

## Planned technology
- Frontend: React + TypeScript + Vite
- Backend: Node.js + Express + TypeScript
- Database: PostgreSQL + Prisma
- Real-time: WebSocket
- Industrial communication: Modbus TCP initially; OPC UA / MQTT may be added later
- PLC integration: OpenPLC or a custom simulator
- Monorepo: npm workspaces

## Structure
- `apps/web` — operator dashboard
- `apps/api` — backend API and orchestration
- `apps/simulator` — simulated PLCs, sensors and process values
- `packages/shared` — shared types and schemas
- `packages/telemetry` — telemetry validation and processing
- `packages/alarm-engine` — reusable alarm evaluation and lifecycle
- `packages/device-connectors` — industrial protocol adapters
- `packages/process-modules/water` — water-treatment process configuration
- `packages/process-modules/oil-gas` — future oil & gas process configuration
- `packages/process-modules/power` — future power process configuration
- `docs` — architecture and industry documentation
- `infra` — local infrastructure and deployment configuration

## Getting started
Install Node.js LTS, then run `npm install` from the repository root.
The workspaces are scaffolds; application dependencies and scripts will be added during implementation.

## Status
Repository scaffold created. Implementation has not started.

## Safety
Educational prototype only. Use simulated data or isolated test equipment. Not certified or intended
to control live industrial machinery.
