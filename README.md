# Explore India

A static travel site showcasing destinations across India — built for DevOps Lab 1 to practice Git branching, merging, conflict resolution, and pull requests.

## Team

| Name | Contribution |
|---|---|
| Kuheli Begum | Built the gallery page (`feature/gallery-page`), resolved the header-color merge conflict |
| Saurabh Burnwal | Added the Ladakh destination card (`feature/ladakh-card`), reviewed and merged gallery-page PR |

Both teammates authored at least one feature branch, opened a pull request, reviewed and merged the other's pull request, and worked through the same merge conflict together.

## Branching strategy

We used short-lived feature branches off `main`, merged only through pull requests (direct pushes to `main` are blocked by branch protection).

**Naming convention:**
- `feature/<description>` — new functionality (`feature/gallery-page`, `feature/ladakh-card`)
- `conflict/<description>` — branches created deliberately to practice conflict resolution
- `fix/<description>` — fixes, including conflict resolutions (`fix/header-color-conflict`)
- `docs/<description>` — documentation changes (`docs/readme`)

## Header color conflict

While practicing merge conflicts, both teammates changed the header background color on separate branches off the same commit — Kuheli set it to navy (`#000080`), Saurabh set it to green (`#138808`). Merging both into `main` produced a real conflict in `css/style.css`.

Resolved together by combining both colors into a horizontal gradient instead of picking one:

```css
header{
    background: linear-gradient(90deg, #000080, #138808);
}
```

The fix went through its own pull request (`fix/header-color-conflict`), reviewed and merged by Saurabh.

## What we learned

- **Kuheli:** [one or two lines, in your own words — e.g. what resolving the conflict taught you]
- **Saurabh:** [his line]

## Running locally

No build step or dependencies — it's a static site. Open `index.html` in a browser.