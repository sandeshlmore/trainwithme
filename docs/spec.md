# TRAIN RIGHT — Product Specification

## Product intent

TRAIN RIGHT is a premium, form-first gym workout companion. It helps people train safely and consistently through a six-day Push / Pull / Legs program, clear exercise coaching, progression tracking, and recovery reminders.

**Tagline:** Train right. Lift hard. Stay consistent.

**Core principle:** Train hard. Train smart. Form first.

## Technical constraints

- Pure HTML, CSS, and vanilla JavaScript.
- No framework, UI library, backend, or external video dependency.
- The site must run by opening `index.html` locally.
- Persist workout tracking in `localStorage`.

## Visual direction

- Near-black / charcoal background; deep gray cards.
- Bright lime green primary accent, white text, muted gray supporting text, and orange/red warnings.
- Minimal, premium, athletic, spacious interface with rounded cards, subtle borders, and restrained hover animation.
- Responsive from mobile to desktop.

Suggested palette:

```css
--background: #0b0d0c;
--card: #141715;
--accent: #b6ff3b;
--text: #f5f7f3;
--muted: #929a92;
--danger: #ff5d5d;
```

## Homepage

- Brand: **TRAIN RIGHT**
- Hero heading: **BUILD YOUR BEST VERSION.**
- Explain the focus on progressive overload, proper form, controlled reps, recovery, and consistency.
- Primary CTA scrolls to the workout plan.
- Surface the six training days, exercise count, and form-first philosophy.

## Weekly program

Use a Push / Pull / Legs split twice weekly:

| Day | Focus | Exercises |
| --- | --- | --- |
| 1 | Push | Barbell Bench Press; Incline Dumbbell Press; Overhead Shoulder Press; Lateral Raises; Triceps Pushdown |
| 2 | Pull | Lat Pulldown; Seated Cable Row; Chest Supported Row; Face Pull; Dumbbell Curl |
| 3 | Legs | Barbell Squat; Romanian Deadlift; Leg Press; Leg Curl; Standing Calf Raise |
| 4 | Push | Incline Barbell Press; Machine Chest Press; Cable Fly; Lateral Raises; Overhead Triceps Extension |
| 5 | Pull | Pull Ups; One Arm Dumbbell Row; Reverse Fly; Face Pull; Hammer Curl |
| 6 | Legs | Hack Squat; Bulgarian Split Squat; Hip Thrust; Leg Extension; Seated Calf Raise |
| 7 | Rest | Rest and recovery |

## Required interaction

- Day navigation for Days 1–6 and Rest; switch content without reloading.
- Keyboard shortcuts `1`–`7` select the matching day.
- Search exercise names and target-muscle labels.
- Filter exercises by All, Chest, Back, Shoulders, Arms, and Legs.
- Show workout progress as completed exercises, percentage, and an animated progress bar.
- Each exercise can be marked complete, with a visual completed state.

## Exercise card requirements

Every card includes:

- Exercise name and target muscles.
- Prescription: sets, rep range, rest, and difficulty.
- Completion checkbox.
- Expandable **How to perform** guide with smooth motion.
- A CSS/SVG/HTML animated demonstration that communicates posture and range of motion without external video.
- Starting position, movement, breathing, tempo, concise form cues, and common mistakes.
- Common mistakes use warning styling and discourage ego lifting, uncontrolled momentum, shortened range, and loss of neutral spine.
- Editable per-set weight and reps, plus adding/removing sets.

## Progression and history

- Persist logs and completion state locally.
- When available, show a prior workout benchmark.
- Recommend a small load increase only after the user reaches the top of the prescribed rep range with clean form across all sets.
- Explicitly advise maintaining or reducing load if technique degrades.

## Support content

### Warm up

Collapsible guidance: 5–10 minutes of light cardio, dynamic movement, then 2–4 progressive warm-up sets for the first compound movement. Clarify that warm-up sets are not working sets.

### Recovery matters

Keep it concise: sleep 7–9 hours, hydrate, eat enough for the goal, take rest days seriously, and never train through sharp pain.

### TRAIN RIGHT rules

1. Form over weight
2. Full controlled reps
3. Do not ego lift
4. Progressive overload
5. Track workouts
6. Recover properly
7. Consistency beats motivation

## Rest timer

- Floating, unobtrusive timer.
- Presets: 60, 90, 120, and 180 seconds.
- Start, pause, and reset actions.
- On zero, show `GO` with a subtle visual notification; no sound by default.
