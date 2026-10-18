# Semester 1 Timetable and Study Plan

A simple one-page timetable and study planner for Semester 1, session 2026/2027, USM School of Computer Sciences (Intelligent Computing), tutorial and lab Group A.

It works as a normal web page. There is nothing to install and no build step. Open `index.html` and it runs.

## Credits

The original timetable and study plan was made by **[Baswara](https://github.com/baswarahm)**.
This project is a fork of [baswarahm/sms1](https://github.com/baswarahm/sms1). Most of the credit for the design and the course data goes to him.

The same credit is shown inside the page. Click the small `<.` button at the top right.

## What the page does

- **Timetable:** a weekly grid (and a day-by-day list on phones). Click a block to see its venue and notes. A "next class" strip at the top shows what is coming up.
- **Weekly plan:** a checklist for each of the 16 weeks, with topics per course. Ticks are saved in your own browser only.
- **Deadlines:** tests, assignments, holidays and the mark breakdown for each course, plus rules that can cost marks.
- **Free resources:** free learning links for each course.
- **Footer quotes:** a random motivational or reality-check line every time you open the page. Some come from a built-in list and some come live from [DummyJSON](https://dummyjson.com/docs/quotes). If you are offline, only the built-in ones show.

## What this fork changes

- Added **LSP201 English** and **LKM400 Bahasa Malaysia** (2 units each), plus the **Bengkel Siswa** workshop slot.
- The **Tuesday common lab is off by default**. Tick the box above the timetable to show it.
- Updated **CCA101** test and assessment times and venues (DUP C).
- Moved **CCA102 Test 1** to Thursday 5 Nov 2026, 8:30-9:30am, DUP C. This was agreed between the lecturer and the students, so it differs from the original course planner.
- Added a credits box and a link to [myCSD](https://mycsd.javanmyna.fyi).
- Replaced the footer with random quotes.

The weekly plan and resources still cover only the four original courses: CKC111, CCA101, CCA102 and SHE102 (this fork uses SHE102 in place of SHE102). LKM400 (BM) and LSP201 (English) also have their marks, deadlines, attendance rules and study tips, but no week-by-week plan.

## Using it

**On your computer or phone:** download `index.html` and open it in any modern browser. An internet connection is only needed for the fonts and the live quotes.

**As a website (GitHub Pages):**
1. Push the repo to GitHub.
2. Go to **Settings > Pages**.
3. Under "Build and deployment", choose **Deploy from a branch**, pick your main branch and the root folder, then save.
4. After a minute or two the page is live at `https://<your-username>.github.io/<repo-name>/`.

## Changing the schedule

Everything lives in `index.html`. The data is near the top of the `<script>` section, so you rarely need to touch the rest.

| To change | Look for |
|---|---|
| Course names, lecturers, units | `COURSES` |
| Class times and venues | `BLOCKS` (days are numbered from 0, so Monday is 0 and Friday is 4) |
| A class with a day and venue but no time yet | `UNTIMED`, then move it to `BLOCKS` once you know the time |
| Tests, assignments and holidays | `DEADLINES` |
| Weekly topics | `TOPICS` |
| Footer quotes | `QUOTES` |

Times are written as 24-hour `'HH:MM'`, for example `'16:00'`.

## Things to confirm

- The CCA101 planner this was built from is headed session 2025/2026, so confirm its times on USM eLearning.
- The release date of the CCA101 report-based assessment is not confirmed. The planner says Wednesday 11 Nov 2026, but the page currently shows 10 Nov.
- Several test dates are still "to be announced" in the source planners, and the page says so instead of guessing.

## Note on CCA102 Test 1

The date was changed on purpose. If you see 12 Nov in an older copy of the planner, the correct date is **Thursday 5 Nov 2026**. A comment next to the entry in `index.html` says the same, so nobody changes it back by mistake.