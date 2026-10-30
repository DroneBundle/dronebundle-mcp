# DroneBundle MCP Server

Connect Claude or ChatGPT to your [DroneBundle](https://dronebundle.com) workspace and ask about your drone operation in plain language. Projects, jobs, flights, pilots, equipment, maintenance, safety, clients and invoices, all from one chat.

The server is hosted by DroneBundle and is **read-only**. It signs in with your own DroneBundle account, sees only what that account can see, and can never create, edit or delete anything.

| | |
|---|---|
| **Server URL** | `https://api.dronebundle.com/v1/mcp` |
| **Transport** | Streamable HTTP |
| **Sign-in** | OAuth with your DroneBundle account (email and password, or Continue with Google) |
| **Access** | Read-only, 60 tools |
| **Plans** | Included on every DroneBundle plan |

There is nothing to install and no keys to copy. You add the server URL to your assistant, sign in, and approve.

## What is DroneBundle?

DroneBundle is operations software for commercial drone teams. It keeps client projects and jobs, pilot scheduling, flight logs (including DJI Dock flights synced from DJI FlightHub 2), drone maps, equipment and maintenance, safety records, clients and invoices in one workspace.

## Connect Claude

1. In Claude, open **Settings > Connectors** and choose **Add custom connector**.
2. Name it `DroneBundle` and paste `https://api.dronebundle.com/v1/mcp` as the URL.
3. Click **Connect**. A DroneBundle sign-in page opens.
4. Sign in with your DroneBundle account and approve the connection.

## Connect ChatGPT

DroneBundle is listed in [ChatGPT's app directory](https://chatgpt.com/plugins/plugin_asdk_app_6a9ad2da2cec8191b217961781bec648) under Business & Operations.

1. Open the [DroneBundle app in ChatGPT](https://chatgpt.com/plugins/plugin_asdk_app_6a9ad2da2cec8191b217961781bec648) and click **Connect**.
2. Sign in with your DroneBundle account and approve the connection.

## What you can ask

- Give me an overview of my workspace.
- Which active jobs don't have a pilot assigned?
- Which flights are scheduled this week, and who is flying them?
- Which pilots are available on Friday?
- Show me the latest flights on the Hudson Bridge job and who flew them.
- Summarize equipment maintenance and call out anything overdue.
- Show me the high and critical safety risks.
- What is the weather at the North Roof job site right now?

## Tools

Every tool is read-only and marked `readOnlyHint: true`.

| Area | Tools |
|---|---|
| Workspace | `workspace_overview`, `search`, `recent_activity`, `workspace_filter_options`, `workspace_storage` |
| Projects and jobs | `list_projects`, `get_project`, `get_project_access`, `get_project_discussion`, `list_jobs`, `get_job` |
| Flights | `list_flights`, `get_flight`, `list_flight_reports`, `list_flight_approvals`, `list_approved_flights` |
| Pilots and scheduling | `list_pilots`, `get_pilot`, `get_pilot_assignments`, `get_pilot_availability`, `get_shift_presets`, `get_pilot_shift_plan`, `get_shift_coverage` |
| Team | `list_team`, `get_team_member` |
| Equipment and maintenance | `list_equipment`, `get_equipment`, `list_assigned_equipment`, `get_equipment_assignments`, `maintenance_overview`, `list_maintenance_schedules`, `get_maintenance_schedule`, `list_maintenance_records`, `get_maintenance_record` |
| Safety | `list_risks`, `get_risk`, `list_incidents`, `get_incident`, `safety_audit_overview`, `list_audits`, `get_audit` |
| Drone maps | `list_scans`, `get_scan` |
| Clients and CRM | `list_client_companies`, `get_client_company`, `get_client_company_access`, `list_clients`, `get_client`, `list_deals`, `get_deal`, `get_deal_activity`, `crm_stats` |
| Invoices | `list_invoices`, `get_invoice` |
| Documents and files | `list_documents`, `get_document`, `list_project_files`, `list_job_files` |
| Weather | `get_weather`, `list_job_weather_locations` |

## Access and security

- **Read-only.** The server has no tools that create, edit or delete records.
- **Signs in as you.** Your assistant gets exactly the access your DroneBundle account has, in the workspace you approve.
- **Admins and project managers.** Workspace admins and project managers can connect an assistant.
- **No shared keys.** Each connection uses its own sign-in, and you can disconnect it at any time from your assistant or from DroneBundle.

## Links

- [DroneBundle](https://dronebundle.com)
- [AI Connectors](https://dronebundle.com/ai-connectors): what an assistant can reach and how to connect it
- [Drone MCP server guide](https://dronebundle.com/blog/drone-mcp-server)
- [Privacy policy](https://dronebundle.com/privacy)
- [Support](https://dronebundle.com/support)

This repository documents the hosted server. The server itself runs on DroneBundle's infrastructure.
