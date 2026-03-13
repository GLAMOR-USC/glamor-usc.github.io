# Updating the GLAMOR Lab Website

First clone this repo. To test any changes before pushing them, run `php -S localhost:8080`.

## Adding people

You will need to periodically update the lab members. This includes updating current PhD students, asking the PhD students and Jesse if they have any UG/MS collaborators who need to be added to the website, and moving any former members to the alumni category.

In the `people/` directory, you will find `.js` files for 5 lab member categories:

- `phd.js`: For current PhD students. Most fields are self-explanatory. For `ws` and `ws_themes`, ask people what [world scope]() their research belongs to. Also note how I added co-advisors.
- `ug_ms.js`: For current undergraduate and Masters students who are either being mentored by a PhD student or working directly with Jesse (if the latter, then leave the `phd_mentor` field empty).
- `alumni_phd.js`: For graduated PhD students. You will have to add ~5 people in May.
- `alumni_ugms.js`: For UG/MS students who are no longer collaborating with the lab. When updating `ug_ms.js`, check whether the current students are still collaboraing with their mentors/Kesse, and if not, move them here.
- `alumni_visiting.js`: For students visiting from other universities or through some outreach program. You don't need to worry about this for now.

For all current lab members (PhD and UG/MS), you can ask them to share a square photo of themselves, which you should save in `glamor_photos/`. Feel free to delete photos of alumni.

For now, you can start by:
1. Asking Jesse who all needs to be added to the PhD students section: I think it is you, Zizhao, Jie, Yuliang, and maybe Gabriela, but he can confirm. Then ask each of these students for the required information (you can share `https://glamor-usc.github.io/people.html` to show what the website looks like for current students)
2. Send a message on `#glamor-lab` asking the other PhD students and Jesse if they have any UG/MS collaborators who need to be added to the website, and check whether any of the current students on there need to be moved to the alumni section by asking the corresponding PhD mentor.

## Adding papers

You will also periodically need to ask people to share any papers (either pre-print or accepted to conferences) that have not been added to the lab website. The current policy is that we only add papers that Jesse is an author on (e.g. if you are collaborating with someone outside on a project and Jesse is not on the paper, do not add it).

You can update the papers in `publications.js`. The fields are mostly self-explanatory. Some pointers: 
- If a paper is only a pre-print, set the `year` field to "Pre-Prints". Once it becomes a publication, set `year` to the year of the conference it was published in.
- Add `<b>...</b>` around the names of lab members in the author list.
- If you are linking to arxiv, add a link to the abstract and not the pdf.

For now, you can start by asking all PhD students to check the [publications page](https://glamor-usc.github.io/publications.html) and ask them if any papers need to be added or updated (e.g. pre-print -> accepted at a conference).

## Adding lab news

I haven't updated this in a while, but typically we "announce" any new publications/lab achievements here. You can update this in line 258 of `index.html` by adding another `<li>...</li>` element.
