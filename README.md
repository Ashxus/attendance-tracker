# ////// Attendance Tracker //////

A simple, single-page attendance system built to manage workdays easily. Staff tap their own name to check in and check out, no typing, no paperwork and the shop owner get a private admin panel with full history and CSV exports.

It's one plain HTML file with no build step, no server to maintain, and it's free to host and run.

## What it does...

Members page - a board of registered staff. Tap "Check In" when you arrive, "Check Out" when you leave. Each button can only be used once per day and grays out automatically. The board resets itself every midnight.

Admin page (PIN-protected) - register or remove staff, browse attendance history by date, export any day (or everything) as a CSV file, and manage who's allowed to log into the site at all.

Login screen - the whole site can be locked behind individual username/password accounts, so only people you've explicitly added can access it.

Salary & hours - pick any date range and see total hours and days worked per person, and who worked the most/least. Exportable as CSV. Also lets you set a payment day for each member individually (everyone can be on a different date), a reminder banner appears in Admin with a notification dot on the Admin tab, as each person's day approaches, on the day, and if it's overdue, until you mark it paid.

Monthly attendance summary - pick any month and see exactly how many days each member was present vs. absent (with a % present figure), exportable as CSV. Great for spotting who's missing shifts.

Live sync - when connected to Supabase (see setup below), every check-in/out is stored in a real shared database, so it doesn't matter whether someone uses their phone, a shop tablet, or your laptop everyone sees the same data.

## Tech stack

- Plain HTML, CSS, and JavaScript, no frameworks, no build tools
- [Supabase](https://supabase.com) (free tier) as the shared database
- Hosted for free on GitHub Pages


## Using the app

 First-time setup (as the shop owner)

1. Open the site. Click the **Admin** tab, you'll be asked to set an admin PIN the first time. Remember this; it's separate from staff logins.
2. Under **Register members**, add each staff member's name. These are the names that appear on the check-in board, no separate login needed just to check in.
3. *(Optional but recommended)* Under **Authorized users**, add a username and password for anyone who should be allowed to open the site at all. As soon as one user is added, everyone (including you) will need to log in on any new device.

## Basic Operation

- Staff open the site, find their name, and tap Check In / Check Out.
- You can view or export attendance history any time from the Admin page.

## Note

This web application is intended for businesses with a manageable workforce.

## License

MIT
