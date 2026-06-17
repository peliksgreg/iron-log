# iron-log

**Iron Log** is a single-file web app (one HTML file, no backend) for tracking strength training, built around a 4-5 day workout split with a strong personalization layer on top.

At its core, it's a workout logger: each training day shows a list of exercises with target rep ranges, input fields for weight and reps per set, and a "last time" comparison so you can see exactly what you did last session before you try to beat it. Saving a session checks every exercise against your all-time best using an estimated one-rep-max formula and flags a PR badge when you've topped it, with separate handling for bodyweight moves like pull-ups and push-ups, where reps rather than load are the real progress signal.

**Personalize Wizard**
A personalization wizard asks five questions, your goal, experience level, training days per week, available equipment, and an optional focus muscle, then generates a tailored split by pulling from a tagged exercise database, with a 10-second animated loading screen and rotating motivational text while it works. It launches automatically for first-time users and can be rerun anytime, offering to replace or merge with whatever program you already have.

**Weekly Progress**
The app also gives you a weekly progress view showing how many of your program days you've completed since Monday, with checkmarks on the nav tabs themselves, and progression suggestions that analyze your session history to nudge you toward adding weight (if you've hit the top of your rep range twice running) or taking a deload (if you've stalled for three sessions). History itself supports full editing: you can fix or delete any individual past session, not just wipe everything at once.

**Track on the Go**
For persistence, everything saves locally in the browser by default, with optional Google Drive sync (via OAuth) so your program, history, and header text follow you across devices. There's also a click-to-edit header for naming the app yourself, and a unit toggle that displays everything in lb or kg without touching how data is actually stored internally.
