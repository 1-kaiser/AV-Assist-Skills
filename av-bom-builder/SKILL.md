---
name: av-bom-builder
description: Use when the user asks for a bill of materials, equipment list, kit list or quote for an AV room, or wants a standard room BOM adapted to a specific room.
---

# BOM Builder

Build a complete, priced bill of materials from the approved products list, then save it to the project only after confirmation.

## Inputs
- Room Summary (av-room-discovery), display result (av-display-sizing), audio result (av-audio-coverage)
- Company room standard for this room type, if one exists
- Budget tier

## Steps
1. Start from the **company room standard** for the room type if one exists; otherwise build from the design results.
2. Fill every category. Use this checklist so nothing is missed:
   - Displays / projector / screen + **mounts**
   - Video conferencing: codec/compute, cameras, touch controller, room scheduler panel
   - Audio: mics, loudspeakers, DSP, amplifier, **Dante licences**
   - Switching / extension / AV-over-IP encoders and decoders
   - Control processor, touch panel, **programming licences**
   - Network: PoE switch (check PoE budget), patch leads
   - Rack or credenza, PDU/UPS, shelves, blanking, fans
   - Cables, connectors, wall plates, table boxes, labels
   - Software/support subscriptions and warranties
   - Labour lines (design, install, programming, commissioning, training) if the user wants them
3. Use only **Approved Products List** items. Use an off-list item only if nothing fits, and mark it **Off-list**.
4. Look up price, stock and lead time with the **Pricing & Stock** tool. If it is unavailable, leave price blank and mark it **TBC**. Never invent a price.
5. Check compatibility before finishing: UC certification, HDCP/EDID, USB extension length, PoE class vs switch budget, DSP I/O and Dante channel counts.
6. Show the BOM in chat, then ask: "Save this BOM to project {{ProjectID}}?" Save to Excel Online / SharePoint only after a clear yes.

## Output
| Line | Qty | Category | Manufacturer | Model | Description | Location | Unit price | Ext. price | Lead time | Notes |
|---|---|---|---|---|---|---|---|---|---|---|

Followed by: subtotal by category, total, list of TBC items, and compatibility notes.

## Don'ts
- No invented model numbers, prices or lead times.
- Do not save or overwrite files without confirmation.
