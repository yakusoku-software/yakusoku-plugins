---
name: wedding-planning
description: Plan a wedding in Yakusoku with its MCP tools. Use when the person asks about their wedding's guests, RSVPs, seating, menu, songs, budget, tasks, calendar, vendors, photos, vision boards, documents, gift registry or messages, or about their Yakusoku vendor business.
---

# Wedding planning with Yakusoku

Yakusoku's tools act as the signed-in person, inside what they allowed when they connected. A tool that is missing from the list was not allowed: say so, and point them to Settings → AI assistants in Yakusoku to reconnect with more access, rather than working around it.

## Find the wedding first

Most tools take a `weddingId`. Call `list_weddings` once, and if the person has more than one wedding, ask which one before changing anything. Planners may have several; couples usually have one.

## Read before you write

- Guests and RSVPs: `list_guests`, `get_rsvp`. Seating: `get_seating`. Budget: `get_budget`. Tasks: `list_tasks`. Calendar: `get_calendar`. Vendors: `get_vendors`. Gift registry: `get_gift_registry`. Messages: `list_messages`.
- Look up ids with a read call rather than guessing them, and match people by the names the read returns.

## Preview bulk changes, then commit

Imports and sends are two steps. Show the person the preview, including flagged rows and duplicates, and commit only after they agree:

- Guest lists from a spreadsheet: `list_guests` (view `import_schema`) to map the columns, `preview_guest_changes` (kind `import`), then `import_guests`.
- Tasks: `preview_task_import`, then `import_tasks`.
- Expenses: `preview_expense_import`, then `import_expenses`.
- RSVP invitations and code reminders: `preview_guest_changes` (kind `invitations` or `code_reminders`), then `send_guest_invitations`.

## Ask before anything that contacts people or deletes

`send_message`, `send_guest_invitations`, `manage_members` invites and vendor `send_questionnaire` email or message real people: confirm the wording and the recipients first. Every `delete_*` tool removes records for good: name what will be deleted and wait for a yes.

## Money

Amounts come back with a `display` string in the wedding's own currency. Quote that string rather than converting or reformatting it.

## Vendors

A vendor's own business (listings, bookings, invoices, questionnaires) is under `get_vendor_business` and `manage_vendor_business`. The weddings a vendor is booked for are read-only through `get_vendor_weddings`.
