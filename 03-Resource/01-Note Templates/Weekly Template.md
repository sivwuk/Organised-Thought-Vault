---
type: "Weekly"

---

# Weekly Review Notes - Week <% tp.date.now("WW-YYYY", 0, tp.file.title, "YYYY-WW") %>

Created: <% tp.date.now("DD-MMM-YYYY") %>

<<[<% tp.date.now("YYYY-WW", "P-1W", tp.file.title, "YYYY-WW") %>](app://obsidian.md/%3C%25%20tp.date.now(%22YYYY-MM-DD%22,%20-1,%20tp.file.title,%20%22YYYY-MM-DD%22)%20%25%3E) | [<% tp.date.now("YYYY-WW", "P+1W", tp.file.title, "YYYY-WW") %>](app://obsidian.md/%3C%25%20tp.date.now(%22YYYY-MM-DD%22,%201,%20tp.file.title,%20%22YYYY-MM-DD%22)%20%25%3E) >>


---

## Goal Tracking

### To do
`$=dv.list(dv.pages('"02-Area/02-Goals"').where(p => p.status == "To Do").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`
### Doing
`$=dv.list(dv.pages('"02-Area/02-Goals"').where(p => p.status == "Doing").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`
### Done
`$=dv.list(dv.pages('"02-Area/02-Goals"').where(p => p.status == "Done").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

---

## Top three wins
1)
2)
3)

---

## Journal

-   Events

---

## Gratitude - What am I grateful for?
1)
2)
3)


