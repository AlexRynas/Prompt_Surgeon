Prompt Tips for Image‑to‑Video (Expanded Guide)

Updated: 2025‑10‑03 • Scope: KlingAI and similar I2V tools

# Overview

This guide synthesizes proven prompting patterns from your examples and refactors the original “Prompt Tips for Image to Video” section into a practical, copy‑ready structure. It focuses on preventing drift, preserving the first frame, and specifying small, cinematic movements that render reliably across image‑to‑video models.

# 1) Master Formula

**Prompt = \[Mode & Continuity Locks\] + \[Duration & Framing\] + \[Subject & Look\] + \[Action Timeline\] + \[Camera Plan\] + \[Environment & Lighting\] + \[Physics & Interaction Rules\] + \[Quality & Lens\] + \[Negatives (Prohibitions)\]**

This extends the classic Subject + Movement + Scene/Background + Camera + Lighting + Atmosphere recipe with the practical guardrails that consistently reduce artifacts and identity drift.

# 2) Components (What to Write & Why)

**A. Mode & Continuity Locks (first line) —** State “Image‑to‑video; use the uploaded photo as the exact first frame. Lock identity, outfit, props, background, composition, and aspect ratio; forbid restyle/reframe.” This sets the non‑negotiable guardrails.

**B. Duration & Framing —** Pick ~5–10 seconds. Add “no crop/wobble; subject centered,” or lock the camera entirely. Shorter clips reduce failure modes and keep motion readable.

**C. Subject & Look (concise) —** In one or two lines: who/what, wardrobe/props, and expression. Avoid style adjectives that imply restyling unless that is desired.

**D. Action Timeline (beats) —** Write a mini‑timeline with seconds and micro‑motions: breathing, blinks, eye saccade, small head/hand moves; one focal action; return to start. Localize effects (e.g., “hair moves only where touched”).

**E. Camera Plan —** Either lock the camera or specify a single subtle move with magnitude and path, e.g., “micro‑dolly push‑in 3–4% with ~5° arc.” Small moves read cinematic; big moves cause warps. If you need shorthand, use: Horizontal, Vertical, Zoom, Pan, Tilt, Roll.

**F. Environment & Lighting —** One sentence on setting and one on light quality/direction; keep both stable to prevent scene swaps.

**G. Physics & Interaction Rules —** Call out constraints like “no secondary drift,” “garments/hair react only to contact,” “walk cycle slow and natural,” “no cuts.” These improve anatomical correctness and continuity.

**H. Quality & Lens —** Optionally add lens/DOF language (e.g., “virtual 85mm, shallow DOF, smooth motion”). Keep it to a single line—over‑specifying can confuse the model.

**I. Negatives (Prohibitions) —** A single line of “No …” to block common glitches: no camera shake, no ghosting, no motion blur, no distortion, no text/logos, no extra characters, no reframing, no cuts.

# 3) Writing Guidelines (Refined)

*   Use simple, concrete verbs (breathe, blink, glance, turn, lift, stroke). Repeat a verb if it is critical.
*   Prefer one focal action over many competing motions—reduces identity loss and clutter.
*   Avoid exact counts for background items; describe patterns instead (prevents overly literal restyling).
*   Keep scope small for 5–10s outputs; complex ballistics or multiple scene changes often break.
*   Use a “sequence of frames” or second‑marked timeline when you need a clear, stepwise arc.

# 4) Ready‑to‑Use Templates

## A) Minimal “Safe” Template

Image‑to‑video. Use the uploaded photo as the exact first frame. Preserve identity, outfit, props, background, composition, aspect ratio. No restyle, no reframing.  
  
Duration 8–10s. Camera locked (or: micro‑dolly push‑in ~3–4% with slight rightward arc ~5°). No crop or wobble; subject stays centered.  
  
Timeline: 0–1s hold + natural breathing; 1–3s eyes glance \[direction\]; 3–6s \[one focal action—e.g., right hand lifts to hair, single gentle stroke; hair moves only where touched\]; 6–8s return to start; 8–10s hold, optional soft blink.  
  
Lighting stays \[e.g., warm sunset\], environment unchanged.  
  
No camera shake, no ghosting, no motion blur, no distortion, no extra characters, no cuts.

## B) Pro “Timeline” Template

Mode/Locks: Photoreal image‑to‑video. First frame = source. Preserve identity, outfit, props, background, composition, AR. No restyle/reframe.  
  
Camera: Ultra‑smooth micro‑dolly push‑in ~3–4% from 0–8s with subtle \[yaw/arc\]; hold 8–10s. No crop/wobble; subject centered.  
  
Timeline (10s):  
0–1s: hold pose, tiny breathing, soft blink ~0.8s.  
1–3s: eyes look \[direction\]; head turn ~20–25° \[direction\]; body still.  
3–6s: \[focal action—e.g., hand lifts to hair, single stroke; hair moves only where touched\].  
6–8s: hand lowers; head/eyes return to camera.  
8–10s: match original pose; optional blink ~9.2s.  
  
Lighting/Scene: \[keep original | specify stable light\].  
Lens/Look: \[e.g., virtual 85mm, shallow DOF, smooth motion\].  
Negatives: No shake, no ghosting, no motion blur, no distortion, no text/logos, no extra characters, no cuts.

# 5) Camera Movement Cheat‑Sheet

*   Lock the camera for facial close‑ups and identity‑critical shots.
*   Use one subtle move max for short clips: micro‑dolly push‑in/out, slight arc, or gentle pan/tilt (avoid stacking).
*   Shorthand verbs: Horizontal, Vertical, Zoom, Pan, Tilt, Roll.

# 6) Troubleshooting Rules

**Faces drifting / identity loss?** Move continuity locks to the first line; reduce camera motion; shorten the timeline; keep one focal action.

**Artifacts / ghosting?** Strengthen the Negatives block; remove overlapping motions; slow the focal action; keep background fixed.

**Over‑stylization?** Delete style adjectives that imply restyle; keep look constraints only in Lighting/Lens and add “No restyle.”

**Wobble / reframing?** Add “No crop/wobble; subject centered.” Lock the camera or reduce the move magnitude to ≤4%.