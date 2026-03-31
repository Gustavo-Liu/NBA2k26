
## Skill routing

When the user's request matches an available skill, ALWAYS invoke it using the Skill
tool as your FIRST action. Do NOT answer directly, do NOT use other tools first.
The skill has specialized workflows that produce better results than ad-hoc answers.

Key routing rules:
- Product ideas, "is this worth building", brainstorming → invoke office-hours
- Bugs, errors, "why is this broken", 500 errors → invoke investigate
- Ship, deploy, push, create PR → invoke ship
- QA, test the site, find bugs → invoke qa
- Code review, check my diff → invoke review
- Update docs after shipping → invoke document-release
- Weekly retro → invoke retro
- Design system, brand → invoke design-consultation
- Visual audit, design polish → invoke design-review
- Architecture review → invoke plan-eng-review

## Project status

This repo currently contains a single-file shot meter prototype in `shot-meter.html`.

Implemented so far:
- Adjustable green window rating from `60` to `99`
- Dynamic green release window scaling from the current `48-52` baseline up to `40-60` at rating `99`
- Adjustable release speed from `300ms` to `1200ms`
- Desktop keyboard input with `Space`
- Mobile/touch support using press to hold and release to shoot
- On-screen controls and status text for current green window and release speed

Behavior notes:
- Lower `fillMs` is faster; higher `fillMs` is slower
- Rating `60` matches the original tight window
- Rating `99` uses the widest current green window: `40-60`
