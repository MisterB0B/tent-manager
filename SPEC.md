# The Light Park - Tent Manager App Spec

> **Logo:** `logo.jpg`

## Overview
Ground-level operations app for tent staff at each venue. Role-based tasks, real-time info, and management visibility.

---

## Roles
- Manager / Tent Lead
- Ticket Scanner
- Merch
- Concessions
- Mascot (DJ Polar Ice, Pixel Penguin)
- Roamer / Safety Patrol
- Traffic / Cue Lane
- Upseller

---

## Core Features

### 📋 Role-Based Task Lists
- Each staff member sees tasks specific to their role
- Daily checklists auto-generated
- Mark tasks complete — management sees progress

### 👥 Staff Management
- Who's working tonight (pulled from Paycor if integrated)
- Role assignments
- Contact info for all on-duty staff

### ⏱️ Mascot Rotation System
- 3 people: 2 in costume, 1 on break
- 30-minute swap timer
- Alerts when time to switch
- Break time logging for compliance

### 📍 Roamer Checkpoints
- QR codes posted around venue
- Roamers scan every 10 minutes
- Missed scan = alert to tent lead
- Patrol route tracking

### 🎵 Tent Audio Control
- Pi-based music system in tent
- Pre-approved playlists only (managers can't add their own)
- Play/pause/skip from app
- Rotates daily to keep it fresh

### 📹 Venue Cameras
- LTS camera feeds (RTSP integration)
- Only shows THIS venue's cameras
- Quick view of parking, queue, entrance

### 🌤️ Weather
- Current conditions for venue location
- Alerts for rain, extreme temps, wind

### 📞 Key Contacts
- Overnight security company info
- Off-duty officer phone (on-site during show)
- Show Tech contact for issues
- Emergency numbers

---

## Inventory & Sales

### 📦 Inventory Tracker
- Merch stock levels
- Concession supplies
- Low stock alerts
- Restock requests

### 💵 Cash Management
- Starting petty cash float
- Cash received log
- Change given
- End-of-night count
- Variance calculation

### 📊 Sales Tracker
- Merch sold per shift
- Concessions sold
- Real-time totals

### 🏆 Upsell Leaderboard
- Track who's selling the most add-ons
- Friendly competition / gamification
- Daily and season totals

---

## Safety & Compliance

### 📝 Incident Reports
- Guest complaints
- Accidents
- Unusual events
- Timestamped, logged

### 🔍 Lost & Found Log
- Item description
- Where found
- Claimed or not

### 🩹 First Aid Log
- Document any medical incidents
- Who, what, when, action taken

### 🚽 Restroom Check Log
- Hourly cleanliness checks
- Staff signs off
- Compliance record

### 🚨 Emergency Procedures
- Quick reference guide
- One tap access
- Fire, medical, weather, security

---

## Communication

### 📢 Daily Briefing
- Morning message from management
- Everyone sees it at shift start
- Announcements, focus areas, reminders

### 🔄 Shift Handoff Notes
- Outgoing shift leaves notes
- Incoming shift reads before starting
- Issues, heads-ups, continuity

### 📻 Radio Channel Assignments
- Who's on what channel
- Quick reference

### 🔗 Link to Show Tech
- Report prop/light issues
- Goes directly to tech task queue
- "Gnome in zone 3 flickering" → tech sees it

---

## Logistics

### 🅿️ Parking Status
- Main lot capacity
- Overflow lot status
- Update in real-time

---

## Integrations

### Paycor (Payroll/Scheduling)
- Pull employee schedules
- Sync shifts
- API available — need to confirm subscription tier

### Ramp (Expenses)
- Read-only visibility
- See what's being spent on Ramp cards
- Tent lead purchases visible to management

### LTS Cameras
- RTSP stream integration
- Per-venue camera views

### Show Tech App
- Issue submission
- Two-way communication

---

## Questions for Michael (VP of Ops)

1. What Paycor tier/products do we have? Is scheduling included?
2. Who manages Ramp access? Can we get read-only API credentials?
3. What positions/roles are officially used in Paycor?
4. How many tent staff per venue typically?
5. Any existing daily task sheets we should reference?
6. Preferred radio channel structure?
7. Any compliance requirements for break logging?
8. Who should have admin access to Tent Manager?
9. LTS camera credentials — who has them?
10. Anything missing from this feature list?

---

## Technical Notes

- **Venue-specific:** User selects their venue, sees only their stuff
- **Mobile-first:** Must work great on phones
- **Offline consideration:** Some features should work if WiFi drops
- **Real-time:** Tasks, inventory, alerts should update live

---

*Spec created: 2026-02-06 12:51am*
*Meeting with Michael: 2026-02-06 1:00pm*
