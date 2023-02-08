
![[Brain.png|100x100]] 

# 🆕 Quick Access
```button
name Fleeting Note
type template note(00-Inbox/New Fleeting Note, split)
action Fleeting Template
templater true
``` 
```button
name Literature Note
type template note(00-Inbox/New Literature Note, split)
action Literature Template
templater true
```
```button
name Permanent Note
type template note(00-Inbox/New Permanent Note, split)
action Permanent Template
templater true
```

```button
name Project Note
type template note(00-Inbox/Project Note, split) note
action Project Template
templater true
```
```button
name Area Note
type template note(00-Inbox/Area Note, split)
action Area Template
templater true
```
```button
name Resource Note
type template note(00-Inbox/Resource Note, split)
action Resource Template
templater true
```
```button
name Weekly Note
type template note(02-Area/01-Weekly Notes/<% tp.date.now("YYYY-WW")%>, split)
action Weekly Template
templater true
``` 
# 📫  Inbox
- 💡 Task 
	- [[00-Inbox/Task List|Task List]]
```tasks
not done
path includes 00-Inbox
limit 5
```

---

- 💡 Projects 
`$=dv.list(dv.pages('"00-Inbox"').where(p => p.type == "Project").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

- 💡 Areas 
`$=dv.list(dv.pages('"00-Inbox"').where(p => p.type == "Area").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

- 💡 Resources 
`$=dv.list(dv.pages('"00-Inbox"').where(p => p.type == "Resource").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

# 🏁  Project
```dataview
TABLE project, file.mtime, published, due, status FROM "01-Project" 
WHERE file.name = "Project Dashboard" SORT file.mtime DESC
```


# 🗓️ Area
- 🗒️  Daily Notes 
`$=dv.list(dv.pages('"02-Area/00-Daily Notes"').where(p => p.type == "Daily").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

- 🗨️ Weekly Review
`$=dv.list(dv.pages('"02-Area/01-Weekly Notes"').where(p => p.type == "Weekly").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

- ⭐  Goal Tracking
	- To do
		 `$=dv.list(dv.pages('"02-Area/02-Goals"').where(p => p.status == "To Do").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`
	- Doing
		 `$=dv.list(dv.pages('"02-Area/02-Goals"').where(p => p.status == "Doing").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`
	- Done
		 `$=dv.list(dv.pages('"02-Area/02-Goals"').where(p => p.status == "Done").sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`


# 🗒️ Research Notes
- 🚢  Fleeting Notes
`$=dv.list(dv.pages('"03-Resource/03-Research/01-Fleeting Notes"').sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

- 📚 Literature Notes
`$=dv.list(dv.pages('"03-Resource/03-Research/02-Literature Notes"').sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`

 - 🖨️ Permanent Notes
`$=dv.list(dv.pages('"03-Resource/03-Research/03-Permanent Notes"').sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`



# 🗃️ Vault Stats
🗄️ Recent file updates
 `$=dv.list(dv.pages('').sort(f=>f.file.mtime.ts,"desc").limit(5).file.link)`
 
- 〽️ Stats
	-  Total File Count: `$=dv.pages().length`
	-  Literature Count: `$=dv.pages('"02-Source Note"').length`
	-  Permanent Count: `$=dv.pages('"03-Permanent Note/1-Idea"').length`


# 🔖  All Tasks 
```tasks
not done
path includes TwitterOS
limit 5
```

