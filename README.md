# iron-log

**Iron Log** is a single-file web app (one HTML file, no backend) for tracking strength training, built around a 4-5 day workout split with a strong personalization layer on top.

At its core, it's a workout logger: each training day shows a list of exercises with target rep ranges, input fields for weight and reps per set, and a "last time" comparison so you can see exactly what you did last session before you try to beat it. Saving a session checks every exercise against your all-time best using an estimated one-rep-max formula and flags a PR badge when you've topped it, with separate handling for bodyweight moves like pull-ups and push-ups, where reps rather than load are the real progress signal.

**Profile**
The Profile tab stores your name, gender, age, height, body weight, lifting experience, main goal and any injuries. Gender, body weight and experience are used to suggest a starting weight for every exercise you haven't logged yet. The estimate also adjusts for age, and for height via BMI: above BMI 25 only part of the extra weight counts. The tab lists the suggestions for your whole program, and you can switch back to the plan's own start weights at any time. The profile also prefills the Personalize wizard and syncs with Google Drive and backups.

**Personalize Wizard**
A personalization wizard asks five questions, your goal, experience level, training days per week, available equipment, and an optional focus muscle, then generates a tailored split by pulling from a tagged exercise database, with a 10-second animated loading screen and rotating motivational text while it works. It launches automatically for first-time users and can be rerun anytime, offering to replace or merge with whatever program you already have.

**Weekly Progress**
The app also gives you a weekly progress view showing how many of your program days you've completed this week (the week starts on Sunday or Monday, set automatically from your plan or chosen in Profile), with checkmarks on the nav tabs themselves, and progression suggestions that analyze your session history to nudge you toward adding weight (if you've hit the top of your rep range twice running) or taking a deload (if you've stalled for three sessions). History itself supports full editing: you can fix or delete any individual past session, not just wipe everything at once.

**Dashboard & Consistency**
The dashboard opens with today's planned session, read from day names like "Mon – Legs", or the next one if today is a rest day. It also shows this week's progress, volume compared with the same point last week, and all-time totals. The Consistency section shows:
- the share of planned days you completed over the last 4 and 12 weeks
- your full-week streak (every planned day done) and your best one
- an active streak (weeks with at least one workout)
- a 13-week calendar showing workouts and missed planned days (tap a day for details)
- planned days done per week against your target
- which days you skip most often

**Track on the Go**
For persistence, everything saves locally in the browser by default, with optional Google Drive sync (via OAuth) so your program, history, and header text follow you across devices. There's also a click-to-edit header for naming the app yourself, and a unit toggle that displays everything in lb or kg without touching how data is actually stored internally.

**Rest Timer**
A rest countdown starts automatically when you enter reps for a set, or you can start it with the ⏱ Rest button on any exercise. Pick 1:00, 1:30, 2:00 or 3:00 (your choice is remembered), nudge it ±15 seconds, or skip. When it ends the phone vibrates and beeps. Auto-start can be turned off from the timer itself.

**Backup & Restore**
From the History tab you can export everything (program, history, header, unit) to a `.json` backup file, export your history as a `.csv` spreadsheet, or import a backup. Imports can either merge sessions into your current history or replace everything. No Google account required.
