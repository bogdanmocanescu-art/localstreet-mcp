# Localstreet MCP server

Local London information for AI assistants: independent businesses, what's on, schools, the borough noticeboard and what is happening right now (tube and rail status, roadworks, flood warnings, air quality).

It is the remote MCP server of [Localstreet](https://localstreet.co.uk), a free local directory for London boroughs. Every answer carries the Localstreet page it came from and when that data was last updated, so the assistant can cite it.

- **Endpoint:** `https://localstreet.co.uk/mcp` (Streamable HTTP)
- **Authentication:** none
- **Cost:** free

## Areas covered

[Ealing](https://localstreet.co.uk/ealing/), [Brent](https://localstreet.co.uk/brent/), [Hammersmith & Fulham](https://localstreet.co.uk/hammersmith-and-fulham/), [Harrow](https://localstreet.co.uk/harrow/), [Hillingdon](https://localstreet.co.uk/hillingdon/), [Hounslow](https://localstreet.co.uk/hounslow/), [Bromley](https://localstreet.co.uk/bromley/) and [Kensington & Chelsea](https://localstreet.co.uk/kensington-and-chelsea/). More boroughs open area by area.

Pass `area` as a borough (`ealing`, `brent`) or a postcode district (`W7`, `UB1`) for local answers.

## Tools

| Tool | What it answers |
|---|---|
| `search_businesses` | Find a local business by trade or name |
| `business_details` | One business: address, phone, opening hours, open now |
| `events_on` | What's on in a borough today, tomorrow, at the weekend or this week |
| `area_now` | Right now: tube and rail status, bus disruption, serious roadworks, flood warnings, air quality |
| `schools_near` | Schools nearby, with Ofsted rating, phase and faith character |
| `catchment_check` | Whether a postcode was inside a school's last admissions distance |
| `noticeboard_search` | Live posts on the borough noticeboard: for sale, free, wanted, local help |

## Example questions

- "Is there a plumber in W7 who's open now?"
- "What's on in Ealing this weekend for kids?"
- "Any problems on the Elizabeth line or roadworks near Hanwell right now?"
- "Which primary schools near UB1 are rated Outstanding?"

## Connect

**Claude** (claude.ai or Claude Desktop): Settings → Connectors → Add custom connector → URL `https://localstreet.co.uk/mcp`.

**Cursor, VS Code, Windsurf and other MCP clients:**

```json
{
  "mcpServers": {
    "localstreet": { "url": "https://localstreet.co.uk/mcp" }
  }
}
```

## Where the data comes from

Public sources, refreshed on a schedule and dated in every answer: TfL, the Environment Agency, London Air, Ofsted and the Department for Education, councils' own listings, local venues' and libraries' event listings, and businesses' own public listings.

## Links

- [Localstreet](https://localstreet.co.uk): the directory
- [What's on in London boroughs](https://localstreet.co.uk/whats-on/)
- [Add your business, free](https://localstreet.co.uk/add)
- [Privacy](https://localstreet.co.uk/privacy)
