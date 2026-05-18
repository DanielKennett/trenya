<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no, viewport-fit=cover">
<meta name="theme-color" content="#181411">
<meta name="application-name" content="Треня">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Треня">
<link rel="manifest" href="./manifest.webmanifest">
<link rel="apple-touch-icon" href="./icon-192.png">
<title>треня</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Geist:wght@400;500;600;700;800&family=Geist+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    /* Palette — warm dark, single accent */
    --bg:        oklch(0.135 0.006 50);
    --bg-soft:   oklch(0.165 0.007 55);
    --surface:   oklch(0.185 0.008 55);
    --surface-2: oklch(0.215 0.009 55);
    --line:      oklch(0.265 0.010 55);
    --line-soft: oklch(0.225 0.009 55);

    --fg:        oklch(0.965 0.004 80);
    --fg-2:      oklch(0.78  0.008 70);
    --fg-3:      oklch(0.60  0.010 65);
    --fg-4:      oklch(0.46  0.010 60);

    --ember:     oklch(0.755 0.165 55);
    --ember-2:   oklch(0.66  0.165 50);
    --ember-soft:oklch(0.755 0.165 55 / 0.14);
    --ember-line:oklch(0.755 0.165 55 / 0.35);

    --good:      oklch(0.78 0.14 145);
    --good-soft: oklch(0.78 0.14 145 / 0.14);
    --bad:       oklch(0.68 0.18 25);
    --bad-soft:  oklch(0.68 0.18 25 / 0.14);
    --info:      oklch(0.78 0.10 240);
    --info-soft: oklch(0.78 0.10 240 / 0.14);
    --gold:      oklch(0.85 0.13 95);
    --gold-soft: oklch(0.85 0.13 95 / 0.16);

    --r-sm: 10px; --r-md: 14px; --r-lg: 18px; --r-xl: 22px;
    --pad: 18px;
    --nav-h: 64px;
    --num: "Geist Mono", ui-monospace, "SF Mono", Menlo, monospace;
    --sans: "Geist", -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
  }

  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
  html, body {
    background: var(--bg); color: var(--fg);
    font-family: var(--sans); font-size: 16px; line-height: 1.4;
    overflow-x: hidden; min-height: 100vh; min-height: 100dvh;
    font-feature-settings: "ss01", "cv11";
    -webkit-font-smoothing: antialiased; text-rendering: optimizeLegibility;
  }
  body {
    padding: env(safe-area-inset-top) 0 calc(var(--nav-h) + 24px + env(safe-area-inset-bottom)) 0;
    background:
      radial-gradient(80% 50% at 50% -10%, oklch(0.755 0.165 55 / 0.10), transparent 60%),
      var(--bg);
  }

  /* Tabular numbers everywhere data flows */
  .tnum, input[type=number], .num, .mono { font-variant-numeric: tabular-nums; font-feature-settings: "tnum"; }
  .mono { font-family: var(--num); }

  /* ============ NAV — bottom tab bar ============ */
  .nav {
    position: fixed; left: 0; right: 0; bottom: 0;
    display: grid; grid-template-columns: repeat(var(--nav-count, 3), 1fr);
    gap: 2px; padding: 8px 8px calc(8px + env(safe-area-inset-bottom));
    background: oklch(0.135 0.006 50 / 0.85);
    backdrop-filter: blur(18px) saturate(140%);
    -webkit-backdrop-filter: blur(18px) saturate(140%);
    border-top: 1px solid var(--line-soft);
    z-index: 50;
  }
  .nav-btn {
    appearance: none; background: transparent; border: 0; cursor: pointer;
    display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 3px;
    padding: 8px 1px 6px; border-radius: 12px;
    color: var(--fg-3); font-family: var(--sans); font-size: 8px; font-weight: 600;
    letter-spacing: 0.01em;
    transition: color .15s, background .15s;
  }
  .nav-btn svg { width: 20px; height: 20px; stroke-width: 1.8; }
  .nav-btn.active { color: var(--ember); }
  .nav-btn.active svg { stroke: var(--ember); }
  .nav-btn:active { background: var(--surface); }
  .nav-btn.section-hidden { display: none; }

  .screen { padding: 14px var(--pad) 0; display: none; max-width: 480px; margin: 0 auto; transform-origin: 50% 24px; }
  .screen.active { display: block; }
  .reveal-item { will-change: transform, opacity; }
  .tap-anim { position: relative; overflow: hidden; }
  .tap-ripple {
    position: absolute; width: 16px; height: 16px; border-radius: 999px;
    pointer-events: none; background: currentColor; opacity: .16;
    transform: translate(-50%, -50%) scale(0);
    mix-blend-mode: screen;
  }
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: .001ms !important;
      animation-iteration-count: 1 !important;
      scroll-behavior: auto !important;
      transition-duration: .001ms !important;
    }
  }

  /* ============ Typography ============ */
  h1 { font-size: 34px; font-weight: 700; letter-spacing: -0.025em; line-height: 1.05; margin-bottom: 4px; }
  h2 { font-size: 13px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase;
       color: var(--fg-3); margin: 28px 0 12px; }
  .subtitle { color: var(--fg-3); font-size: 14px; margin-bottom: 22px; letter-spacing: -0.01em; }
  #screen-workout h1 { font-size: 23px; line-height: 1.12; margin-bottom: 2px; }
  #screen-workout .subtitle { font-size: 12px; margin-bottom: 12px; }
  .eyebrow { font-family: var(--num); font-size: 10px; font-weight: 600;
             letter-spacing: 0.12em; text-transform: uppercase; color: var(--fg-4); }
  .label   { font-family: var(--num); font-size: 10px; font-weight: 600;
             letter-spacing: 0.10em; text-transform: uppercase; color: var(--fg-3); }

  /* ============ DASHBOARD ============ */
  .hero {
    position: relative; overflow: hidden;
    background: var(--surface); border: 1px solid var(--line);
    border-radius: var(--r-xl); padding: 20px;
    margin-bottom: 14px;
    display: grid; grid-template-columns: 96px 1fr; gap: 18px; align-items: center;
  }
  .ring { width: 96px; height: 96px; position: relative; }
  .ring svg { width: 100%; height: 100%; transform: rotate(-90deg); }
  .ring-track { stroke: var(--line); }
  .ring-prog  { stroke: var(--ember); stroke-linecap: round;
                transition: stroke-dashoffset .6s cubic-bezier(.2,.7,.2,1); }
  .ring-num   { position: absolute; inset: 0; display: flex; flex-direction: column;
                align-items: center; justify-content: center; gap: 5px; padding-top: 2px;
                font-family: var(--num); font-weight: 700; font-size: 22px;
                line-height: 1; letter-spacing: 0; text-align: center; }
  .ring-num small { display: block; font-size: 9px; font-weight: 600; line-height: 1;
                    letter-spacing: 0.10em; color: var(--fg-3); text-transform: uppercase; }
  .hero-meta .eyebrow { margin-bottom: 6px; }
  .hero-meta .h-title { font-size: 22px; font-weight: 700; letter-spacing: -0.02em; line-height: 1.15; }
  .hero-meta .h-sub   { font-size: 12px; color: var(--fg-3); margin-top: 6px;
                        font-family: var(--num); letter-spacing: 0.02em; }

  .cta {
    appearance: none; cursor: pointer; border: 1px solid var(--ember-line);
    background:
      linear-gradient(180deg, oklch(0.755 0.165 55 / 0.18), oklch(0.755 0.165 55 / 0.08)),
      var(--surface);
    color: var(--fg); width: 100%; padding: 18px 20px; border-radius: var(--r-lg);
    display: flex; align-items: center; gap: 14px;
    text-align: left; margin-bottom: 14px;
    transition: transform .08s, background .15s;
  }
  .cta:active { transform: scale(0.99); }
  .cta-arrow { width: 40px; height: 40px; border-radius: 12px; flex-shrink: 0;
               display: grid; place-items: center; background: var(--ember); color: var(--bg); }
  .cta-arrow svg { width: 20px; height: 20px; stroke-width: 2.4; }
  .cta-text { flex: 1; min-width: 0; }
  .cta-eyebrow { font-family: var(--num); font-size: 10px; font-weight: 600;
                 letter-spacing: 0.12em; text-transform: uppercase; color: var(--ember); margin-bottom: 3px; }
  .cta-title { font-size: 17px; font-weight: 700; letter-spacing: -0.015em; }

  .stat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 10px; }
  .stat {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 14px 14px 12px;
    display: flex; flex-direction: column; gap: 6px;
  }
  .stat-val { font-family: var(--num); font-size: 26px; font-weight: 700;
              letter-spacing: -0.025em; line-height: 1; }
  .stat-val .unit { font-size: 13px; color: var(--fg-3); font-weight: 500; margin-left: 4px; letter-spacing: 0; }
  .stat-lbl { font-family: var(--num); font-size: 10px; font-weight: 600;
              letter-spacing: 0.10em; text-transform: uppercase; color: var(--fg-3); }
  .stat-date { font-family: var(--num); font-size: 10px; color: var(--fg-4); margin-top: -1px; letter-spacing: 0.02em; }
  .stat .flame { color: var(--ember); }
  .burned-calories { color: var(--good) !important; }
  .burned-calories .unit { color: var(--good) !important; opacity: .85; }
  .dash-links {
    display: grid; grid-template-columns: 1fr 1fr; gap: 8px;
    margin: 0 0 14px;
  }
  .dash-link {
    appearance: none; border: 1px solid var(--line-soft);
    background: var(--surface); color: var(--fg);
    border-radius: var(--r-md); padding: 12px;
    min-height: 58px; cursor: pointer; font-family: var(--sans);
    display: flex; align-items: center; gap: 10px; text-align: left;
    transition: transform .08s, background .15s, border-color .15s;
  }
  .dash-link:active { transform: scale(.985); background: var(--surface-2); }
  .dash-link svg {
    width: 20px; height: 20px; flex-shrink: 0;
    stroke: var(--ember); stroke-width: 1.9;
  }
  .dash-link span { font-size: 14px; font-weight: 700; letter-spacing: -0.01em; }

  .deload-banner {
    background: var(--gold-soft); border: 1px solid oklch(0.85 0.13 95 / 0.3);
    border-radius: var(--r-md); padding: 14px 16px; margin-bottom: 14px;
    font-size: 13px; color: var(--gold); line-height: 1.55;
    display: flex; gap: 12px; align-items: flex-start;
  }
  .deload-banner b { color: oklch(0.95 0.12 95); font-weight: 600; }
  .deload-icon { flex-shrink: 0; width: 24px; height: 24px; border-radius: 8px;
                 background: var(--gold-soft); color: var(--gold); display: grid; place-items: center;
                 font-family: var(--num); font-weight: 700; font-size: 14px; }
  .dash-calendar-head {
    display: flex; justify-content: space-between; align-items: baseline;
    gap: 10px; margin: 28px 0 12px;
  }
  .dash-calendar-head h2 { margin: 0; }
  .dash-calendar-range {
    font-family: var(--num); font-size: 10px; color: var(--fg-4);
    text-transform: uppercase; font-weight: 700; letter-spacing: 0.04em;
  }
  .dash-calendar-scroll {
    overflow-x: auto; margin: 0 calc(var(--pad) * -1) 14px;
    padding: 0 var(--pad) 6px; scrollbar-width: none;
    scroll-snap-type: x proximity; -webkit-overflow-scrolling: touch;
    -ms-overflow-style: none;
  }
  .dash-calendar-scroll::-webkit-scrollbar { display: none; }
  .dash-calendar {
    display: flex; gap: 6px; width: max-content;
  }
  .cal-day {
    width: 58px; min-height: 78px; border-radius: 12px; padding: 8px 5px;
    background: var(--surface); border: 1px solid var(--line-soft);
    display: grid; grid-template-rows: auto auto 10px 1fr; gap: 3px; align-items: start;
    scroll-snap-align: start;
  }
  .cal-day.today { border-color: var(--ember-line); box-shadow: inset 0 0 0 1px var(--ember-line); }
  .cal-day.done { background: var(--good-soft); border-color: oklch(0.78 0.14 145 / 0.35); }
  .cal-day.planned { border-color: var(--ember-line); }
  .cal-day.muted { opacity: .45; }
  .cal-weekday {
    font-family: var(--num); font-size: 9px; color: var(--fg-4);
    text-transform: uppercase; font-weight: 700; text-align: center; letter-spacing: 0;
  }
  .cal-num {
    font-family: var(--num); font-size: 17px; font-weight: 800;
    color: var(--fg); text-align: center; line-height: 1.1;
  }
  .cal-today-label {
    font-family: var(--num); font-size: 8px; font-weight: 800;
    color: var(--ember); text-transform: uppercase; text-align: center;
    line-height: 1; letter-spacing: 0;
  }
  .cal-workout {
    align-self: end; min-height: 22px; color: var(--fg-3);
    font-size: 9px; font-weight: 700; line-height: 1.15;
    text-align: center; word-break: normal; overflow-wrap: anywhere;
  }
  .cal-day.done .cal-workout { color: var(--good); }
  .cal-day.planned .cal-workout { color: var(--ember); }

  /* ============ WORKOUT ============ */
  .week-bar {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 10px 12px; margin-bottom: 12px;
    display: flex; align-items: center; gap: 12px;
  }
  .week-bar-left { flex: 1; }
  .week-bar .label { margin-bottom: 4px; }
  .week-bar-big {
    font-family: var(--num); font-size: 15px; font-weight: 700;
    color: var(--fg); letter-spacing: -0.01em;
  }
  .week-bar-big em { color: var(--ember); font-style: normal; }
  .week-bar-right { display: flex; align-items: center; gap: 6px; }
  .week-step { width: 36px; height: 36px; border-radius: 10px;
               background: var(--surface-2); border: 1px solid var(--line-soft);
               color: var(--fg-2); cursor: pointer;
               display: grid; place-items: center; font-size: 16px; font-weight: 600; }
  .week-step:active { background: var(--line); }
  .week-num-input {
    background: var(--surface-2); border: 1px solid var(--line-soft); color: var(--fg);
    width: 48px; padding: 8px 0; border-radius: 10px; text-align: center;
    font-family: var(--num); font-size: 15px; font-weight: 700;
  }
  .week-num-input:focus { outline: none; border-color: var(--ember); }

  .day-selector { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 8px; margin-bottom: 10px; }
  .day-btn {
    appearance: none; cursor: pointer; position: relative;
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 14px 8px;
    color: var(--fg); font-family: var(--sans); font-weight: 600;
    display: flex; flex-direction: column; align-items: center; gap: 2px;
    transition: background .12s, border-color .12s, transform .08s;
  }
  .day-btn:active { transform: scale(0.98); }
  .day-btn .d-label { font-size: 15px; letter-spacing: -0.01em; }
  .day-btn .d-sub   { font-size: 10px; font-weight: 500; color: var(--fg-3);
                      font-family: var(--num); letter-spacing: 0.04em; text-transform: uppercase; }
  .day-btn.active { background: var(--ember); border-color: var(--ember); color: var(--bg); }
  .day-btn.active .d-sub { color: oklch(0.20 0.04 50); }
  .day-btn.suggested { padding-top: 24px; }
  .day-btn.suggested::after {
    content: attr(data-badge); position: absolute; top: 6px; left: 50%; transform: translateX(-50%);
    background: var(--good); color: var(--bg);
    font-family: var(--num); font-size: 9px; font-weight: 700;
    line-height: 1; letter-spacing: 0.08em; text-transform: uppercase;
    padding: 4px 8px; border-radius: 999px; white-space: nowrap; z-index: 2;
    box-shadow: 0 2px 8px oklch(0 0 0 / 0.25);
  }
  .day-btn.next-up::after { background: var(--ember); }

  /* ============ EXERCISE CARD ============ */
  .exercise {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-lg); margin-bottom: 14px; overflow: hidden;
  }
  .exercise-header {
    padding: 14px 16px 12px;
    display: flex; justify-content: space-between; align-items: flex-start; gap: 12px;
  }
  .exercise-name { font-size: 16px; font-weight: 600; letter-spacing: -0.01em; line-height: 1.25; }
  .exercise-target { font-family: var(--num); font-size: 11px; color: var(--fg-3);
                     margin-top: 4px; letter-spacing: 0.03em; }
  .ex-toolbar {
    display: flex; gap: 4px; padding: 0 12px 10px; border-bottom: 1px solid var(--line-soft);
  }
  .icon-btn {
    appearance: none; background: var(--surface-2); color: var(--fg-2);
    border: 1px solid var(--line-soft); border-radius: 8px;
    padding: 7px 11px; font-size: 13px; font-weight: 600; cursor: pointer;
    line-height: 1; display: inline-flex; align-items: center; gap: 4px;
    font-family: var(--sans);
  }
  .icon-btn:active { background: var(--line); }
  .icon-btn:disabled { opacity: 0.3; }
  .pr-badge {
    display: inline-flex; align-items: center; gap: 3px;
    background: var(--gold-soft); color: var(--gold);
    font-family: var(--num); font-size: 10px; font-weight: 700;
    padding: 2px 7px; border-radius: 6px; margin-left: 8px;
    letter-spacing: 0.05em;
  }
  .draft-banner {
    background: var(--info-soft); border: 1px solid oklch(0.78 0.10 240 / 0.32);
    color: var(--info); border-radius: var(--r-md);
    padding: 12px; margin-bottom: 14px; display: grid; gap: 10px;
    font-size: 13px; line-height: 1.45;
  }
  .draft-actions { display: flex; gap: 8px; }
  .draft-actions button {
    flex: 1; padding: 10px; border-radius: 10px;
    background: var(--surface); color: var(--fg);
    border: 1px solid var(--line-soft); font-family: var(--sans);
    font-weight: 700; cursor: pointer;
  }
  .draft-actions button:last-child { color: var(--bad); }

  .sets { padding: 4px 0 2px; }
  .header-labels {
    display: grid; grid-template-columns: 26px minmax(0,1fr) minmax(0,1fr) 44px 40px 48px; gap: 5px;
    padding: 10px 14px 6px;
    font-family: var(--num); font-size: 10px;
    color: var(--fg-4); text-transform: uppercase; letter-spacing: 0.12em; font-weight: 600;
  }
  .header-labels span { text-align: center; }
  .header-labels span:first-child { text-align: center; }
  .set-wrap {
    position: relative; overflow: hidden; touch-action: pan-y;
    background: var(--surface);
  }
  .set-row {
    display: grid; grid-template-columns: 26px minmax(0,1fr) minmax(0,1fr) 44px 40px 48px; gap: 5px;
    padding: 4px 14px; align-items: center; position: relative; z-index: 1;
    background: var(--surface); transition: transform .16s cubic-bezier(.2,.7,.2,1);
    touch-action: pan-y; user-select: none; will-change: transform;
  }
  .set-wrap.show-delete .set-row { transform: translateX(58px); }
  .set-delete-btn {
    appearance: none; position: absolute; left: 14px; top: 4px; bottom: 4px;
    width: 46px; border: 0; border-radius: 10px;
    background: var(--bad); color: var(--fg); cursor: pointer;
    font-family: var(--sans); font-size: 22px; font-weight: 800;
    display: grid; place-items: center; opacity: 0; transform: scale(.88);
    pointer-events: none; transition: opacity .14s, transform .14s; z-index: 0;
  }
  .set-wrap.show-delete .set-delete-btn,
  .set-wrap.swiping-delete .set-delete-btn { opacity: 1; transform: scale(1); pointer-events: auto; }
  .set-row::before {
    content: ""; position: absolute; left: 0; top: 0; bottom: 0; width: 3px;
    background: transparent; transition: background .12s;
  }
  .set-row.done::before { background: var(--good); }
  .set-num {
    color: var(--fg-3); font-family: var(--num); font-size: 14px; font-weight: 600;
    text-align: center;
  }
  .set-input, .rir-input {
    background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg); padding: 13px 2px; border-radius: 10px;
    font-family: var(--num); font-size: 17px; font-weight: 600;
    text-align: center; width: 100%; -webkit-appearance: none;
    letter-spacing: -0.01em;
  }
  .set-input::placeholder, .rir-input::placeholder {
    color: var(--fg-4); font-weight: 500;
  }
  .set-input:focus, .rir-input:focus {
    outline: none; border-color: var(--ember);
    background: oklch(0.215 0.025 55);
  }
  .set-input.done { background: var(--good-soft); border-color: oklch(0.78 0.14 145 / 0.4); color: var(--fg); }
  .rir-input { font-size: 15px; padding: 13px 0; }
  .check-btn {
    appearance: none; background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg-3); border-radius: 10px; height: 46px; cursor: pointer;
    display: grid; place-items: center;
    transition: background .12s, border-color .12s, color .12s;
  }
  .check-btn svg { width: 18px; height: 18px; }
  .check-btn.done { background: var(--good); border-color: var(--good); color: var(--bg); }
  .drop-toggle {
    appearance: none; border: 1px solid var(--line-soft);
    background: var(--surface-2); color: var(--fg-3);
    border-radius: 10px; height: 46px; cursor: pointer;
    font-family: var(--num); font-size: 10px; font-weight: 800;
    letter-spacing: 0; transition: background .12s, border-color .12s, color .12s, transform .12s;
  }
  .drop-toggle.active {
    background: var(--ember-soft); border-color: var(--ember-line);
    color: var(--ember);
  }
  .drop-toggle:active { transform: scale(.97); }
  .drop-row {
    display: grid; grid-template-columns: 48px minmax(0,1fr) minmax(0,1fr); gap: 8px;
    margin: 2px 14px 8px 50px; padding: 8px;
    background: var(--bg-soft); border: 1px solid var(--line-soft);
    border-radius: 10px; align-items: center;
  }
  .drop-row-label {
    font-family: var(--num); font-size: 10px; font-weight: 800;
    color: var(--ember); text-align: center; letter-spacing: 0;
  }
  .drop-input {
    background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg); padding: 10px 2px; border-radius: 9px;
    font-family: var(--num); font-size: 15px; font-weight: 700;
    text-align: center; width: 100%; -webkit-appearance: none; letter-spacing: 0;
  }
  .drop-input:focus {
    outline: none; border-color: var(--ember);
    background: oklch(0.215 0.025 55);
  }
  .drop-input::placeholder { color: var(--fg-4); font-weight: 600; }

  .add-set {
    width: calc(100% - 28px); margin: 8px 14px 12px;
    padding: 11px; background: transparent;
    border: 1px dashed var(--line); color: var(--fg-3);
    border-radius: 10px; font-size: 13px; font-weight: 600; cursor: pointer;
    font-family: var(--sans);
  }
  .add-set:active { background: var(--surface-2); }
  .compare-row {
    padding: 9px 16px; font-family: var(--num); font-size: 11px;
    color: var(--fg-3); border-top: 1px solid var(--line-soft);
    background: var(--bg-soft); letter-spacing: 0.03em;
    display: flex; align-items: center; flex-wrap: wrap; gap: 4px;
  }
  .compare-row .up   { color: var(--good); font-weight: 700; }
  .compare-row .down { color: var(--bad);  font-weight: 700; }
  .compare-row .same { color: var(--fg-3); }

  /* ============ TIMER — floating pill ============ */
  .timer-bar {
    position: fixed;
    bottom: calc(var(--nav-h) + 12px + env(safe-area-inset-bottom));
    left: 50%; transform: translate(-50%, 30px); opacity: 0;
    background: var(--ember); color: oklch(0.18 0.03 50);
    padding: 12px 16px 12px 18px; border-radius: 999px;
    z-index: 80; transition: transform .25s cubic-bezier(.2,.7,.2,1), opacity .2s, background .2s;
    display: flex; align-items: center; gap: 12px; pointer-events: none;
    box-shadow: 0 12px 40px -8px oklch(0.755 0.165 55 / 0.5), 0 0 0 1px oklch(0.85 0.16 55 / 0.5);
    font-family: var(--num);
  }
  .timer-bar.active { transform: translate(-50%, 0); opacity: 1; pointer-events: auto; }
  .timer-bar.done-pulse {
    animation: timerPulse .75s ease-in-out 4;
    box-shadow: 0 0 0 1px oklch(0.78 0.14 145 / 0.7), 0 0 36px oklch(0.78 0.14 145 / 0.55);
  }
  body.timer-flash::before {
    content: ""; position: fixed; inset: 0; z-index: 70;
    background: oklch(0.78 0.14 145 / 0.12); pointer-events: none;
    animation: screenFlash .9s ease-out 2;
  }
  @keyframes timerPulse {
    0%, 100% { transform: translate(-50%, 0) scale(1); }
    50% { transform: translate(-50%, 0) scale(1.04); }
  }
  @keyframes screenFlash {
    0% { opacity: 0; }
    20% { opacity: 1; }
    100% { opacity: 0; }
  }
  .timer-bar #timer-display {
    font-size: 22px; font-weight: 700; letter-spacing: -0.02em;
    font-variant-numeric: tabular-nums;
  }
  .timer-bar button {
    background: oklch(0.20 0.03 50 / 0.55); border: 0; color: oklch(0.98 0.005 80);
    padding: 7px 14px; border-radius: 999px; font-size: 12px; font-weight: 700;
    cursor: pointer; font-family: var(--sans); letter-spacing: 0.02em;
  }

  /* ============ BUTTONS ============ */
  .btn-primary {
    width: 100%; padding: 16px; background: var(--ember); color: var(--bg);
    border: 0; border-radius: var(--r-md);
    font-family: var(--sans); font-size: 15px; font-weight: 700; letter-spacing: -0.01em;
    margin-top: 14px; cursor: pointer; transition: transform .08s, background .15s;
  }
  .btn-primary:active { transform: scale(0.99); background: var(--ember-2); }
  .btn-secondary {
    width: 100%; padding: 13px; background: var(--surface); color: var(--fg);
    border: 1px solid var(--line-soft); border-radius: var(--r-md);
    font-family: var(--sans); font-size: 14px; font-weight: 600;
    margin-top: 8px; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 8px;
  }
  .btn-secondary:active { background: var(--surface-2); }
  .file-input { display: none; }
  .support-note {
    margin-top: 10px; color: var(--fg-3); font-size: 12px; line-height: 1.45;
    padding: 10px 12px; background: var(--bg-soft);
    border: 1px solid var(--line-soft); border-radius: 10px;
  }
  .health-meta {
    margin-top: 8px; color: var(--fg-3);
    font-family: var(--num); font-size: 11px; line-height: 1.5;
  }
  .health-meta b { color: var(--fg); font-weight: 700; }

  /* ============ WORKOUT NOTE ============ */
  .workout-note-section {
    margin-top: 18px; padding: 14px;
    background: var(--surface); border: 1px solid var(--line-soft); border-radius: var(--r-md);
  }
  .workout-note-section label { display: block; margin-bottom: 10px;
    font-family: var(--num); font-size: 10px; font-weight: 600;
    letter-spacing: 0.10em; text-transform: uppercase; color: var(--fg-3); }
  .workout-note-section textarea {
    width: 100%; background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg); padding: 12px 14px; border-radius: 10px;
    font-family: var(--sans); font-size: 14px; line-height: 1.5;
    resize: vertical; min-height: 76px; -webkit-appearance: none;
  }
  .workout-note-section textarea:focus { outline: none; border-color: var(--ember); }
  .workout-note-section textarea::placeholder { color: var(--fg-4); }
  .history-edit-banner {
    display: none; margin-bottom: 14px; padding: 12px;
    background: var(--ember-soft); border: 1px solid var(--ember-line);
    border-radius: var(--r-md); color: var(--fg);
  }
  .history-edit-banner.active { display: grid; gap: 10px; }
  .history-edit-banner-title { font-size: 13px; font-weight: 800; color: var(--ember); }
  .history-edit-controls {
    display: grid; grid-template-columns: 1fr auto auto; gap: 8px; align-items: end;
  }
  .history-edit-controls label {
    display: grid; gap: 5px; font-family: var(--num); font-size: 10px;
    color: var(--fg-3); text-transform: uppercase; font-weight: 700;
  }
  .history-edit-controls input {
    background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg); padding: 10px; border-radius: 10px;
    font-family: var(--num); font-size: 14px;
  }
  .history-edit-controls button,
  .history-edit-btn {
    appearance: none; border: 1px solid var(--line-soft);
    background: var(--surface-2); color: var(--fg);
    border-radius: 10px; padding: 10px 12px;
    font-family: var(--sans); font-size: 12px; font-weight: 800;
    cursor: pointer;
  }
  .history-edit-delete {
    border-color: oklch(0.68 0.18 25 / 0.42) !important;
    background: var(--bad-soft) !important;
    color: var(--bad) !important;
  }
  @media (max-width: 380px) {
    .history-edit-controls { grid-template-columns: 1fr 1fr; }
    .history-edit-controls label { grid-column: 1 / -1; }
  }
  .exercise-note-section {
    margin-top: 12px; padding: 12px;
    background: oklch(0.165 0.007 55 / 0.72);
    border: 1px solid var(--line-soft); border-radius: var(--r-md);
  }
  .exercise-note-section label {
    display: block; margin-bottom: 8px;
    font-family: var(--num); font-size: 10px; font-weight: 600;
    letter-spacing: 0.10em; text-transform: uppercase; color: var(--fg-3);
  }
  .exercise-note-section textarea {
    width: 100%; background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg); padding: 10px 11px; border-radius: 10px;
    font-family: var(--sans); font-size: 14px; line-height: 1.4;
    resize: vertical; min-height: 58px; -webkit-appearance: none;
  }
  .exercise-note-section textarea:focus { outline: none; border-color: var(--ember); }
  .exercise-note-section textarea::placeholder { color: var(--fg-4); }

  /* ============ HISTORY ============ */
  .history-day {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 0; margin-bottom: 10px;
    overflow: hidden;
  }
  .history-day summary {
    list-style: none; cursor: pointer; padding: 14px 16px;
    display: grid; grid-template-columns: 1fr auto; gap: 12px; align-items: center;
  }
  .history-day summary::-webkit-details-marker { display: none; }
  .history-summary-title {
    font-size: 16px; font-weight: 700; color: var(--fg);
    letter-spacing: -0.01em; margin-bottom: 3px;
  }
  .history-summary-sub {
    font-family: var(--num); font-size: 11px; color: var(--fg-3);
    letter-spacing: 0.02em; line-height: 1.35;
  }
  .history-chevron {
    width: 28px; height: 28px; border-radius: 9px;
    background: var(--surface-2); color: var(--fg-3);
    display: grid; place-items: center; font-size: 18px; font-weight: 700;
    transition: transform .16s, color .16s, background .16s;
  }
  .history-summary-actions { display: flex; align-items: center; gap: 8px; }
  .history-day[open] .history-chevron {
    transform: rotate(90deg); color: var(--ember); background: var(--ember-soft);
  }
  .history-details {
    padding: 0 16px 14px; border-top: 1px solid var(--line-soft);
  }
  .history-actions {
    display: flex; gap: 8px; padding-top: 12px; margin-top: 10px;
    border-top: 1px solid var(--line-soft);
  }
  .history-date {
    font-family: var(--num); font-size: 11px; color: var(--ember);
    font-weight: 700; letter-spacing: 0.08em; text-transform: uppercase;
    margin-bottom: 5px;
  }
  .history-workout { font-size: 16px; font-weight: 600; letter-spacing: -0.01em; margin-bottom: 12px; }
  .history-exercise {
    font-size: 13px; padding: 8px 0; border-top: 1px solid var(--line-soft); color: var(--fg-2);
  }
  .history-details .history-exercise:first-child { border-top: 0; }
  .history-exercise-name { font-weight: 600; color: var(--fg); margin-bottom: 3px; letter-spacing: -0.005em; }
  .history-sets { color: var(--fg-3); font-family: var(--num); font-size: 12px; letter-spacing: 0.02em; }
  .history-note {
    font-size: 12px; color: var(--fg-2); margin-top: 10px; padding-top: 10px;
    border-top: 1px solid var(--line-soft); line-height: 1.5;
    display: flex; gap: 8px;
  }
  .history-note::before { content: "—"; color: var(--fg-4); }

  .empty-state {
    text-align: center; color: var(--fg-3); padding: 56px 24px; font-size: 14px; line-height: 1.6;
  }
  .empty-state::before {
    content: ""; display: block; width: 36px; height: 36px;
    border: 1px dashed var(--line); border-radius: 50%; margin: 0 auto 14px;
  }

  /* ============ CHARTS ============ */
  .chart-card {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 16px; margin-bottom: 12px;
  }
  .chart-title { font-size: 15px; font-weight: 600; letter-spacing: -0.01em; margin-bottom: 3px; }
  .chart-subtitle { font-family: var(--num); font-size: 11px; color: var(--fg-3);
                    margin-bottom: 14px; letter-spacing: 0.03em; }
  .chart-stats {
    display: flex; gap: 18px; margin-bottom: 12px; flex-wrap: wrap;
    font-family: var(--num); font-size: 12px; letter-spacing: 0.02em;
  }
  .chart-stat-label { color: var(--fg-3); }
  .chart-stat-value { color: var(--fg); font-weight: 700; margin-left: 4px; }
  svg.chart { width: 100%; height: 150px; display: block; }
  .health-range {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px;
    margin-bottom: 12px;
  }
  .health-range button {
    padding: 10px 8px; border-radius: 10px;
    background: var(--surface); border: 1px solid var(--line-soft);
    color: var(--fg-3); font-family: var(--sans); font-size: 13px;
    font-weight: 700; cursor: pointer;
  }
  .health-range button.active {
    background: var(--ember); border-color: var(--ember); color: var(--bg);
  }
  .health-workout-month .history-details { padding-bottom: 8px; }
  .health-workout-item {
    border-top: 1px solid var(--line-soft);
  }
  .health-workout-item:first-child { border-top: 0; }
  .health-workout-item summary {
    list-style: none; cursor: pointer; padding: 11px 0;
    display: grid; grid-template-columns: 1fr auto; gap: 10px; align-items: center;
  }
  .health-workout-item summary::-webkit-details-marker { display: none; }
  .health-workout-chevron {
    width: 24px; height: 24px; border-radius: 8px;
    background: var(--surface-2); color: var(--fg-3);
    display: grid; place-items: center; font-size: 16px; font-weight: 700;
    transition: transform .16s, color .16s, background .16s;
  }
  .health-workout-item[open] .health-workout-chevron {
    transform: rotate(90deg); color: var(--ember); background: var(--ember-soft);
  }
  .health-workout-detail { padding: 0 0 12px; }
  .food-items { display: grid; gap: 8px; padding-top: 10px; }
  .food-item {
    display: grid; grid-template-columns: 1fr auto; gap: 6px 10px; align-items: baseline;
    padding: 10px 12px; background: var(--bg-soft);
    border: 1px solid var(--line-soft); border-radius: 10px;
  }
  .food-item-name { font-size: 13px; font-weight: 650; color: var(--fg); }
  .food-item-kcal { font-family: var(--num); font-size: 13px; font-weight: 800; color: var(--fg); }
  .food-item-macros, .food-item-micros {
    grid-column: 1 / -1; font-family: var(--num); font-size: 10px;
    color: var(--fg-3); letter-spacing: 0.02em;
  }
  .food-item-micros { color: var(--fg-4); }
  .macro-bar {
    display: flex; overflow: hidden; height: 10px; border-radius: 999px;
    background: var(--surface-2); border: 1px solid var(--line-soft); margin: 12px 0;
  }
  .macro-bar span { display: block; min-width: 2px; }
  .macro-protein { background: #5fcf6f; }
  .macro-carbs { background: #4a9eff; }
  .macro-fat { background: #ff9f43; }
  .progress-day-summary {
    margin: -4px 0 14px; color: var(--fg-3);
    font-family: var(--num); font-size: 11px; letter-spacing: 0.03em;
  }
  .progress-exercise-card .chart { margin-bottom: 12px; }
  .progress-exercise-card .chart:last-child { margin-bottom: 0; }
  .progress-mini-title {
    display: flex; align-items: center; justify-content: space-between;
    margin: 10px 0 6px; font-family: var(--num);
    font-size: 10px; font-weight: 700; letter-spacing: 0.10em;
    text-transform: uppercase; color: var(--fg-3);
  }
  .progress-mini-title span:last-child {
    color: var(--fg-4); font-weight: 600; text-transform: none; letter-spacing: 0.02em;
  }
  .exercise-picker {
    background: var(--surface); border: 1px solid var(--line-soft);
    color: var(--fg); width: 100%; padding: 14px 16px; border-radius: var(--r-md);
    font-family: var(--sans); font-size: 14px; font-weight: 500; margin-bottom: 16px;
    -webkit-appearance: none; appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8' fill='none' stroke='%23999' stroke-width='1.8' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M1 1.5L6 6.5L11 1.5'/%3E%3C/svg%3E");
    background-repeat: no-repeat; background-position: right 16px center;
    padding-right: 40px;
  }
  .exercise-picker:focus { outline: none; border-color: var(--ember); }

  .forecast-pill {
    display: inline-block; background: var(--info-soft); color: var(--info);
    font-family: var(--num); font-size: 11px; padding: 3px 8px; border-radius: 6px;
    font-weight: 600; margin-left: 8px; letter-spacing: 0.04em;
  }

  /* ============ MEASURE ============ */
  .measure-form {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 16px; margin-bottom: 14px;
  }
  .measure-form h3 {
    font-family: var(--num); font-size: 10px; font-weight: 600;
    letter-spacing: 0.10em; text-transform: uppercase; color: var(--fg-3);
    margin-bottom: 14px;
  }
  .measure-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 12px; }
  .measure-field label {
    display: block; font-family: var(--num); font-size: 10px;
    color: var(--fg-3); margin-bottom: 6px; text-transform: uppercase; letter-spacing: 0.10em; font-weight: 600;
  }
  .measure-field input {
    background: var(--surface-2); border: 1px solid var(--line-soft); color: var(--fg);
    width: 100%; padding: 12px 14px; border-radius: 10px;
    font-family: var(--num); font-size: 16px; font-weight: 600;
    -webkit-appearance: none;
  }
  .measure-field input:focus { outline: none; border-color: var(--ember); }
  .ideal-goals { display: grid; gap: 8px; margin-top: 12px; }
  .goal-profile {
    display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 12px;
  }
  .goal-profile button {
    padding: 11px 8px; border-radius: 10px;
    background: var(--surface-2); border: 1px solid var(--line-soft);
    color: var(--fg-3); font-family: var(--sans); font-size: 13px;
    font-weight: 700; cursor: pointer;
  }
  .goal-profile button.active {
    background: var(--ember); border-color: var(--ember); color: var(--bg);
  }
  .goal-formula-note {
    color: var(--fg-3); font-size: 12px; line-height: 1.45;
    background: var(--bg-soft); border: 1px solid var(--line-soft);
    border-radius: 10px; padding: 10px 12px; margin: 10px 0 12px;
  }
  .ideal-row {
    display: grid; grid-template-columns: 1fr auto; gap: 10px; align-items: center;
    padding: 10px 12px; background: var(--bg-soft);
    border: 1px solid var(--line-soft); border-radius: 10px;
  }
  .ideal-row span:first-child {
    color: var(--fg-3); font-family: var(--num); font-size: 11px;
    letter-spacing: 0.06em; text-transform: uppercase;
  }
  .ideal-row b { font-family: var(--num); font-size: 14px; color: var(--fg); }
  .ideal-empty {
    color: var(--fg-3); font-size: 13px; line-height: 1.5;
    background: var(--bg-soft); border: 1px solid var(--line-soft);
    border-radius: 10px; padding: 12px;
  }

  /* ============ MODAL ============ */
  .modal-bg {
    position: fixed; inset: 0; background: oklch(0.08 0.005 50 / 0.72);
    backdrop-filter: blur(6px); -webkit-backdrop-filter: blur(6px);
    display: none; align-items: flex-end; z-index: 200;
  }
  .modal-bg.active { display: flex; }
  .modal {
    background: var(--bg-soft); border-top: 1px solid var(--line);
    width: 100%; max-width: 480px; margin: 0 auto;
    border-radius: var(--r-xl) var(--r-xl) 0 0;
    padding: 22px 20px calc(20px + env(safe-area-inset-bottom));
    max-height: 88vh; overflow-y: auto;
  }
  .modal::before {
    content: ""; display: block; width: 38px; height: 4px; border-radius: 2px;
    background: var(--line); margin: -8px auto 18px;
  }
  .modal h3 { font-size: 17px; font-weight: 600; letter-spacing: -0.01em; margin-bottom: 14px; }
  .modal-option {
    background: var(--surface); border: 1px solid var(--line-soft);
    color: var(--fg); width: 100%; padding: 14px 16px; border-radius: 10px;
    margin-bottom: 8px; font-size: 14px; font-weight: 500; text-align: left; cursor: pointer;
    font-family: var(--sans);
  }
  .modal-option:active { background: var(--surface-2); }
  .modal-close {
    background: transparent; color: var(--fg-3); border: 0;
    width: 100%; padding: 14px; font-size: 14px; font-weight: 500; margin-top: 8px;
    cursor: pointer; font-family: var(--sans);
  }

  /* ============ EDITOR ============ */
  .editor-day-tab { display: flex; gap: 6px; margin-bottom: 14px; }
  .editor-day-tab button {
    flex: 1; padding: 10px; background: var(--surface); color: var(--fg-3);
    border: 1px solid var(--line-soft); border-radius: 10px;
    font-family: var(--sans); font-size: 13px; font-weight: 600; cursor: pointer;
  }
  .editor-day-tab button.active { background: var(--ember); color: var(--bg); border-color: var(--ember); }
  .program-editor { display: grid; gap: 12px; }
  .program-editor-top {
    position: sticky; top: -22px; z-index: 3;
    background: var(--bg-soft); padding-top: 4px; padding-bottom: 10px;
  }
  .editor-field { display: grid; gap: 6px; }
  .editor-field label {
    font-family: var(--num); font-size: 10px; font-weight: 600;
    letter-spacing: 0.10em; text-transform: uppercase; color: var(--fg-3);
  }
  .editor-input {
    width: 100%; min-width: 0; background: var(--surface-2);
    border: 1px solid var(--line-soft); color: var(--fg);
    padding: 11px 12px; border-radius: 10px; font-size: 14px;
    -webkit-appearance: none; font-family: var(--sans);
  }
  .editor-input:focus { outline: none; border-color: var(--ember); }
  .editor-input.num { text-align: center; font-family: var(--num); font-weight: 700; }
  .editor-hint {
    color: var(--fg-3); font-size: 12px; line-height: 1.45;
    background: var(--bg-soft); border: 1px solid var(--line-soft);
    border-radius: 10px; padding: 10px 12px;
  }
  .editor-section-title {
    display: flex; justify-content: space-between; align-items: baseline;
    margin: 8px 0 2px;
  }
  .editor-section-title span:first-child {
    font-family: var(--num); font-size: 10px; font-weight: 700;
    letter-spacing: 0.12em; text-transform: uppercase; color: var(--fg-3);
  }
  .editor-section-title span:last-child { color: var(--fg-4); font-size: 12px; }
  .editor-ex {
    background: var(--surface); border: 1px solid var(--line-soft);
    border-radius: var(--r-md); padding: 12px; margin-bottom: 10px;
  }
  .editor-ex-head {
    display: flex; justify-content: space-between; align-items: center;
    gap: 10px; margin-bottom: 10px;
  }
  .editor-ex-num {
    font-family: var(--num); font-size: 11px; font-weight: 700;
    color: var(--ember); letter-spacing: 0.08em; text-transform: uppercase;
  }
  .editor-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .editor-ex-row { display: flex; gap: 6px; align-items: center; margin-bottom: 6px; }
  .editor-ex-row input {
    background: var(--surface-2); border: 1px solid var(--line-soft); color: var(--fg);
    padding: 9px 10px; border-radius: 8px; font-size: 13px; flex: 1;
    -webkit-appearance: none; font-family: var(--sans);
  }
  .editor-ex-row input.small { flex: 0 0 56px; text-align: center; font-family: var(--num); font-weight: 600; }
  .editor-ex-row input.target { flex: 2; }
  .editor-ex-row > span { font-family: var(--num); font-size: 10px;
                          color: var(--fg-3); letter-spacing: 0.06em; text-transform: uppercase; }
  .editor-ex-actions { display: flex; gap: 4px; margin-top: 6px; }
  .editor-ex-actions button {
    flex: 1; padding: 7px; background: var(--surface-2); color: var(--fg-2);
    border: 1px solid var(--line-soft); border-radius: 7px;
    font-size: 12px; cursor: pointer; font-family: var(--sans);
  }
  .editor-ex-head .editor-ex-actions { margin-top: 0; flex: 0 0 auto; }
  .editor-ex-head .editor-ex-actions button { width: 38px; flex: 0 0 38px; }
  .editor-ex-actions button.del { color: var(--bad); }
  .editor-swap {
    background: var(--surface-2); border: 1px solid var(--line-soft); color: var(--fg);
    padding: 9px 10px; border-radius: 8px; font-size: 12px; width: 100%; margin-top: 6px;
    -webkit-appearance: none; font-family: var(--sans);
  }

  /* ============ INFO + TOGGLES ============ */
  .info-box {
    background: var(--surface); padding: 14px 16px; border-radius: var(--r-md);
    font-size: 13px; color: var(--fg-2); line-height: 1.55; margin-bottom: 12px;
    border: 1px solid var(--line-soft); position: relative; padding-left: 18px;
  }
  .info-box::before {
    content: ""; position: absolute; left: 0; top: 10%; bottom: 10%;
    width: 2px; background: var(--ember); border-radius: 1px;
  }
  .info-box b { color: var(--fg); font-weight: 600; }

  .toggle-row {
    display: flex; justify-content: space-between; align-items: center;
    padding: 14px 16px; background: var(--surface);
    border: 1px solid var(--line-soft); border-radius: var(--r-md);
    margin-bottom: 8px;
  }
  .toggle-row span { font-size: 14px; }
  .toggle {
    position: relative; width: 46px; height: 28px;
    background: var(--surface-2); border: 1px solid var(--line);
    border-radius: 14px; cursor: pointer; transition: background .2s, border-color .2s;
  }
  .toggle.on { background: var(--ember); border-color: var(--ember); }
  .toggle::after {
    content: ""; position: absolute; top: 2px; left: 2px; width: 22px; height: 22px;
    background: var(--fg); border-radius: 50%; transition: transform .2s;
  }
  .toggle.on::after { transform: translateX(18px); background: var(--bg); }

  input[type=number]::-webkit-inner-spin-button, input[type=number]::-webkit-outer-spin-button { -webkit-appearance: none; margin: 0; }
  input[type=number] { -moz-appearance: textfield; }
  input[type=date] {
    background: var(--surface-2); border: 1px solid var(--line-soft); color: var(--fg);
    width: 100%; padding: 12px 14px; border-radius: 10px;
    font-family: var(--num); font-size: 15px; -webkit-appearance: none;
  }
  input[type=date]:focus { outline: none; border-color: var(--ember); }
  ::selection { background: var(--ember-soft); color: var(--fg); }

  /* Phone-only: lock nav width on wide screens too */
  .nav { max-width: 480px; left: 50%; transform: translateX(-50%); right: auto; width: 100%; }
</style>
</head>
<body>

<nav class="nav">
  <button class="nav-btn active" data-screen="dashboard" aria-label="Главная">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><path d="M3 11l9-7 9 7v9a2 2 0 0 1-2 2h-4v-7h-6v7H5a2 2 0 0 1-2-2z"/></svg>
    <span>Главная</span>
  </button>
  <button class="nav-btn" data-screen="workout" aria-label="Тренировка">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><path d="M6.5 6.5l11 11M4 9l-2 2 4 4-2 2 3 3 2-2 4 4 2-2M15 9l2-2 3 3-2 2M9 15l-2 2 3 3 2-2"/></svg>
    <span>Трен</span>
  </button>
  <button class="nav-btn" data-screen="settings" aria-label="Настройки">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.7 1.7 0 0 0 .3 1.8l.1.1a2 2 0 1 1-2.8 2.8l-.1-.1a1.7 1.7 0 0 0-1.8-.3 1.7 1.7 0 0 0-1 1.5V21a2 2 0 1 1-4 0v-.1a1.7 1.7 0 0 0-1.1-1.5 1.7 1.7 0 0 0-1.8.3l-.1.1a2 2 0 1 1-2.8-2.8l.1-.1a1.7 1.7 0 0 0 .3-1.8 1.7 1.7 0 0 0-1.5-1H3a2 2 0 1 1 0-4h.1a1.7 1.7 0 0 0 1.5-1.1 1.7 1.7 0 0 0-.3-1.8l-.1-.1a2 2 0 1 1 2.8-2.8l.1.1a1.7 1.7 0 0 0 1.8.3H9a1.7 1.7 0 0 0 1-1.5V3a2 2 0 1 1 4 0v.1a1.7 1.7 0 0 0 1 1.5 1.7 1.7 0 0 0 1.8-.3l.1-.1a2 2 0 1 1 2.8 2.8l-.1.1a1.7 1.7 0 0 0-.3 1.8V9a1.7 1.7 0 0 0 1.5 1H21a2 2 0 1 1 0 4h-.1a1.7 1.7 0 0 0-1.5 1z"/></svg>
    <span>Опции</span>
  </button>
</nav>

<!-- DASHBOARD -->
<div class="screen active" id="screen-dashboard">
  <div class="eyebrow" id="dash-date"></div>
  <div id="dash-content"></div>
</div>

<!-- WORKOUT -->
<div class="screen" id="screen-workout">
  <h1 id="workout-title">Выбери день</h1>
  <div class="subtitle" id="workout-date"></div>
  <div class="week-bar">
    <div class="week-bar-left">
      <div class="label">Текущий цикл</div>
      <div class="week-bar-big" id="week-display"><em>Неделя 1</em></div>
    </div>
    <div class="week-bar-right">
      <button class="week-step" onclick="stepWeek(-1)" aria-label="Минус">−</button>
      <input type="number" class="week-num-input" id="week-input" min="1" max="20" value="1" onchange="setWeek(this.value)">
      <button class="week-step" onclick="stepWeek(1)" aria-label="Плюс">+</button>
    </div>
  </div>
  <div id="deload-banner"></div>
  <div id="draft-banner"></div>
  <div class="history-edit-banner" id="history-edit-banner"></div>
  <div class="day-selector" id="day-selector"></div>
  <div id="exercises-list"></div>
  <div id="workout-note-container" style="display:none">
    <div class="workout-note-section">
      <label>Заметка к тренировке (необязательно)</label>
      <textarea id="workout-note" placeholder="Как себя чувствовал? Что было сложно/легко? Что заметил?" oninput="updateWorkoutNote(this.value)"></textarea>
    </div>
  </div>
  <button class="btn-primary" id="finish-btn" style="display:none">Завершить тренировку</button>
</div>

<!-- PROGRESS -->
<div class="screen" id="screen-progress">
  <h1>Графики</h1>
  <div class="subtitle">Динамика по тренировочным дням</div>
  <select class="exercise-picker" id="progress-day-picker" onchange="updateProgressDay(this.value)"></select>
  <div id="progress-content"></div>
</div>

<!-- MEASURE -->
<div class="screen" id="screen-measure">
  <h1>Замеры</h1>
  <div class="subtitle">Раз в неделю, утром, натощак</div>
  <div class="measure-form">
    <h3 style="font-size: 14px; margin-bottom: 12px;">Новый замер</h3>
    <div class="measure-grid">
      <div class="measure-field"><label>Вес, кг</label><input type="number" id="m-weight" inputmode="decimal"></div>
      <div class="measure-field"><label>Рост, см</label><input type="number" id="m-height" inputmode="decimal"></div>
      <div class="measure-field"><label>Запястье, см</label><input type="number" id="m-wrist" inputmode="decimal"></div>
      <div class="measure-field"><label>Шея, см</label><input type="number" id="m-neck" inputmode="decimal"></div>
      <div class="measure-field"><label>Плечи, см</label><input type="number" id="m-shoulders" inputmode="decimal"></div>
      <div class="measure-field"><label>Грудь, см</label><input type="number" id="m-chest" inputmode="decimal"></div>
      <div class="measure-field"><label>Талия, см</label><input type="number" id="m-waist" inputmode="decimal"></div>
      <div class="measure-field"><label>Таз/ягодицы, см</label><input type="number" id="m-hips" inputmode="decimal"></div>
      <div class="measure-field"><label>Бицепс, см</label><input type="number" id="m-biceps" inputmode="decimal"></div>
      <div class="measure-field"><label>Предплечье, см</label><input type="number" id="m-forearm" inputmode="decimal"></div>
      <div class="measure-field"><label>Бедро, см</label><input type="number" id="m-thigh" inputmode="decimal"></div>
      <div class="measure-field"><label>Икра, см</label><input type="number" id="m-calf" inputmode="decimal"></div>
    </div>
    <button class="btn-primary" onclick="saveMeasure()">Сохранить замер</button>
  </div>
  <div class="measure-form">
    <h3 style="font-size: 14px; margin-bottom: 12px;">Цели на конец программы</h3>
    <div class="goal-profile" id="goal-profile">
      <button type="button" data-profile="male" onclick="setGoalProfile('male')">Мужской расчет</button>
      <button type="button" data-profile="female" onclick="setGoalProfile('female')">Женский расчет</button>
    </div>
    <div class="goal-formula-note" id="goal-formula-note"></div>
    <div class="measure-grid">
      <div class="measure-field"><label>Цель: вес, кг</label><input type="number" id="g-weight" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: шея, см</label><input type="number" id="g-neck" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: плечи, см</label><input type="number" id="g-shoulders" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: грудь, см</label><input type="number" id="g-chest" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: талия, см</label><input type="number" id="g-waist" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: таз, см</label><input type="number" id="g-hips" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: бицепс, см</label><input type="number" id="g-biceps" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: предплечье, см</label><input type="number" id="g-forearm" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: бедро, см</label><input type="number" id="g-thigh" inputmode="decimal" onchange="saveGoal()"></div>
      <div class="measure-field"><label>Цель: икра, см</label><input type="number" id="g-calf" inputmode="decimal" onchange="saveGoal()"></div>
    </div>
    <div id="ideal-goals" class="ideal-goals"></div>
    <button class="btn-secondary" onclick="applyIdealGoals()">Заполнить пустые цели формулой</button>
  </div>
  <h2>Динамика</h2>
  <div id="measure-charts"></div>
</div>

<!-- HEALTH -->
<div class="screen" id="screen-health">
  <h1>Часы</h1>
  <div class="subtitle">Apple Watch / Apple Health</div>
  <div class="measure-form">
    <h3 style="font-size: 14px; margin-bottom: 12px;">Импорт</h3>
    <input class="file-input" type="file" id="health-import-file" accept=".zip,.xml,application/zip,application/xml,text/xml" onchange="importAppleHealthFile(this.files[0]); this.value='';">
    <button class="btn-secondary" onclick="document.getElementById('health-import-file').click()">⌚ Импорт Apple Health ZIP/XML</button>
  </div>
  <div id="health-overview"></div>
  <h2>Сон</h2>
  <div id="health-sleep"></div>
  <h2>Состав тела</h2>
  <div id="health-body"></div>
  <h2>Графики</h2>
  <div id="health-charts"></div>
  <h2>Тренировки Apple Watch</h2>
  <div id="health-workouts"></div>
</div>

<!-- FOOD -->
<div class="screen" id="screen-food">
  <h1>Еда</h1>
  <div class="subtitle">Yazio / питание из Apple Health</div>
  <input class="file-input" type="file" id="food-import-file" accept=".zip,.xml,application/zip,application/xml,text/xml" onchange="importAppleHealthFile(this.files[0]); this.value='';">
  <button class="btn-secondary" onclick="document.getElementById('food-import-file').click()">Импорт Apple Health / Yazio ZIP</button>
  <div id="food-overview"></div>
  <h2>Дни</h2>
  <div id="food-days"></div>
</div>

<!-- HISTORY -->
<div class="screen" id="screen-history">
  <h1>История</h1>
  <div class="subtitle">Последние тренировки</div>
  <div id="history-list"></div>
</div>

<!-- SETTINGS -->
<div class="screen" id="screen-settings">
  <h1>Настройки</h1>
  
  <h2>Дата старта</h2>
  <div class="measure-form">
    <div class="measure-field"><label>Дата начала программы</label><input type="date" id="start-date" onchange="setStartDate(this.value)" style="background:#1f1f1f;border:1px solid #2a2a2a;color:#fff;width:100%;padding:12px;border-radius:8px;font-size:16px;-webkit-appearance:none;"></div>
  </div>
  
  <h2>Поведение</h2>
  <div class="toggle-row">
    <span>Автозапуск таймера отдыха</span>
    <div class="toggle" id="toggle-timer" onclick="toggleSetting('timer')"></div>
  </div>
  <div class="toggle-row">
    <span>Скрывать таймер по нулю</span>
    <div class="toggle on" id="toggle-autoclose" onclick="toggleSetting('autoclose')"></div>
  </div>

  <h2>Программа</h2>
  <button class="btn-secondary" onclick="openProgramEditor()">✏️ Редактировать программу</button>
  <button class="btn-secondary" onclick="newProgramVersion()">🆕 Новая версия программы</button>
  
  <h2>Резервная копия</h2>
  <button class="btn-secondary" onclick="downloadData()">⬇️ Скачать JSON-бэкап</button>
  <input class="file-input" type="file" id="import-data-file" accept=".json,application/json" onchange="importDataFile(this.files[0]); this.value='';">
  <button class="btn-secondary" onclick="document.getElementById('import-data-file').click()">⬆️ Восстановить JSON-бэкап</button>
  <button class="btn-secondary" onclick="downloadAIExport()">🧠 Скачать данные для нейронки</button>

  <h2 style="color: #c33;">Опасная зона</h2>
  <button class="btn-secondary" style="border-color:#5a1a1a;color:#c33;" onclick="resetAll()">🗑 Удалить все данные</button>
</div>

<!-- TIMER -->
<div class="timer-bar" id="timer-bar">
  <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="13" r="8"/><path d="M12 9v4l2 2M9 2h6M5 5l1.5 1.5"/></svg>
  <span id="timer-display">02:00</span>
  <button onclick="stopTimer()">Стоп</button>
</div>

<!-- MODAL -->
<div class="modal-bg" id="modal">
  <div class="modal">
    <h3 id="modal-title"></h3>
    <div id="modal-body"></div>
    <button class="modal-close" onclick="closeModal()">Закрыть</button>
  </div>
</div>

<script>
// ===== DEFAULT PROGRAM =====
const DEFAULT_PROGRAM = {
  version: 1,
  days: {
    upperA: {
      name: "Upper A — Грудь / Плечи / Трицепс",
      exercises: [
        { name: "Жим штанги наклонный 30°", target: "3×8-10, RIR 2", sets: 3, reps_min: 8, reps_max: 10, rest: 150, increment: 2.5, swaps: ["Жим гантелей наклонный 30°", "Жим в Смите наклонный"] },
        { name: "Жим плечами в тренажёре", target: "4×10-12, RIR 1-2", sets: 4, reps_min: 10, reps_max: 12, rest: 120, increment: 2.5, swaps: ["Жим гантелей сидя", "Жим в Смите сидя"] },
        { name: "Разводки гантелей lean-away", target: "4×12-15, RIR 1", sets: 4, reps_min: 12, reps_max: 15, rest: 75, increment: 1, swaps: ["Разводки в кроссовере", "Разводки гантелей стоя"] },
        { name: "Сведения в бабочке (Pec Deck)", target: "3×12-15, посл. RIR 0-1", sets: 3, reps_min: 12, reps_max: 15, rest: 90, increment: 2.5, swaps: ["Кроссовер на грудь", "Разводки гантелей лёжа"] },
        { name: "Трицепс в блоке с канатом", target: "3×12-15, RIR 1", sets: 3, reps_min: 12, reps_max: 15, rest: 60, increment: 2.5, swaps: ["Разгибания одной рукой обр. хват", "Отжимания на трицепс в гравитроне"] },
        { name: "Подъём гантелей перед собой", target: "2×12-15, RIR 1", sets: 2, reps_min: 12, reps_max: 15, rest: 60, increment: 1, swaps: ["Подъём с блином", "Подъём в нижнем блоке"] }
      ]
    },
    upperB: {
      name: "Upper B — Спина / Задняя дельта / Бицепс",
      exercises: [
        { name: "Подтягивания широким хватом", target: "4×6-10, RIR 1-2", sets: 4, reps_min: 6, reps_max: 10, rest: 150, increment: 2.5, swaps: ["Тяга верхнего блока широким", "Подтягивания в гравитроне"] },
        { name: "Тяга горизонтального блока", target: "4×10-12, RIR 2", sets: 4, reps_min: 10, reps_max: 12, rest: 120, increment: 2.5, swaps: ["Тяга гантели в наклоне с упором", "Тяга Т-грифа с упором"] },
        { name: "Тяга верхнего блока обр. хватом", target: "3×10-12, RIR 1", sets: 3, reps_min: 10, reps_max: 12, rest: 90, increment: 2.5, swaps: ["Тяга верхнего блока узким", "Подтягивания обратным хватом"] },
        { name: "Face pull / задние дельты", target: "4×12-15, RIR 1", sets: 4, reps_min: 12, reps_max: 15, rest: 75, increment: 2.5, swaps: ["Обратные разводки в кроссовере", "Обратные разводки в тренажёре"] },
        { name: "Шраги с гантелями", target: "3×12-15, RIR 1", sets: 3, reps_min: 12, reps_max: 15, rest: 60, increment: 2.5, swaps: ["Шраги в Смите", "Шраги в кроссовере"] },
        { name: "Бицепс в скамье Скотта", target: "3×8-12, RIR 1", sets: 3, reps_min: 8, reps_max: 12, rest: 90, increment: 1, swaps: ["Сгибания EZ-штангой стоя", "Сгибания в блоке стоя"] },
        { name: "Молотки с гантелями", target: "2×10-12, RIR 1", sets: 2, reps_min: 10, reps_max: 12, rest: 60, increment: 1, swaps: ["Молотки в кроссовере", "Сгибания обратным хватом"] }
      ]
    },
    lower: {
      name: "Lower — Ноги / Кор",
      exercises: [
        { name: "Жим ногами", target: "4×10-12, RIR 2", sets: 4, reps_min: 10, reps_max: 12, rest: 150, increment: 5, swaps: ["Жим ногами в Смите", "Гак-машина"] },
        { name: "Сгибания ног лёжа", target: "4×10-12, RIR 1", sets: 4, reps_min: 10, reps_max: 12, rest: 90, increment: 2.5, swaps: ["Сгибания ног сидя", "Сгибания стоя одной ногой"] },
        { name: "Разгибания ног сидя", target: "3×12-15, RIR 1", sets: 3, reps_min: 12, reps_max: 15, rest: 90, increment: 2.5, swaps: ["Разгибания одной ногой", "Сисси-присед"] },
        { name: "Hip Thrust (ягодичный мост)", target: "3×10-12, RIR 2", sets: 3, reps_min: 10, reps_max: 12, rest: 120, increment: 5, swaps: ["Hip Thrust в Смите", "Ягодичный мост на полу"] },
        { name: "Подъёмы на носки", target: "3×12-15, RIR 1", sets: 3, reps_min: 12, reps_max: 15, rest: 60, increment: 2.5, swaps: ["Подъёмы на носки сидя", "Подъёмы в жиме ногами"] },
        { name: "Планка / скручивания", target: "3×30-45 сек или 12-15", sets: 3, reps_min: 12, reps_max: 15, rest: 60, increment: 0, swaps: ["Скручивания на блоке", "Подъём ног в висе"] }
      ]
    }
  }
};
const ROTATION = { odd: ["upperA", "lower", "upperB"], even: ["lower", "upperA", "upperB"] };
const HEALTH_IMPORT_START_DATE = '2026-05-16';
const OPTIONAL_SECTIONS = [
  { key: 'progress', label: 'Графики' },
  { key: 'measure', label: 'Замеры' },
  { key: 'health', label: 'Часы' },
  { key: 'food', label: 'Еда' },
  { key: 'history', label: 'История' }
];
const ALWAYS_VISIBLE_SECTIONS = new Set(['dashboard', 'workout', 'settings']);
const DASH_LINK_ICONS = {
  progress: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><path d="M3 17l5-5 4 4 8-9"/><path d="M14 7h7v7"/></svg>',
  measure: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><path d="M3 8h18v8H3z"/><path d="M7 8v3M11 8v4M15 8v3M19 8v4"/></svg>',
  health: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><rect x="7" y="5" width="10" height="14" rx="4"/><path d="M9 5V3h6v2M9 19v2h6v-2M10 12h4"/></svg>',
  food: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3v8M10 3v8M8 3v18"/><path d="M4 11h8"/><path d="M17 3v18"/><path d="M17 3c2 2.4 3 4.7 3 7 0 2-1.2 3.4-3 3.4"/></svg>',
  history: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 2"/></svg>'
};

// ===== STATE =====
let currentDay = null;
let currentWorkout = null;
let timerInterval = null;
let timerSeconds = 0;
let timerEndAt = null;
let timerDurationSeconds = 0;
let timerFinished = false;
let timerAutocloseTimeout = null;
let activeSwapExIdx = null;
let editorDay = "upperA";
let editingHistoryIndex = null;
let progressDay = null;
let dashboardCalendarAnchor = new Date();
let setSwipeState = null;
const TIMER_STATE_KEY = 'active_timer_state';

function escapeHTML(value) {
  return String(value == null ? '' : value).replace(/[&<>"']/g, ch => ({
    '&': '&amp;',
    '<': '&lt;',
    '>': '&gt;',
    '"': '&quot;',
    "'": '&#39;'
  })[ch]);
}

const MEASURE_FIELDS = [
  { key: 'weight', label: 'Вес', unit: 'кг', color: '#ff6b00' },
  { key: 'height', label: 'Рост', unit: 'см', color: '#8f8f8f' },
  { key: 'wrist', label: 'Запястье', unit: 'см', color: '#a68bff' },
  { key: 'neck', label: 'Шея', unit: 'см', color: '#4a9eff' },
  { key: 'shoulders', label: 'Плечи', unit: 'см', color: '#ff9f43' },
  { key: 'chest', label: 'Грудь', unit: 'см', color: '#5fcf6f' },
  { key: 'waist', label: 'Талия', unit: 'см', color: '#4a9eff' },
  { key: 'hips', label: 'Таз', unit: 'см', color: '#ff7eb6' },
  { key: 'biceps', label: 'Бицепс', unit: 'см', color: '#5fcf6f' },
  { key: 'forearm', label: 'Предплечье', unit: 'см', color: '#9bdc65' },
  { key: 'thigh', label: 'Бедро', unit: 'см', color: '#c878ff' },
  { key: 'calf', label: 'Икра', unit: 'см', color: '#ffc857' }
];
const GOAL_FIELDS = MEASURE_FIELDS.filter(f => !['height', 'wrist'].includes(f.key));

function numberFromInput(id) {
  const el = document.getElementById(id);
  if (!el) return null;
  const raw = String(el.value || '').replace(',', '.');
  const value = parseFloat(raw);
  return Number.isFinite(value) ? value : null;
}
function round1(value) {
  return Math.round(value * 10) / 10;
}
function formatKg(value) {
  const rounded = value >= 100 ? Math.round(value) : round1(value);
  return rounded.toLocaleString('ru-RU');
}

// ===== STORAGE =====
function readJSON(key, fallback) {
  try {
    const raw = localStorage.getItem(key);
    return raw ? JSON.parse(raw) : fallback;
  } catch (e) {
    return fallback;
  }
}
function getHistory() { return readJSON('workout_history', []); }
function saveHistory(h) { localStorage.setItem('workout_history', JSON.stringify(h)); }
function getMeasures() { return readJSON('measures', []); }
function saveMeasures(m) { localStorage.setItem('measures', JSON.stringify(m)); }
function isHealthDateAllowed(dateKey) {
  return String(dateKey || '').slice(0, 10) >= HEALTH_IMPORT_START_DATE;
}
function filterHealthRows(rows) {
  return (Array.isArray(rows) ? rows : [])
    .filter(row => row && isHealthDateAllowed(row.date))
    .sort((a, b) => String(a.date).localeCompare(String(b.date)));
}
function getHealthDaily() { return filterHealthRows(readJSON('apple_health_daily', [])); }
function saveHealthDaily(rows) { localStorage.setItem('apple_health_daily', JSON.stringify(filterHealthRows(rows))); }
function getFoodDaily() { return filterHealthRows(readJSON('yazio_food_daily', [])); }
function saveFoodDaily(rows) { localStorage.setItem('yazio_food_daily', JSON.stringify(filterHealthRows(rows))); }
function getHealthImportMeta() { return readJSON('apple_health_import', null); }
function saveHealthImportMeta(meta) { localStorage.setItem('apple_health_import', JSON.stringify(meta)); }
function getGoals() { return readJSON('goals', {}); }
function saveGoals(g) { localStorage.setItem('goals', JSON.stringify(g)); }
function getProgram() {
  const stored = readJSON('program', null);
  if (!stored) { localStorage.setItem('program', JSON.stringify(DEFAULT_PROGRAM)); return DEFAULT_PROGRAM; }
  return stored;
}
function saveProgram(p) { localStorage.setItem('program', JSON.stringify(p)); }
function getStartDate() {
  let d = localStorage.getItem('start_date');
  if (!d) { d = new Date().toISOString().split('T')[0]; localStorage.setItem('start_date', d); }
  return d;
}
function setStartDate(d) { localStorage.setItem('start_date', d); updateWeekDisplay(); renderDashboard(); }
function getSettings() {
  const stored = readJSON('settings', {});
  return {
    timer: stored.timer !== false,
    autoclose: stored.autoclose !== false
  };
}
function saveSettings(s) { localStorage.setItem('settings', JSON.stringify(s)); }
function getWorkoutDraft() { return readJSON('workout_draft', null); }
function saveWorkoutDraft() {
  if (!currentWorkout) return;
  if (editingHistoryIndex != null) return;
  localStorage.setItem('workout_draft', JSON.stringify({ currentDay, workout: currentWorkout, saved_at: new Date().toISOString() }));
}
function clearWorkoutDraft() { localStorage.removeItem('workout_draft'); }
function hasWorkoutInput(workout = currentWorkout) {
  if (!workout) return false;
  return !!(workout.note || workout.exercises.some(ex =>
    ex.note || ex.sets.some(setHasWorkoutData)
  ));
}

// ===== HELPERS =====
function normalizeExerciseName(name) {
  return String(name || '')
    .toLowerCase()
    .replace(/ё/g, 'е')
    .replace(/[–—]/g, '-')
    .replace(/\s+/g, ' ')
    .trim();
}
function getExerciseDefNames(ex) {
  return [ex && ex.name, ...((ex && Array.isArray(ex.aliases)) ? ex.aliases : [])]
    .map(n => String(n || '').trim())
    .filter(Boolean);
}
function exerciseNameMatchesDef(name, ex) {
  const key = normalizeExerciseName(name);
  return !!key && getExerciseDefNames(ex).some(n => normalizeExerciseName(n) === key);
}
function getProgramExerciseDef(exerciseName) {
  const program = getProgram();
  for (const dayKey of Object.keys(program.days || {})) {
    const found = (program.days[dayKey].exercises || []).find(e => exerciseNameMatchesDef(exerciseName, e));
    if (found) return found;
  }
  return null;
}
function getExerciseMatchKeys(exerciseName) {
  const names = [exerciseName];
  const def = getProgramExerciseDef(exerciseName);
  if (def) names.push(...getExerciseDefNames(def));
  return new Set(names.map(normalizeExerciseName).filter(Boolean));
}
function exerciseNameMatches(targetName, candidateName) {
  const candidate = normalizeExerciseName(candidateName);
  return !!candidate && getExerciseMatchKeys(targetName).has(candidate);
}
function getExerciseIdentityKey(exerciseName) {
  const def = getProgramExerciseDef(exerciseName);
  return normalizeExerciseName(def ? def.name : exerciseName);
}
function parseNameList(value) {
  return String(value || '')
    .split(',')
    .map(s => s.trim())
    .filter(Boolean);
}
function cleanExerciseAliases(aliases, currentName) {
  const currentKey = normalizeExerciseName(currentName);
  const seen = new Set();
  return parseNameList(Array.isArray(aliases) ? aliases.join(',') : aliases)
    .filter(name => {
      const key = normalizeExerciseName(name);
      if (!key || key === currentKey || seen.has(key)) return false;
      seen.add(key);
      return true;
    });
}
function getLastExerciseData(exerciseName) {
  const history = getHistory();
  for (let i = history.length - 1; i >= 0; i--) {
    const ex = history[i].exercises.find(e => exerciseNameMatches(exerciseName, e.name));
    if (ex && ex.sets.some(setHasLiftData)) return ex;
  }
  return null;
}
function normalizeNumber(value) {
  const n = parseFloat(String(value || '').replace(',', '.'));
  return Number.isFinite(n) ? n : null;
}
function fmtNum(value) {
  const n = normalizeNumber(value);
  if (n == null) return '';
  return Number.isInteger(n) ? String(n) : String(n).replace('.', ',');
}
function getDateKey(dateValue) {
  const d = new Date(dateValue);
  if (isNaN(d)) return '';
  const y = d.getFullYear();
  const m = String(d.getMonth() + 1).padStart(2, '0');
  const day = String(d.getDate()).padStart(2, '0');
  return `${y}-${m}-${day}`;
}
function getCalendarWeekStart(dateValue = new Date()) {
  const d = new Date(dateValue);
  d.setHours(0, 0, 0, 0);
  const offset = (d.getDay() + 6) % 7;
  d.setDate(d.getDate() - offset);
  return d;
}
function getMonthEnd(dateValue = new Date()) {
  const d = new Date(dateValue);
  return new Date(d.getFullYear(), d.getMonth() + 1, 0);
}
function addDays(dateValue, days) {
  const d = new Date(dateValue);
  d.setDate(d.getDate() + days);
  return d;
}
function daysBetween(a, b) {
  const da = new Date(a), db = new Date(b);
  da.setHours(0, 0, 0, 0);
  db.setHours(0, 0, 0, 0);
  return Math.floor((db - da) / 86400000);
}
function maxDate(...dates) {
  return dates.reduce((best, date) => {
    const d = new Date(date);
    if (isNaN(d)) return best;
    return !best || d > best ? d : best;
  }, null);
}
function hasWorkoutOnDate(dateValue) {
  const key = getDateKey(dateValue);
  return getHistory().some(w => getDateKey(w.date) === key);
}
function shortWorkoutName(name) {
  if (!name) return '';
  return String(name).split(' — ')[0].trim();
}
function getProgramWeekForDate(dateValue) {
  const start = new Date(getStartDate());
  const date = new Date(dateValue);
  if (isNaN(start) || isNaN(date)) return null;
  start.setHours(0, 0, 0, 0);
  date.setHours(0, 0, 0, 0);
  const days = Math.floor((date - start) / 86400000);
  if (days < 0) return null;
  return { week: Math.floor(days / 7) + 1, offset: days % 7 };
}
function getProgramWeekStartDate(week) {
  const start = new Date(getStartDate());
  start.setHours(0, 0, 0, 0);
  start.setDate(start.getDate() + (week - 1) * 7);
  return start;
}
function getPlannedWorkoutForDate(dateValue) {
  const slot = getProgramWeekForDate(dateValue);
  if (!slot) return null;
  const offsets = [0, 2, 4];
  const idx = offsets.indexOf(slot.offset);
  if (idx === -1) return null;
  const rotation = slot.week % 2 === 1 ? ROTATION.odd : ROTATION.even;
  const dayKey = rotation[idx];
  const day = getProgram().days[dayKey];
  if (!day) return null;
  return { day: dayKey, name: day.name, week: slot.week };
}
function cloneData(value) {
  return JSON.parse(JSON.stringify(value));
}
function setLocalDate(dateValue, dateKey) {
  const base = new Date(dateValue);
  const next = new Date(dateKey + 'T12:00:00');
  if (isNaN(next)) return dateValue;
  next.setHours(base.getHours(), base.getMinutes(), base.getSeconds(), base.getMilliseconds());
  return next.toISOString();
}
function hasDropSet(set) {
  const drop = set && set.drop;
  return !!(drop && (drop.enabled || drop.weight || drop.reps));
}
function dropSetHasData(set) {
  const drop = set && set.drop;
  return !!(drop && (drop.weight || drop.reps));
}
function setHasWorkoutData(set) {
  return !!(set && (set.weight || set.reps || set.rir || set.done || hasDropSet(set)));
}
function setHasLiftData(set) {
  return !!(set && (set.weight || set.reps || dropSetHasData(set)));
}
function getSetVolume(set) {
  if (!set) return 0;
  const weight = normalizeNumber(set.weight);
  const reps = parseInt(set.reps, 10);
  let total = weight != null && Number.isFinite(reps) ? weight * reps : 0;
  if (dropSetHasData(set)) {
    const dropWeight = normalizeNumber(set.drop.weight);
    const dropReps = parseInt(set.drop.reps, 10);
    if (dropWeight != null && Number.isFinite(dropReps)) total += dropWeight * dropReps;
  }
  return total;
}
function formatSetForHistory(set) {
  if (!set.weight && !set.reps && dropSetHasData(set)) return `дроп ${set.drop.weight || '?'}×${set.drop.reps || '?'}`;
  const main = `${set.weight || '?'}×${set.reps || '?'}${set.rir ? ` (R${set.rir})` : ''}`;
  if (!dropSetHasData(set)) return main;
  return `${main} ↓ ${set.drop.weight || '?'}×${set.drop.reps || '?'}`;
}
function getCurrentWeek() {
  const start = new Date(getStartDate());
  const now = new Date();
  const days = Math.floor((now - start) / 86400000);
  return Math.max(1, Math.floor(days / 7) + 1);
}
function isDeloadWeek(week) { return week === 7; }
function getSuggestedDay() {
  const week = getCurrentWeek();
  const rotation = week % 2 === 1 ? ROTATION.odd : ROTATION.even;
  const history = getHistory();
  const start = new Date(getStartDate());
  const weekStart = new Date(start);
  weekStart.setDate(weekStart.getDate() + (week - 1) * 7);
  const thisWeekDays = history.filter(w => new Date(w.date) >= weekStart).map(w => w.day);
  for (const day of rotation) { if (!thisWeekDays.includes(day)) return day; }
  return null;
}
function getWeekWorkouts(weekNum) {
  const start = new Date(getStartDate());
  const ws = new Date(start); ws.setDate(ws.getDate() + (weekNum - 1) * 7);
  const we = new Date(ws); we.setDate(we.getDate() + 7);
  return getHistory().filter(w => { const d = new Date(w.date); return d >= ws && d < we; });
}
function getStreak() {
  // Streaks of weeks with >= 2 workouts each. Count consecutive completed weeks ending at current week.
  const currentWeek = getCurrentWeek();
  let streak = 0;
  // Don't count current week if it's not complete yet AND has < 2 workouts
  const currentWeekWorkouts = getWeekWorkouts(currentWeek).length;
  if (currentWeekWorkouts >= 2) streak = 1;
  // Count back
  for (let w = currentWeek - 1; w >= 1; w--) {
    if (getWeekWorkouts(w).length >= 2) streak++;
    else break;
  }
  return streak;
}
function setWeek(w) {
  w = Math.max(1, Math.min(20, parseInt(w) || 1));
  const newStart = new Date();
  newStart.setDate(newStart.getDate() - (w - 1) * 7);
  localStorage.setItem('start_date', newStart.toISOString().split('T')[0]);
  updateWeekDisplay();
  renderDashboard();
}
function stepWeek(d) { setWeek(getCurrentWeek() + d); }

// ===== PR DETECTION =====
function isPR(exerciseName, weight, reps) {
  const history = getHistory();
  let bestE1RM = 0;
  history.forEach(w => {
    const ex = w.exercises.find(e => exerciseNameMatches(exerciseName, e.name));
    if (!ex) return;
    ex.sets.forEach(s => {
      const wv = parseFloat(s.weight), r = parseInt(s.reps);
      if (isNaN(wv) || isNaN(r) || r >= 37) return;
      const e1rm = wv * (36 / (37 - r));
      if (e1rm > bestE1RM) bestE1RM = e1rm;
    });
  });
  const currentE1RM = weight * (36 / (37 - reps));
  return currentE1RM > bestE1RM;
}

function getWorkingSetsFromLast(lastExercise, count) {
  const valid = lastExercise && lastExercise.sets ? lastExercise.sets.filter(s => s.weight && s.reps) : [];
  if (valid.length <= count) return valid;
  return valid.slice(valid.length - count);
}

// ===== MOTION =====
function prefersReducedMotion() {
  return window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
}
function animateScreen(screen) {
  if (!screen || prefersReducedMotion() || !screen.animate) return;
  screen.animate([
    { opacity: 0, transform: 'translateY(10px) scale(.992)' },
    { opacity: 1, transform: 'translateY(0) scale(1)' }
  ], { duration: 240, easing: 'cubic-bezier(.2,.7,.2,1)' });

  const items = screen.querySelectorAll('.hero, .cta, .deload-banner, .stat, .week-bar, .day-btn, .exercise, .chart-card, .measure-form, .history-day, .info-box, .toggle-row, .btn-primary, .btn-secondary');
  items.forEach((item, i) => {
    item.classList.add('reveal-item');
    item.animate([
      { opacity: 0, transform: 'translateY(12px)' },
      { opacity: 1, transform: 'translateY(0)' }
    ], {
      duration: 260,
      delay: Math.min(i, 8) * 28,
      easing: 'cubic-bezier(.2,.7,.2,1)'
    });
  });
}
function animateDashboard() {
  if (prefersReducedMotion()) return;

  const ring = document.querySelector('#dash-content .ring-prog');
  if (ring) {
    const total = ring.getAttribute('stroke-dasharray');
    const target = ring.getAttribute('data-target-offset') || ring.getAttribute('stroke-dashoffset');
    ring.style.strokeDashoffset = total;
    requestAnimationFrame(() => {
      ring.style.strokeDashoffset = target;
    });
  }

  document.querySelectorAll('[data-count-to]').forEach((el) => {
    const target = Number(el.dataset.countTo);
    if (!Number.isFinite(target)) return;
    const suffix = el.dataset.suffix || '';
    const duration = 520;
    const start = performance.now();
    const step = (now) => {
      const t = Math.min(1, (now - start) / duration);
      const eased = 1 - Math.pow(1 - t, 3);
      el.textContent = Math.round(target * eased) + suffix;
      if (t < 1) requestAnimationFrame(step);
    };
    requestAnimationFrame(step);
  });
}
function initTapAnimations() {
  document.addEventListener('pointerdown', (event) => {
    const target = event.target.closest('button, .toggle');
    if (!target || prefersReducedMotion()) return;
    target.classList.add('tap-anim');
    const rect = target.getBoundingClientRect();
    const ripple = document.createElement('span');
    ripple.className = 'tap-ripple';
    ripple.style.left = `${event.clientX - rect.left}px`;
    ripple.style.top = `${event.clientY - rect.top}px`;
    const size = Math.max(rect.width, rect.height) * 2.4;
    target.appendChild(ripple);
    if (!ripple.animate) {
      ripple.remove();
      return;
    }
    ripple.animate([
      { transform: 'translate(-50%, -50%) scale(0)', opacity: .18 },
      { transform: `translate(-50%, -50%) scale(${size / 16})`, opacity: 0 }
    ], { duration: 420, easing: 'cubic-bezier(.2,.7,.2,1)' }).onfinish = () => ripple.remove();
  });
}

// ===== NAV =====
function isSectionVisible(name) {
  return ALWAYS_VISIBLE_SECTIONS.has(name) || OPTIONAL_SECTIONS.some(section => section.key === name);
}
function applySectionVisibility() {
  const nav = document.querySelector('.nav');
  document.querySelectorAll('.nav-btn').forEach(btn => {
    btn.classList.remove('section-hidden');
    btn.hidden = false;
  });
  if (nav) nav.style.setProperty('--nav-count', '3');
}
function switchToScreen(name, animate = true) {
  if (!isSectionVisible(name)) name = 'dashboard';
  const navName = ['dashboard', 'workout', 'settings'].includes(name) ? name : 'dashboard';
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.toggle('active', b.dataset.screen === navName));
  document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
  const screen = document.getElementById('screen-' + name);
  if (!screen) return;
  screen.classList.add('active');
  if (name === 'dashboard') renderDashboard();
  if (name === 'workout') renderDaySelector();
  if (name === 'history') renderHistory();
  if (name === 'progress') initProgress();
  if (name === 'measure') renderMeasures();
  if (name === 'health') renderHealth();
  if (name === 'food') renderFood();
  if (name === 'settings') initSettings();
  if (animate) animateScreen(screen);
}
document.querySelectorAll('.nav-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    switchToScreen(btn.dataset.screen);
  });
});

// ===== DASHBOARD =====
function renderDashboardCalendar(today = new Date()) {
  const start = getCalendarWeekStart(today);
  const end = getMonthEnd(today);
  const todayKey = getDateKey(today);
  const history = getHistory();
  const program = getProgram();
  const weekdays = ['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс'];
  const planOffsets = [0, 2, 4];
  const weekState = new Map();
  let lastTrainingDate = null;
  function getState(week) {
    if (!weekState.has(week)) weekState.set(week, new Set());
    return weekState.get(week);
  }
  const daysCount = Math.max(1, Math.floor((end - start) / 86400000) + 1);
  const days = Array.from({ length: daysCount }, (_, idx) => {
    const date = new Date(start);
    date.setDate(start.getDate() + idx);
    const key = getDateKey(date);
    const slot = getProgramWeekForDate(date);
    const workouts = history.filter(w => getDateKey(w.date) === key);
    workouts.forEach(w => {
      const workoutSlot = getProgramWeekForDate(w.date);
      if (workoutSlot && w.day) getState(workoutSlot.week).add(w.day);
    });
    const names = workouts.map(w => shortWorkoutName(w.dayName)).filter(Boolean);
    let planned = null;
    if (workouts.length === 0 && key >= todayKey && date.getMonth() === today.getMonth() && slot && !isDeloadWeek(slot.week)) {
      const rotation = slot.week % 2 === 1 ? ROTATION.odd : ROTATION.even;
      const state = getState(slot.week);
      const nextIdx = rotation.findIndex(dayKey => !state.has(dayKey));
      if (nextIdx !== -1) {
        const targetDate = addDays(getProgramWeekStartDate(slot.week), planOffsets[nextIdx]);
        const minAfterLast = lastTrainingDate ? addDays(lastTrainingDate, 2) : null;
        const planDate = maxDate(targetDate, today, minAfterLast || targetDate);
        if (getDateKey(planDate) === key) {
          const dayKey = rotation[nextIdx];
          const day = program.days[dayKey];
          if (day) {
            planned = { day: dayKey, name: day.name, week: slot.week };
            state.add(dayKey);
          }
        }
      }
    }
    if (workouts.length || planned) lastTrainingDate = date;
    const showPlan = !!planned;
    const label = names.length > 1 ? `${names[0]} +${names.length - 1}` : (names[0] || (showPlan ? shortWorkoutName(planned.name) : ''));
    const classes = ['cal-day'];
    if (date.getMonth() !== today.getMonth()) classes.push('muted');
    if (key === todayKey) classes.push('today');
    if (workouts.length) classes.push('done');
    if (showPlan) classes.push('planned');
    return `<div class="${classes.join(' ')}">
      <div class="cal-weekday">${weekdays[(date.getDay() + 6) % 7]}</div>
      <div class="cal-num">${date.getDate()}</div>
      <div class="cal-today-label">${key === todayKey ? 'Сегодня' : ''}</div>
      <div class="cal-workout">${label ? escapeHTML(label) : ''}</div>
    </div>`;
  }).join('');
  const monthName = today.toLocaleDateString('ru-RU', { month: 'long' });
  return `<div class="dash-calendar-head"><h2>Календарь</h2><div class="dash-calendar-range">${monthName} до ${end.getDate()}</div></div>
    <div class="dash-calendar-scroll"><div class="dash-calendar">${days}</div></div>`;
}
function renderDashboardLinks() {
  const order = ['history', 'progress', 'measure', 'health', 'food'];
  const links = order
    .map(key => OPTIONAL_SECTIONS.find(section => section.key === key))
    .filter(Boolean)
    .map(section => `<button class="dash-link" onclick="switchToScreen('${section.key}')">
      ${DASH_LINK_ICONS[section.key] || ''}
      <span>${escapeHTML(section.label)}</span>
    </button>`)
    .join('');
  return links ? `<div class="dash-links">${links}</div>` : '';
}
function renderRecoverySummary() {
  const rows = getHealthDaily();
  if (!rows.length) return '';
  const sleepRow = getLatestHealthMetric('sleep_asleep_min');
  const hrvRow = getLatestHealthMetric('hrv_sdnn_ms');
  const rhrRow = getLatestHealthMetric('resting_hr_bpm');
  const activeRow = getLatestActivityMetricRow('active_energy_kcal');
  const cards = [];
  if (sleepRow && sleepRow.sleep_asleep_min != null) {
    cards.push(`<div class="stat"><div class="stat-val">${formatHealthValue(sleepRow, 'sleep_asleep_min', 'ч', v => round1(v / 60))}</div><div class="stat-lbl">Сон</div><div class="stat-date">${formatHealthStatDate(sleepRow)}</div></div>`);
  }
  if (hrvRow && hrvRow.hrv_sdnn_ms != null) {
    cards.push(`<div class="stat"><div class="stat-val">${formatHealthValue(hrvRow, 'hrv_sdnn_ms', 'мс')}</div><div class="stat-lbl">HRV</div><div class="stat-date">${formatHealthStatDate(hrvRow)}</div></div>`);
  }
  if (rhrRow && rhrRow.resting_hr_bpm != null) {
    cards.push(`<div class="stat"><div class="stat-val">${formatHealthValue(rhrRow, 'resting_hr_bpm')}</div><div class="stat-lbl">Пульс покоя</div><div class="stat-date">${formatHealthStatDate(rhrRow)}</div></div>`);
  }
  if (activeRow && activeRow.active_energy_kcal != null) {
    cards.push(`<div class="stat"><div class="stat-val burned-calories">${formatHealthValue(activeRow, 'active_energy_kcal', 'ккал')}</div><div class="stat-lbl">Активные</div><div class="stat-date">${formatHealthStatDate(activeRow)}</div></div>`);
  }
  if (!cards.length) return '';
  const hasRecovery = cards.length && (sleepRow || hrvRow || rhrRow);
  return `<h2>${hasRecovery ? 'Восстановление' : 'Активность'}</h2>
    <div class="stat-grid">${cards.join('')}</div>`;
}
function renderDashboard() {
  const week = getCurrentWeek();
  const totalWorkouts = getHistory().length;
  const streak = getStreak();
  const thisWeekDone = getWeekWorkouts(week).length;
  const suggested = getSuggestedDay();
  const program = getProgram();
  const deload = isDeloadWeek(week);
  const today = new Date();

  const dateEl = document.getElementById('dash-date');
  if (dateEl) dateEl.textContent = today.toLocaleDateString('ru-RU', { weekday: 'long', day: 'numeric', month: 'long' });

  const lastWorkout = getHistory()[getHistory().length - 1];
  let daysSince = '—';
  if (lastWorkout) {
    const lastDay = new Date(lastWorkout.date);
    lastDay.setHours(0, 0, 0, 0);
    const todayDay = new Date(today);
    todayDay.setHours(0, 0, 0, 0);
    const d = Math.floor((todayDay - lastDay) / 86400000);
    daysSince = d === 0 ? 'сегодня' : d === 1 ? 'вчера' : `${d} д.`;
  }

  // Ring math
  const R = 38, C = 2 * Math.PI * R;
  const wkPct = Math.max(0, Math.min(1, week / 12));
  const wkOff = C * (1 - wkPct);

  let html = '';

  // Hero: week progress ring + meta
  html += `<div class="hero">
    <div class="ring">
      <svg viewBox="0 0 96 96">
        <circle class="ring-track" cx="48" cy="48" r="${R}" fill="none" stroke-width="6"/>
        <circle class="ring-prog"  cx="48" cy="48" r="${R}" fill="none" stroke-width="6"
                stroke-dasharray="${C.toFixed(2)}" stroke-dashoffset="${wkOff.toFixed(2)}" data-target-offset="${wkOff.toFixed(2)}"/>
      </svg>
      <div class="ring-num">${week}<small>из 12</small></div>
    </div>
    <div class="hero-meta">
      <div class="eyebrow">Программа</div>
      <div class="h-title">${deload ? 'Deload-неделя' : `Неделя ${week}`}</div>
      <div class="h-sub">${thisWeekDone}/3 трен. на этой неделе</div>
    </div>
  </div>`;

  if (deload) {
    html += `<div class="deload-banner"><div class="deload-icon">!</div><div><b>Разгрузочная неделя.</b> Бери −40% от рабочих весов, повторы те же, RIR 3. Не лень — восстановление связок. Пропустишь — травма на 9-й.</div></div>`;
  }

  // CTA
  if (suggested) {
    const sugDay = program.days[suggested];
    const sugTitle = sugDay.name.split(' — ')[0];
    const sugSub = sugDay.name.split(' — ')[1] || '';
    html += `<button class="cta" onclick="startWorkoutFromDash('${suggested}')">
      <div class="cta-arrow"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><polygon points="6,4 20,12 6,20" fill="currentColor" stroke="none"/></svg></div>
      <div class="cta-text">
        <div class="cta-eyebrow">Следующая тренировка</div>
        <div class="cta-title">${escapeHTML(sugTitle)}</div>
        <div class="h-sub" style="margin-top:3px">${escapeHTML(sugSub)}</div>
      </div>
    </button>`;
  } else if (thisWeekDone >= 3) {
    html += `<div class="cta" style="cursor:default;background:var(--good-soft);border-color:oklch(0.78 0.14 145 / 0.3);">
      <div class="cta-arrow" style="background:var(--good);"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><polyline points="5,12 10,17 19,7"/></svg></div>
      <div class="cta-text">
        <div class="cta-eyebrow" style="color:var(--good)">Неделя выполнена</div>
        <div class="cta-title">3 из 3</div>
        <div class="h-sub" style="margin-top:3px">Можешь сделать ещё, если есть силы.</div>
      </div>
    </div>`;
  }

  html += renderDashboardCalendar(today);
  html += renderDashboardLinks();

  // Stat grid
  html += `<h2>Сводка</h2>
  <div class="stat-grid">
    <div class="stat"><div class="stat-val flame"><span data-count-to="${streak}">${streak}</span><span class="unit">нед.</span></div><div class="stat-lbl">Стрик</div></div>
    <div class="stat"><div class="stat-val"><span data-count-to="${totalWorkouts}">${totalWorkouts}</span></div><div class="stat-lbl">Всего трен.</div></div>
    <div class="stat"><div class="stat-val">${daysSince}</div><div class="stat-lbl">Последняя</div></div>
    <div class="stat"><div class="stat-val"><span data-count-to="${Math.max(0, 12 - week)}">${Math.max(0, 12 - week)}</span><span class="unit">нед.</span></div><div class="stat-lbl">Осталось</div></div>
  </div>`;

  document.getElementById('dash-content').innerHTML = html;
  animateDashboard();
}
function startWorkoutFromDash(dayKey) {
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  document.querySelector('.nav-btn[data-screen="workout"]').classList.add('active');
  document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
  const screen = document.getElementById('screen-workout');
  screen.classList.add('active');
  renderDaySelector();
  startWorkout(dayKey);
  document.querySelectorAll('.day-btn').forEach(b => b.classList.remove('active'));
  const btn = document.querySelector(`.day-btn[data-day="${dayKey}"]`);
  if (btn) btn.classList.add('active');
  animateScreen(screen);
}

// ===== WORKOUT =====
function renderDaySelector() {
  const program = getProgram();
  const sel = document.getElementById('day-selector');
  sel.innerHTML = Object.entries(program.days).map(([key, day]) => {
    const short = key === 'upperA' ? 'Грудь·Плечи' : key === 'upperB' ? 'Спина·Биц' : 'Ноги·Кор';
    const label = key === 'upperA' ? 'Upper A' : key === 'upperB' ? 'Upper B' : 'Lower';
    return `<button class="day-btn" data-day="${key}"><span class="d-label">${label}</span><span class="d-sub">${short}</span></button>`;
  }).join('');
  sel.querySelectorAll('.day-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      sel.querySelectorAll('.day-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      startWorkout(btn.dataset.day);
      animateScreen(document.getElementById('screen-workout'));
    });
  });
  updateWeekDisplay();
  // Deload banner
  const week = getCurrentWeek();
  document.getElementById('deload-banner').innerHTML = isDeloadWeek(week) 
    ? `<div class="deload-banner"><div class="deload-icon">!</div><div><b>Неделя 7 — Deload.</b> Веса −40%, RIR 3.</div></div>` : '';
  renderDraftBanner();
  renderHistoryEditBanner();
}

function updateWeekDisplay() {
  const w = getCurrentWeek();
  const wd = document.getElementById('week-display');
  if (wd) wd.innerHTML = `<em>Неделя ${w}</em>`;
  const wi = document.getElementById('week-input');
  if (wi) wi.value = w;
  const sd = document.getElementById('start-date');
  if (sd) sd.value = getStartDate();
  document.querySelectorAll('.day-btn').forEach(b => {
    b.classList.remove('suggested', 'next-up');
    b.removeAttribute('data-badge');
  });
  const sug = getSuggestedDay();
  if (sug) {
    const btn = document.querySelector(`.day-btn[data-day="${sug}"]`);
    if (btn) {
      const trainedToday = hasWorkoutOnDate(new Date());
      btn.classList.add('suggested');
      if (trainedToday) btn.classList.add('next-up');
      btn.dataset.badge = trainedToday ? 'дальше' : 'сегодня';
    }
  }
  if (currentDay) {
    const active = document.querySelector(`.day-btn[data-day="${currentDay}"]`);
    if (active) active.classList.add('active');
  }
}

function renderDraftBanner() {
  const holder = document.getElementById('draft-banner');
  if (!holder) return;
  const draft = getWorkoutDraft();
  if (!draft || currentWorkout) {
    holder.innerHTML = '';
    return;
  }
  const d = draft.saved_at ? new Date(draft.saved_at).toLocaleString('ru-RU', { day: 'numeric', month: 'short', hour: '2-digit', minute: '2-digit' }) : '';
  holder.innerHTML = `<div class="draft-banner">
    <div><b>Есть незавершенная тренировка.</b>${d ? ` Сохранена ${d}.` : ''}</div>
    <div class="draft-actions">
      <button onclick="restoreWorkoutDraft()">Продолжить</button>
      <button onclick="discardWorkoutDraft()">Удалить</button>
    </div>
  </div>`;
}
function updateFinishButtonLabel() {
  const btn = document.getElementById('finish-btn');
  if (btn) btn.textContent = editingHistoryIndex != null ? 'Сохранить изменения' : 'Завершить тренировку';
}
function renderHistoryEditBanner() {
  const holder = document.getElementById('history-edit-banner');
  if (!holder) return;
  if (editingHistoryIndex == null || !currentWorkout) {
    holder.classList.remove('active');
    holder.innerHTML = '';
    updateFinishButtonLabel();
    return;
  }
  holder.classList.add('active');
  holder.innerHTML = `
    <div class="history-edit-banner-title">Редактирование записи из истории</div>
    <div class="history-edit-controls">
      <label>Дата тренировки
        <input type="date" value="${escapeHTML(getDateKey(currentWorkout.date))}" onchange="updateWorkoutDate(this.value)">
      </label>
      <button onclick="cancelHistoryEdit()">Отмена</button>
      <button class="history-edit-delete" onclick="deleteEditingHistoryWorkout()">Удалить</button>
    </div>
  `;
  updateFinishButtonLabel();
}
function resetWorkoutScreen() {
  currentWorkout = null;
  currentDay = null;
  editingHistoryIndex = null;
  document.querySelectorAll('.day-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('workout-title').textContent = 'Выбери день';
  document.getElementById('workout-date').textContent = '';
  document.getElementById('exercises-list').innerHTML = '';
  document.getElementById('workout-note').value = '';
  document.getElementById('workout-note-container').style.display = 'none';
  document.getElementById('finish-btn').style.display = 'none';
  renderDraftBanner();
  renderHistoryEditBanner();
  updateWeekDisplay();
}
function updateWorkoutDate(dateKey) {
  if (!currentWorkout || !dateKey) return;
  currentWorkout.date = setLocalDate(currentWorkout.date, dateKey);
  const d = new Date(currentWorkout.date);
  document.getElementById('workout-date').textContent = d.toLocaleDateString('ru-RU', { weekday: 'long', day: 'numeric', month: 'long' });
  saveWorkoutDraft();
}
function cancelHistoryEdit() {
  if (!confirm('Отменить редактирование? Несохраненные изменения пропадут.')) return;
  resetWorkoutScreen();
  switchToScreen('history');
}
function deleteEditingHistoryWorkout() {
  if (editingHistoryIndex == null) return;
  const history = getHistory();
  const workout = history[editingHistoryIndex];
  if (!workout) {
    alert('Не нашел эту тренировку в истории.');
    resetWorkoutScreen();
    switchToScreen('history');
    return;
  }
  const date = new Date(workout.date).toLocaleDateString('ru-RU', { day: 'numeric', month: 'long' });
  const title = shortWorkoutName(workout.dayName || workout.day || 'тренировку');
  if (!confirm(`Удалить ${title} за ${date}? Это нельзя отменить.`)) return;
  history.splice(editingHistoryIndex, 1);
  saveHistory(history);
  clearWorkoutDraft();
  resetWorkoutScreen();
  renderDashboard();
  switchToScreen('history');
  alert('Тренировка удалена ✓');
}
function editHistoryWorkout(index) {
  const history = getHistory();
  const workout = history[index];
  if (!workout) { alert('Не нашел эту тренировку в истории.'); return; }
  if (currentWorkout && !confirm('Сейчас открыта другая тренировка. Перейти к редактированию записи из истории?')) return;
  clearWorkoutDraft();
  editingHistoryIndex = index;
  currentWorkout = cloneData(workout);
  currentDay = currentWorkout.day;
  switchToScreen('workout', false);
  document.getElementById('workout-title').textContent = currentWorkout.dayName;
  const d = new Date(currentWorkout.date);
  document.getElementById('workout-date').textContent = d.toLocaleDateString('ru-RU', { weekday: 'long', day: 'numeric', month: 'long' });
  document.querySelectorAll('.day-btn').forEach(b => b.classList.toggle('active', b.dataset.day === currentDay));
  document.getElementById('workout-note').value = currentWorkout.note || '';
  document.getElementById('finish-btn').style.display = 'block';
  document.getElementById('workout-note-container').style.display = 'block';
  renderDraftBanner();
  renderHistoryEditBanner();
  renderExercises();
  animateScreen(document.getElementById('screen-workout'));
}
function restoreWorkoutDraft() {
  const draft = getWorkoutDraft();
  if (!draft || !draft.workout) return;
  editingHistoryIndex = null;
  currentDay = draft.currentDay || draft.workout.day;
  currentWorkout = draft.workout;
  document.getElementById('workout-title').textContent = currentWorkout.dayName;
  const d = new Date(currentWorkout.date);
  document.getElementById('workout-date').textContent = d.toLocaleDateString('ru-RU', { weekday: 'long', day: 'numeric', month: 'long' });
  document.querySelectorAll('.day-btn').forEach(b => b.classList.toggle('active', b.dataset.day === currentDay));
  document.getElementById('workout-note').value = currentWorkout.note || '';
  document.getElementById('finish-btn').style.display = 'block';
  document.getElementById('workout-note-container').style.display = 'block';
  renderDraftBanner();
  renderHistoryEditBanner();
  renderExercises();
}
function discardWorkoutDraft() {
  if (!confirm('Удалить черновик тренировки?')) return;
  clearWorkoutDraft();
  renderDraftBanner();
}

function startWorkout(dayKey) {
  if (editingHistoryIndex != null && !confirm('Выйти из редактирования истории и начать новую тренировку?')) return;
  editingHistoryIndex = null;
  if (currentWorkout && hasWorkoutInput() && !confirm('Текущая тренировка не завершена. Начать новую и заменить черновик?')) return;
  if (!currentWorkout && getWorkoutDraft() && !confirm('Есть незавершенная тренировка. Начать новую и заменить черновик?')) return;
  const program = getProgram();
  currentDay = dayKey;
  const day = program.days[dayKey];
  currentWorkout = {
    date: new Date().toISOString(),
    day: dayKey,
    dayName: day.name,
    week: getCurrentWeek(),
    programVersion: program.version,
    note: '',
    exercises: day.exercises.map(ex => createWorkoutExercise(ex))
  };
  document.getElementById('workout-title').textContent = day.name;
  const d = new Date();
  document.getElementById('workout-date').textContent = d.toLocaleDateString('ru-RU', { weekday: 'long', day: 'numeric', month: 'long' });
  renderExercises();
  saveWorkoutDraft();
  renderDraftBanner();
  renderHistoryEditBanner();
  document.getElementById('finish-btn').style.display = 'block';
  document.getElementById('workout-note-container').style.display = 'block';
}

function createWorkoutExercise(ex) {
  const last = getLastExerciseData(ex.name);
  const sourceSets = getWorkingSetsFromLast(last, ex.sets);
  return {
    name: ex.name,
    aliases: Array.isArray(ex.aliases) ? ex.aliases.slice() : [],
    target: ex.target,
    rest: ex.rest,
    note: '',
    sets: Array(ex.sets).fill(null).map((_, idx) => {
      const lastSet = sourceSets[idx] || (last && last.sets[idx]);
      return {
        weight: lastSet && lastSet.weight ? lastSet.weight : '',
        reps: lastSet && lastSet.reps ? lastSet.reps : '',
        rir: '',
        done: false,
        drop: { enabled: false, weight: '', reps: '' }
      };
    })
  };
}

function renderExercises() {
  const list = document.getElementById('exercises-list');
  list.innerHTML = '';
  currentWorkout.exercises.forEach((ex, exIdx) => {
    const last = getLastExerciseData(ex.name);
    const safeName = escapeHTML(ex.name);
    const safeTarget = escapeHTML(ex.target || '');

    const card = document.createElement('div');
    card.className = 'exercise';
    card.innerHTML = `
      <div class="exercise-header">
        <div style="flex: 1; min-width: 0;">
          <div class="exercise-name">${safeName}</div>
          <div class="exercise-target">${safeTarget}</div>
        </div>
      </div>
      <div class="ex-toolbar">
        <button class="icon-btn" onclick="moveExercise(${exIdx}, -1)" ${exIdx === 0 ? 'disabled' : ''} aria-label="Вверх">↑</button>
        <button class="icon-btn" onclick="moveExercise(${exIdx}, 1)" ${exIdx === currentWorkout.exercises.length - 1 ? 'disabled' : ''} aria-label="Вниз">↓</button>
        <button class="icon-btn" onclick="openSwap(${exIdx})">⇄ Замена</button>
      </div>
      <div class="header-labels"><span>#</span><span>кг</span><span>повт</span><span>RIR</span><span></span><span>drop</span></div>
      <div class="sets">${ex.sets.map((s, sIdx) => renderSetRow(exIdx, sIdx, s, last)).join('')}</div>
      ${last ? renderCompareRow(ex, last) : ''}
      <div class="exercise-note-section">
        <label for="exercise-note-${exIdx}">Заметка к упражнению</label>
        <textarea id="exercise-note-${exIdx}" placeholder="Техника, ощущения, боль, что поменять в следующий раз" oninput="updateExerciseNote(${exIdx}, this.value)">${escapeHTML(ex.note || '')}</textarea>
      </div>
      <button class="add-set" onclick="addSet(${exIdx})">+ Добавить подход</button>
    `;
    list.appendChild(card);
  });
}

function renderCompareRow(currentEx, lastEx) {
  const currValid = currentEx.sets.filter(s => s.weight && s.reps);
  if (currValid.length === 0) return '';
  const currTon = currentEx.sets.reduce((sum, s) => sum + getSetVolume(s), 0);
  const lastValid = lastEx.sets.filter(s => s.weight && s.reps);
  if (lastValid.length === 0) return '';
  const lastTon = lastEx.sets.reduce((sum, s) => sum + getSetVolume(s), 0);
  const delta = currTon - lastTon;
  const cls = delta > 0 ? 'up' : delta < 0 ? 'down' : 'same';
  const arrow = delta > 0 ? '↑' : delta < 0 ? '↓' : '=';
  // PR check
  let prText = '';
  for (const s of currValid) {
    const w = parseFloat(s.weight), r = parseInt(s.reps);
    if (!isNaN(w) && !isNaN(r) && r < 37 && isPR(currentEx.name, w, r)) { prText = ' <span class="pr-badge">🏆 PR</span>'; break; }
  }
  return `<div class="compare-row">vs прошлый: <span class="${cls}">${arrow} ${delta >= 0 ? '+' : ''}${delta.toFixed(0)} кг</span> объёма${prText}</div>`;
}

function renderSetRow(exIdx, sIdx, set, lastEx) {
  const lastSet = lastEx && lastEx.sets[sIdx];
  const wPh = lastSet ? escapeHTML(lastSet.weight) : '';
  const rPh = lastSet ? escapeHTML(lastSet.reps) : '';
  const drop = set.drop || { enabled: false, weight: '', reps: '' };
  const dropActive = hasDropSet(set);
  const dropWPh = lastSet && lastSet.drop ? escapeHTML(lastSet.drop.weight) : '';
  const dropRPh = lastSet && lastSet.drop ? escapeHTML(lastSet.drop.reps) : '';
  const dropRow = dropActive ? `
    <div class="drop-row" data-ex-idx="${exIdx}" data-set-idx="${sIdx}">
      <div class="drop-row-label">DROP</div>
      <input type="number" inputmode="decimal" class="drop-input" placeholder="${dropWPh || 'кг'}" value="${escapeHTML(drop.weight)}" onchange="updateDropSet(${exIdx}, ${sIdx}, 'weight', this.value)" aria-label="Вес дропсета">
      <input type="number" inputmode="numeric" class="drop-input" placeholder="${dropRPh || 'повт'}" value="${escapeHTML(drop.reps)}" onchange="updateDropSet(${exIdx}, ${sIdx}, 'reps', this.value)" aria-label="Повторы дропсета">
    </div>
  ` : '';
  return `
    <div class="set-wrap" data-ex-idx="${exIdx}" data-set-idx="${sIdx}">
      <button class="set-delete-btn" onclick="deleteSet(${exIdx}, ${sIdx}); event.stopPropagation();" aria-label="Удалить подход">×</button>
      <div class="set-row ${set.done ? 'done' : ''}" data-ex-idx="${exIdx}" data-set-idx="${sIdx}">
        <div class="set-num">${sIdx + 1}</div>
        <input type="number" inputmode="decimal" class="set-input ${set.done ? 'done' : ''}" placeholder="${wPh}" value="${escapeHTML(set.weight)}" onchange="updateSet(${exIdx}, ${sIdx}, 'weight', this.value)">
        <input type="number" inputmode="numeric" class="set-input ${set.done ? 'done' : ''}" placeholder="${rPh}" value="${escapeHTML(set.reps)}" onchange="updateSet(${exIdx}, ${sIdx}, 'reps', this.value)">
        <input type="number" inputmode="numeric" class="rir-input" placeholder="–" value="${escapeHTML(set.rir)}" min="0" max="5" onchange="updateSet(${exIdx}, ${sIdx}, 'rir', this.value)">
        <button class="check-btn ${set.done ? 'done' : ''}" onclick="toggleSet(${exIdx}, ${sIdx})" aria-label="Отметить"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><polyline points="5,12 10,17 19,7"/></svg></button>
        <button class="drop-toggle ${dropActive ? 'active' : ''}" onclick="toggleDropSet(${exIdx}, ${sIdx})" aria-label="Дропсет подхода ${sIdx + 1}" title="Дропсет">DROP</button>
      </div>
    </div>
    ${dropRow}
  `;
}

function updateSet(exIdx, sIdx, field, value) {
  const set = currentWorkout.exercises[exIdx].sets[sIdx];
  set[field] = value;
  saveWorkoutDraft();
  updateSetRowState(exIdx, sIdx);
  updateExerciseCompare(exIdx);
}
function updateSetRowState(exIdx, sIdx) {
  const row = document.querySelector(`.set-row[data-ex-idx="${exIdx}"][data-set-idx="${sIdx}"]`);
  const set = currentWorkout && currentWorkout.exercises[exIdx] && currentWorkout.exercises[exIdx].sets[sIdx];
  if (!row || !set) return;
  row.classList.toggle('done', !!set.done);
  row.querySelectorAll('.set-input').forEach(input => input.classList.toggle('done', !!set.done));
  const btn = row.querySelector('.check-btn');
  if (btn) btn.classList.toggle('done', !!set.done);
  const dropBtn = row.querySelector('.drop-toggle');
  if (dropBtn) dropBtn.classList.toggle('active', hasDropSet(set));
}
function ensureDropSet(set) {
  if (!set.drop) set.drop = { enabled: false, weight: '', reps: '' };
  return set.drop;
}
function toggleDropSet(exIdx, sIdx) {
  const set = currentWorkout.exercises[exIdx].sets[sIdx];
  const drop = ensureDropSet(set);
  const active = hasDropSet(set);
  drop.enabled = !active;
  if (!drop.enabled) {
    drop.weight = '';
    drop.reps = '';
  }
  saveWorkoutDraft();
  renderExercises();
}
function updateDropSet(exIdx, sIdx, field, value) {
  const set = currentWorkout.exercises[exIdx].sets[sIdx];
  const drop = ensureDropSet(set);
  drop.enabled = true;
  drop[field] = value;
  saveWorkoutDraft();
  updateExerciseCompare(exIdx);
}
function closeSetDeleteButtons(except = null) {
  document.querySelectorAll('.set-wrap.show-delete').forEach(wrap => {
    if (wrap !== except) wrap.classList.remove('show-delete');
  });
}
function deleteSet(exIdx, sIdx) {
  if (!currentWorkout || !currentWorkout.exercises[exIdx]) return;
  const sets = currentWorkout.exercises[exIdx].sets;
  if (!sets[sIdx]) return;
  if (sets.length <= 1) {
    sets[0] = { weight: '', reps: '', rir: '', done: false, drop: { enabled: false, weight: '', reps: '' } };
  } else {
    sets.splice(sIdx, 1);
  }
  saveWorkoutDraft();
  renderExercises();
}
function initSetSwipeGestures() {
  const list = document.getElementById('exercises-list');
  if (!list || list.dataset.swipeReady) return;
  list.dataset.swipeReady = '1';
  const startSwipe = (event, point) => {
    const row = event.target.closest('.set-row');
    const wrap = row && row.closest('.set-wrap');
    if (!row || !wrap) return;
    if (event.button != null && event.button > 0) return;
    setSwipeState = {
      wrap,
      row,
      startX: point.clientX,
      startY: point.clientY,
      lastX: point.clientX,
      dragging: false
    };
  };
  const moveSwipe = (event, point) => {
    if (!setSwipeState) return;
    const dx = point.clientX - setSwipeState.startX;
    const dy = point.clientY - setSwipeState.startY;
    setSwipeState.lastX = point.clientX;
    if (dx > 10 && Math.abs(dx) > Math.abs(dy) * 1.3) {
      setSwipeState.dragging = true;
      setSwipeState.wrap.classList.add('swiping-delete');
      setSwipeState.row.style.transform = `translateX(${Math.min(58, dx)}px)`;
      event.preventDefault();
    }
    if (dx < -16 && setSwipeState.wrap.classList.contains('show-delete')) {
      setSwipeState.wrap.classList.remove('show-delete');
    }
  };
  const endSwipe = point => {
    if (!setSwipeState) return;
    const dx = (point && point.clientX ? point.clientX : setSwipeState.lastX) - setSwipeState.startX;
    setSwipeState.row.style.transform = '';
    setSwipeState.wrap.classList.remove('swiping-delete');
    if (setSwipeState.dragging && dx > 46) {
      closeSetDeleteButtons(setSwipeState.wrap);
      setSwipeState.wrap.classList.add('show-delete');
    }
    setSwipeState = null;
  };
  const cancelSwipe = () => {
    if (setSwipeState) {
      setSwipeState.row.style.transform = '';
      setSwipeState.wrap.classList.remove('swiping-delete');
    }
    setSwipeState = null;
  };
  list.addEventListener('pointerdown', event => startSwipe(event, event));
  list.addEventListener('pointermove', event => moveSwipe(event, event));
  list.addEventListener('pointerup', event => endSwipe(event));
  list.addEventListener('pointercancel', () => {
    cancelSwipe();
  });
  list.addEventListener('touchstart', event => {
    if (setSwipeState || !event.touches || event.touches.length !== 1) return;
    startSwipe(event, event.touches[0]);
  }, { passive: true });
  list.addEventListener('touchmove', event => {
    if (!setSwipeState || !event.touches || event.touches.length !== 1) return;
    moveSwipe(event, event.touches[0]);
  }, { passive: false });
  list.addEventListener('touchend', event => endSwipe(event.changedTouches && event.changedTouches[0]), { passive: true });
  list.addEventListener('touchcancel', cancelSwipe, { passive: true });
  document.addEventListener('click', event => {
    if (!event.target.closest('.set-wrap')) closeSetDeleteButtons();
  });
}
function updateExerciseCompare(exIdx) {
  const cards = document.querySelectorAll('#exercises-list .exercise');
  const card = cards[exIdx];
  if (!card || !currentWorkout || !currentWorkout.exercises[exIdx]) return;
  const ex = currentWorkout.exercises[exIdx];
  const last = getLastExerciseData(ex.name);
  let compare = card.querySelector('.compare-row');
  const html = last ? renderCompareRow(ex, last) : '';
  if (!html) {
    if (compare) compare.remove();
    return;
  }
  if (compare) compare.outerHTML = html;
  else {
    const note = card.querySelector('.exercise-note-section');
    if (note) note.insertAdjacentHTML('beforebegin', html);
  }
}
function updateExerciseNote(exIdx, value) {
  if (!currentWorkout || !currentWorkout.exercises[exIdx]) return;
  currentWorkout.exercises[exIdx].note = value;
  saveWorkoutDraft();
}
function updateWorkoutNote(value) {
  if (!currentWorkout) return;
  currentWorkout.note = value;
  saveWorkoutDraft();
}
function toggleSet(exIdx, sIdx) {
  const set = currentWorkout.exercises[exIdx].sets[sIdx];
  set.done = !set.done;
  if (set.done && getSettings().timer) startTimer(currentWorkout.exercises[exIdx].rest);
  saveWorkoutDraft();
  updateSetRowState(exIdx, sIdx);
  updateExerciseCompare(exIdx);
}
function addSet(exIdx) {
  const sets = currentWorkout.exercises[exIdx].sets;
  const last = sets.slice().reverse().find(s => s.weight || s.reps);
  sets.push({ weight: last ? last.weight : '', reps: last ? last.reps : '', rir: '', done: false, drop: { enabled: false, weight: '', reps: '' } });
  saveWorkoutDraft();
  renderExercises();
}
function moveExercise(exIdx, dir) {
  const ex = currentWorkout.exercises;
  const newIdx = exIdx + dir;
  if (newIdx < 0 || newIdx >= ex.length) return;
  [ex[exIdx], ex[newIdx]] = [ex[newIdx], ex[exIdx]];
  saveWorkoutDraft();
  renderExercises();
}

// ===== SWAP =====
function openSwap(exIdx) {
  activeSwapExIdx = exIdx;
  const ex = currentWorkout.exercises[exIdx];
  const program = getProgram();
  const dayExercises = program.days[currentDay].exercises;
  const original = dayExercises.find(e => exerciseNameMatchesDef(ex.name, e));
  const swaps = original ? original.swaps : [];
  const originalName = original ? original.name : ex.name;
  const body = document.getElementById('modal-body');
  document.getElementById('modal-title').textContent = 'Замена упражнения';
  body.innerHTML = `
    <div style="font-size: 13px; color: #888; margin-bottom: 10px;">Заменить "${escapeHTML(ex.name)}" на:</div>
    ${[originalName, ...swaps].map(name => {
      const encoded = encodeURIComponent(name).replace(/'/g, '%27');
      return `<button class="modal-option" onclick="applySwap(decodeURIComponent('${encoded}'))">${escapeHTML(name)}${name === ex.name ? ' ← текущее' : ''}</button>`;
    }).join('')}
  `;
  document.getElementById('modal').classList.add('active');
}
function applySwap(newName) {
  currentWorkout.exercises[activeSwapExIdx].name = newName;
  saveWorkoutDraft();
  closeModal();
  renderExercises();
}
function closeModal() { document.getElementById('modal').classList.remove('active'); activeSwapExIdx = null; }

// ===== TIMER =====
let audioCtx = null;
function canVibrate() {
  return typeof navigator !== 'undefined' && typeof navigator.vibrate === 'function';
}
async function primeTimerAudio() {
  try {
    if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
    if (audioCtx.state === 'suspended') await audioCtx.resume();
    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    osc.connect(gain);
    gain.connect(audioCtx.destination);
    gain.gain.setValueAtTime(0.0001, audioCtx.currentTime);
    osc.start();
    osc.stop(audioCtx.currentTime + 0.01);
    return true;
  } catch (e) {
    return false;
  }
}
async function playBeep(repeats = 2) {
  try {
    if (!await primeTimerAudio()) return false;
    const now = audioCtx.currentTime + 0.03;
    for (let i = 0; i < repeats; i++) {
      const t = now + i * 0.55;
      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();
      osc.connect(gain); gain.connect(audioCtx.destination);
      osc.frequency.value = i % 2 ? 1320 : 880;
      osc.type = 'sine';
      gain.gain.setValueAtTime(0.001, t);
      gain.gain.exponentialRampToValueAtTime(0.35, t + 0.02);
      gain.gain.exponentialRampToValueAtTime(0.001, t + 0.34);
      osc.start(t);
      osc.stop(t + 0.36);
    }
    return true;
  } catch (e) {}
  return false;
}
function vibrateSignal(pattern = [220, 90, 220, 90, 500]) {
  if (!canVibrate()) return false;
  if (navigator.userActivation && !navigator.userActivation.hasBeenActive) return false;
  try { return navigator.vibrate(pattern); } catch (e) { return false; }
}
function flashTimerSignal() {
  const bar = document.getElementById('timer-bar');
  if (bar) {
    bar.classList.remove('done-pulse');
    void bar.offsetWidth;
    bar.classList.add('active', 'done-pulse');
    setTimeout(() => bar.classList.remove('done-pulse'), 3200);
  }
  document.body.classList.remove('timer-flash');
  void document.body.offsetWidth;
  document.body.classList.add('timer-flash');
  setTimeout(() => document.body.classList.remove('timer-flash'), 2200);
  const oldTitle = document.title;
  document.title = 'Готово! Отдых закончен';
  setTimeout(() => { if (document.title === 'Готово! Отдых закончен') document.title = oldTitle; }, 4500);
}
function fireTimerSignal() {
  flashTimerSignal();
  vibrateSignal();
  playBeep(4);
}
function saveTimerState() {
  if (!timerEndAt) return;
  localStorage.setItem(TIMER_STATE_KEY, JSON.stringify({
    endAt: timerEndAt,
    duration: timerDurationSeconds,
    savedAt: Date.now()
  }));
}
function clearTimerState() {
  localStorage.removeItem(TIMER_STATE_KEY);
}
function clearTimerHandles() {
  if (timerInterval) clearInterval(timerInterval);
  timerInterval = null;
  if (timerAutocloseTimeout) clearTimeout(timerAutocloseTimeout);
  timerAutocloseTimeout = null;
}
function getTimerRemainingSeconds() {
  if (!timerEndAt) return Math.max(0, timerSeconds || 0);
  return Math.max(0, Math.ceil((timerEndAt - Date.now()) / 1000));
}
function finishTimer() {
  if (timerFinished) return;
  timerFinished = true;
  timerSeconds = 0;
  updateTimerDisplay();
  clearTimerHandles();
  clearTimerState();
  fireTimerSignal();
  if (getSettings().autoclose) {
    timerAutocloseTimeout = setTimeout(() => {
      const bar = document.getElementById('timer-bar');
      if (bar) bar.classList.remove('active');
      timerEndAt = null;
    }, 3200);
  }
}
function tickTimer() {
  if (!timerEndAt) return;
  timerSeconds = getTimerRemainingSeconds();
  updateTimerDisplay();
  if (timerSeconds <= 0) finishTimer();
}
function startTimer(s) {
  stopTimer();
  const seconds = Math.max(1, Math.round(Number(s) || 0));
  timerDurationSeconds = seconds;
  timerEndAt = Date.now() + seconds * 1000;
  timerFinished = false;
  timerSeconds = seconds;
  saveTimerState();
  primeTimerAudio();
  document.getElementById('timer-bar').classList.add('active');
  tickTimer();
  timerInterval = setInterval(tickTimer, 500);
}
function stopTimer(options = {}) {
  clearTimerHandles();
  timerEndAt = null;
  timerDurationSeconds = 0;
  timerFinished = false;
  timerSeconds = 0;
  if (options.clearState !== false) clearTimerState();
  const bar = document.getElementById('timer-bar');
  if (bar) bar.classList.remove('active', 'done-pulse');
}
function updateTimerDisplay() {
  const secondsLeft = Math.max(0, Math.round(timerSeconds || 0));
  const m = Math.floor(secondsLeft / 60).toString().padStart(2, '0');
  const s = (secondsLeft % 60).toString().padStart(2, '0');
  const display = document.getElementById('timer-display');
  if (!display) return;
  display.textContent = `${m}:${s}`;
  const bar = document.getElementById('timer-bar');
  if (!bar) return;
  if (secondsLeft <= 0) {
    bar.style.background = '#5fcf6f';
    display.textContent = 'Готов!';
  } else if (secondsLeft <= 10) {
    bar.style.background = '#c33';
  } else {
    bar.style.background = '#ff6b00';
  }
}
function restoreTimerState() {
  const stored = readJSON(TIMER_STATE_KEY, null);
  if (!stored || !stored.endAt) return;
  timerEndAt = Number(stored.endAt);
  timerDurationSeconds = Number(stored.duration) || 0;
  timerFinished = false;
  if (!Number.isFinite(timerEndAt)) {
    stopTimer();
    return;
  }
  const bar = document.getElementById('timer-bar');
  if (bar) bar.classList.add('active');
  tickTimer();
  if (timerEndAt) timerInterval = setInterval(tickTimer, 500);
}
document.addEventListener('visibilitychange', () => {
  if (!document.hidden) tickTimer();
});
window.addEventListener('focus', tickTimer);
window.addEventListener('pageshow', tickTimer);

// ===== FINISH =====
document.getElementById('finish-btn').addEventListener('click', () => {
  if (!currentWorkout) return;
  const hasData = currentWorkout.exercises.some(ex => ex.sets.some(setHasLiftData));
  if (!hasData) { alert('Заполни хотя бы один подход'); return; }
  const isEditingHistory = editingHistoryIndex != null;
  if (!confirm(isEditingHistory ? 'Сохранить изменения в истории?' : 'Завершить и сохранить?')) return;
  currentWorkout.note = document.getElementById('workout-note').value || '';
  const history = getHistory();
  if (isEditingHistory) {
    if (!history[editingHistoryIndex]) { alert('Не нашел эту запись в истории.'); return; }
    history[editingHistoryIndex] = currentWorkout;
  } else {
    history.push(currentWorkout);
  }
  saveHistory(history);
  clearWorkoutDraft();
  resetWorkoutScreen();
  renderDashboard();
  if (isEditingHistory) {
    switchToScreen('history');
    alert('Изменения сохранены ✓');
  } else {
    alert('Сохранено ✓');
  }
});

// ===== HISTORY =====
function renderHistory() {
  const list = document.getElementById('history-list');
  const rawHistory = getHistory();
  const history = rawHistory.map((workout, index) => ({ workout, index })).reverse();
  if (rawHistory.length === 0) {
    list.innerHTML = '<div class="empty-state">Пока нет записей.<br>Начни первую тренировку.</div>';
    return;
  }
  list.innerHTML = history.map(({ workout: w, index }) => {
    const d = new Date(w.date);
    const dateStr = d.toLocaleDateString('ru-RU', { day: 'numeric', month: 'long', weekday: 'short' });
    const weekTag = w.week ? `<span style="color:#888;"> · Нед. ${w.week}</span>` : '';
    const verTag = w.programVersion ? `<span style="color:#666;font-size:11px;"> · v${w.programVersion}</span>` : '';
    const filledExercises = w.exercises.filter(ex => ex.sets.some(setHasLiftData));
    const workoutTonnage = round1(filledExercises.reduce((total, ex) => (
      total + ex.sets.reduce((sum, set) => sum + getSetVolume(set), 0)
    ), 0));
    const tonnageTag = workoutTonnage ? ` · тоннаж ${formatKg(workoutTonnage)} кг` : '';
    const exercises = filledExercises.map(ex => {
      const setsText = ex.sets.filter(setHasLiftData).map(formatSetForHistory).join(' · ');
      const exNote = ex.note ? `<div class="history-note">📝 ${escapeHTML(ex.note)}</div>` : '';
      return `<div class="history-exercise"><div class="history-exercise-name">${escapeHTML(ex.name)}</div><div class="history-sets">${escapeHTML(setsText)}</div>${exNote}</div>`;
    }).join('');
    const title = shortWorkoutName(w.dayName);
    return `<details class="history-day">
      <summary>
        <div>
          <div class="history-summary-title">${escapeHTML(title)}</div>
          <div class="history-summary-sub">${dateStr}${weekTag}${verTag} · ${filledExercises.length} упр.${tonnageTag}</div>
        </div>
        <div class="history-summary-actions">
          <button class="history-edit-btn" onclick="event.preventDefault(); event.stopPropagation(); editHistoryWorkout(${index})">Редактировать</button>
          <div class="history-chevron">›</div>
        </div>
      </summary>
      <div class="history-details">
        ${exercises}${w.note ? `<div class="history-note">📝 ${escapeHTML(w.note)}</div>` : ''}
      </div>
    </details>`;
  }).join('');
}

// ===== PROGRESS =====
function initProgress() {
  const picker = document.getElementById('progress-day-picker');
  const days = getProgressDays();
  if (!picker) return;
  if (days.length === 0) {
    document.getElementById('progress-content').innerHTML = '<div class="empty-state">Нет тренировочных дней.</div>';
    picker.innerHTML = '<option>Нет данных</option>';
    return;
  }
  const stored = localStorage.getItem('progress_day');
  const selected = days.some(d => d.key === progressDay) ? progressDay :
    (days.some(d => d.key === stored) ? stored : days[0].key);
  progressDay = selected;
  picker.innerHTML = days.map(d =>
    `<option value="${escapeHTML(d.key)}" ${d.key === selected ? 'selected' : ''}>${escapeHTML(d.name)}</option>`
  ).join('');
  renderProgress();
}
function updateProgressDay(dayKey) {
  progressDay = dayKey;
  localStorage.setItem('progress_day', dayKey);
  renderProgress();
}
function getProgressDays() {
  const program = getProgram();
  const seen = new Set();
  const days = Object.keys(program.days || {}).map(key => {
    seen.add(key);
    return { key, name: program.days[key].name || key };
  });
  getHistory().forEach(w => {
    if (!w.day || seen.has(w.day)) return;
    seen.add(w.day);
    days.push({ key: w.day, name: w.dayName || w.day });
  });
  return days;
}
function getProgressExercisesForDay(dayKey) {
  const program = getProgram();
  const names = [];
  const seen = new Set();
  const day = program.days && program.days[dayKey];
  if (day && Array.isArray(day.exercises)) {
    day.exercises.forEach(ex => {
      const key = getExerciseIdentityKey(ex.name);
      if (!ex.name || seen.has(key)) return;
      seen.add(key);
      names.push({ name: ex.name, target: ex.target || '' });
    });
  }
  getHistory().forEach(w => {
    if (w.day !== dayKey || !Array.isArray(w.exercises)) return;
    w.exercises.forEach(ex => {
      const key = getExerciseIdentityKey(ex.name);
      if (!ex.name || seen.has(key) || !ex.sets.some(setHasLiftData)) return;
      seen.add(key);
      names.push({ name: ex.name, target: ex.target || '' });
    });
  });
  return names;
}
function getExerciseProgressPoints(exerciseName, dayKey) {
  const points = [];
  getHistory().forEach(w => {
    if (dayKey && w.day !== dayKey) return;
    const ex = (w.exercises || []).find(e => exerciseNameMatches(exerciseName, e.name));
    if (!ex) return;
    const valid = ex.sets.filter(s => normalizeNumber(s.weight) != null && normalizeNumber(s.reps) != null);
    if (valid.length === 0) return;
    const weights = valid.map(s => normalizeNumber(s.weight)).filter(x => x != null);
    if (weights.length === 0) return;
    const topWeight = Math.max(...weights);
    const tonnage = ex.sets.reduce((sum, s) => sum + getSetVolume(s), 0);
    const topSet = valid.reduce((best, s) => {
      const wv = normalizeNumber(s.weight), r = parseInt(s.reps);
      if (wv == null || isNaN(r) || r >= 37) return best;
      const e = wv * (36 / (37 - r));
      return (!best || e > best.e1rm) ? { e1rm: e } : best;
    }, null);
    points.push({ date: new Date(w.date), topWeight, tonnage, e1rm: topSet ? topSet.e1rm : topWeight });
  });
  return points.sort((a, b) => a.date - b.date);
}
function renderProgress() {
  const picker = document.getElementById('progress-day-picker');
  const dayKey = picker ? picker.value : progressDay;
  const day = getProgressDays().find(d => d.key === dayKey);
  const exercises = getProgressExercisesForDay(dayKey);
  const cards = exercises.map(ex => {
    const points = getExerciseProgressPoints(ex.name, dayKey);
    return renderProgressExerciseCard(ex, points);
  }).filter(Boolean);
  const content = document.getElementById('progress-content');
  if (!cards.length) {
    content.innerHTML = '<div class="empty-state">Нужно минимум 2 сохраненные тренировки одного упражнения в этом дне.</div>';
    return;
  }
  content.innerHTML = `
    <div class="progress-day-summary">${escapeHTML(day ? day.name : 'День')} · ${cards.length} граф.</div>
    ${cards.join('')}
  `;
}
function renderProgressExerciseCard(exercise, points) {
  if (points.length < 2) return '';
  const first = points[0], last = points[points.length - 1];
  const wDelta = (last.topWeight - first.topWeight).toFixed(1);
  const wPct = first.topWeight ? ((last.topWeight - first.topWeight) / first.topWeight * 100).toFixed(0) : 0;
  const tDelta = (last.tonnage - first.tonnage).toFixed(0);
  const tPct = first.tonnage ? ((last.tonnage - first.tonnage) / first.tonnage * 100).toFixed(0) : 0;

  return `
    <div class="chart-card progress-exercise-card">
      <div class="chart-title">${escapeHTML(exercise.name)}</div>
      <div class="chart-subtitle">${escapeHTML(exercise.target || `${points.length} трен.`)}</div>
      <div class="chart-stats">
        <div><span class="chart-stat-label">Сейчас:</span> <span class="chart-stat-value">${last.topWeight} кг</span></div>
        <div><span class="chart-stat-label">Δ:</span> <span class="chart-stat-value">${wDelta >= 0 ? '+' : ''}${wDelta} кг (${wPct >= 0 ? '+' : ''}${wPct}%)</span></div>
      </div>
      <div class="progress-mini-title"><span>Топ вес</span><span>${points.length} точ.</span></div>
      ${renderLineChart(points.map(p => ({ x: p.date, y: p.topWeight })), '#ff6b00')}
      <div class="progress-mini-title"><span>Тоннаж</span><span>за упражнение</span></div>
      <div class="chart-stats">
        <div><span class="chart-stat-label">Сейчас:</span> <span class="chart-stat-value">${last.tonnage} кг</span></div>
        <div><span class="chart-stat-label">Δ:</span> <span class="chart-stat-value">${tDelta >= 0 ? '+' : ''}${tDelta} кг (${tPct >= 0 ? '+' : ''}${tPct}%)</span></div>
      </div>
      ${renderLineChart(points.map(p => ({ x: p.date, y: p.tonnage })), '#4a9eff')}
    </div>
  `;
}

function forecastValue(points) {
  if (points.length < 2) return null;
  // Linear regression y = a + b*x
  const n = points.length;
  const sumX = points.reduce((s, p) => s + p.x, 0);
  const sumY = points.reduce((s, p) => s + p.y, 0);
  const sumXY = points.reduce((s, p) => s + p.x * p.y, 0);
  const sumXX = points.reduce((s, p) => s + p.x * p.x, 0);
  const denom = n * sumXX - sumX * sumX;
  if (denom === 0) return null;
  const b = (n * sumXY - sumX * sumY) / denom;
  const a = (sumY - b * sumX) / n;
  // Forecast at end of 12-week program
  const start = new Date(getStartDate());
  const endTarget = new Date(start);
  endTarget.setDate(endTarget.getDate() + 12 * 7);
  return a + b * endTarget.getTime();
}

function chartPointKey(point) {
  return `${point.x.getTime()}|${point.y}`;
}
function downsampleChartData(data, maxPoints = 80) {
  const sorted = data.slice().sort((a, b) => a.x - b.x);
  if (sorted.length <= maxPoints) return sorted;
  const keep = new Map();
  const add = (point) => keep.set(chartPointKey(point), point);
  const first = sorted[0];
  const last = sorted[sorted.length - 1];
  add(first);
  add(last);
  const bucketCount = Math.max(1, Math.floor((maxPoints - 2) / 2));
  const span = last.x.getTime() - first.x.getTime() || 1;
  const buckets = Array.from({ length: bucketCount }, () => []);
  sorted.slice(1, -1).forEach(point => {
    const raw = ((point.x.getTime() - first.x.getTime()) / span) * bucketCount;
    const index = Math.max(0, Math.min(bucketCount - 1, Math.floor(raw)));
    buckets[index].push(point);
  });
  buckets.forEach(bucket => {
    if (!bucket.length) return;
    let min = bucket[0], max = bucket[0];
    bucket.forEach(point => {
      if (point.y < min.y) min = point;
      if (point.y > max.y) max = point;
    });
    add(min);
    add(max);
  });
  return Array.from(keep.values()).sort((a, b) => a.x - b.x);
}
function renderLineChart(data, color, goal, options = {}) {
  const source = data
    .map(d => ({ x: d.x instanceof Date ? d.x : new Date(d.x), y: Number(d.y) }))
    .filter(d => !isNaN(d.x) && Number.isFinite(d.y))
    .sort((a, b) => a.x - b.x);
  if (source.length < 2) return '';
  const series = options.reducePoints ? downsampleChartData(source, options.maxPoints || 80) : source;
  const W = 320, H = 140, padL = 32, padR = 10, padT = 12, padB = 24;
  const xs = source.map(d => d.x.getTime());
  const ys = source.map(d => d.y);
  if (goal != null) ys.push(goal);
  const xMin = Math.min(...xs), xMax = Math.max(...xs);
  const yMin = Math.min(...ys), yMax = Math.max(...ys);
  const yPad = (yMax - yMin) * 0.15 || 1;
  const yLo = Math.max(0, yMin - yPad), yHi = yMax + yPad;
  const sx = x => padL + ((x - xMin) / (xMax - xMin || 1)) * (W - padL - padR);
  const sy = y => H - padB - ((y - yLo) / (yHi - yLo || 1)) * (H - padT - padB);
  const path = series.map((d, i) => `${i === 0 ? 'M' : 'L'} ${sx(d.x.getTime()).toFixed(1)} ${sy(d.y).toFixed(1)}`).join(' ');
  let dots = '';
  if (options.highlightExtremes) {
    const minPoint = source.reduce((best, point) => point.y < best.y ? point : best, source[0]);
    const maxPoint = source.reduce((best, point) => point.y > best.y ? point : best, source[0]);
    const lastPoint = source[source.length - 1];
    const highlights = new Map();
    [minPoint, maxPoint, lastPoint].forEach(point => highlights.set(chartPointKey(point), point));
    dots = Array.from(highlights.values()).map(point => {
      const isLast = chartPointKey(point) === chartPointKey(lastPoint);
      return `<circle cx="${sx(point.x.getTime()).toFixed(1)}" cy="${sy(point.y).toFixed(1)}" r="${isLast ? 4.3 : 3.8}" fill="${color}" stroke="#120d0a" stroke-width="2"/>`;
    }).join('');
  } else {
    dots = series.map(d => `<circle cx="${sx(d.x.getTime()).toFixed(1)}" cy="${sy(d.y).toFixed(1)}" r="3.5" fill="${color}"/>`).join('');
  }
  const yTicks = `<text x="4" y="${(sy(yHi) + 4).toFixed(1)}" fill="#666" font-size="10">${yHi.toFixed(0)}</text><text x="4" y="${sy(yLo).toFixed(1)}" fill="#666" font-size="10">${yLo.toFixed(0)}</text>`;
  const dateFmt = (d) => new Date(d).toLocaleDateString('ru-RU', { day: 'numeric', month: 'short' });
  const xTicks = `<text x="${padL}" y="${H - 6}" fill="#666" font-size="10">${dateFmt(xMin)}</text><text x="${W - padR}" y="${H - 6}" text-anchor="end" fill="#666" font-size="10">${dateFmt(xMax)}</text>`;
  const yMid = (yLo + yHi) / 2;
  const grid = `<line x1="${padL}" y1="${sy(yMid).toFixed(1)}" x2="${W - padR}" y2="${sy(yMid).toFixed(1)}" stroke="#222" stroke-dasharray="2,3"/>`;
  const goalLine = goal != null ? `<line x1="${padL}" y1="${sy(goal).toFixed(1)}" x2="${W - padR}" y2="${sy(goal).toFixed(1)}" stroke="#ffc107" stroke-width="1.5" stroke-dasharray="4,3"/><text x="${W - padR}" y="${(sy(goal) - 4).toFixed(1)}" text-anchor="end" fill="#ffc107" font-size="10">цель ${goal}</text>` : '';
  return `<svg class="chart" viewBox="0 0 ${W} ${H}" preserveAspectRatio="none">${grid}${goalLine}${yTicks}${xTicks}<path d="${path}" fill="none" stroke="${color}" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"/>${dots}</svg>`;
}

// ===== MEASURE =====
function saveMeasure() {
  const m = { date: new Date().toISOString() };
  MEASURE_FIELDS.forEach(f => { m[f.key] = numberFromInput('m-' + f.key); });
  if (!MEASURE_FIELDS.some(f => m[f.key] != null)) { alert('Заполни хотя бы одно поле'); return; }
  const measures = getMeasures();
  measures.push(m);
  saveMeasures(measures);
  MEASURE_FIELDS.forEach(f => {
    const el = document.getElementById('m-' + f.key);
    if (el) el.value = '';
  });
  renderMeasures();
  alert('Замер сохранён ✓');
}
function saveGoal() {
  const current = getGoals();
  const g = { _profile: current._profile || 'male' };
  GOAL_FIELDS.forEach(f => { g[f.key] = numberFromInput('g-' + f.key); });
  saveGoals(g);
  renderMeasures();
}
function getGoalProfile() {
  const profile = getGoals()._profile;
  return profile === 'female' ? 'female' : 'male';
}
function setGoalProfile(profile) {
  const goals = getGoals();
  goals._profile = profile === 'female' ? 'female' : 'male';
  saveGoals(goals);
  renderMeasures();
}
function getLatestMeasureWith(keys) {
  const measures = getMeasures().slice().reverse();
  return measures.find(m => keys.some(k => m[k] != null)) || null;
}
function getLatestMeasureValue(key) {
  const latest = getLatestMeasureWith([key]);
  return latest ? latest[key] : null;
}
function getIdealGoals() {
  const profile = getGoalProfile();
  const latest = getLatestMeasureWith(['wrist', 'height', 'waist', 'hips', 'shoulders']);
  if (!latest) return {};

  const ideal = {};
  const wrist = normalizeNumber(latest.wrist);
  const height = normalizeNumber(latest.height);
  const hips = normalizeNumber(latest.hips);

  if (profile === 'female') {
    const waistFromHeight = height ? height * 0.43 : null;
    const waistFromHips = hips ? hips * 0.72 : null;
    if (waistFromHeight && waistFromHips) ideal.waist = round1((waistFromHeight + waistFromHips) / 2);
    else if (waistFromHeight) ideal.waist = round1(waistFromHeight);
    else if (waistFromHips) ideal.waist = round1(waistFromHips);

    if (ideal.waist) {
      ideal.hips = round1(hips || ideal.waist / 0.72);
      ideal.shoulders = round1((hips || ideal.hips) * 0.95);
      ideal.chest = round1(ideal.waist * 1.18);
      ideal.thigh = round1((hips || ideal.hips) * 0.58);
    }
    if (wrist) {
      ideal.neck = round1(wrist * 2.05);
      ideal.biceps = round1(wrist * 1.85);
      ideal.forearm = round1(wrist * 1.55);
      ideal.calf = round1(wrist * 2.05);
    } else if (height) {
      ideal.neck = round1(height * 0.20);
      ideal.biceps = round1(height * 0.17);
      ideal.forearm = round1(height * 0.145);
      ideal.calf = round1(height * 0.205);
    }
  } else {
    if (wrist) {
      const chest = wrist * 6.5;
      ideal.chest = round1(chest);
      ideal.waist = round1(chest * 0.70);
      ideal.hips = round1(chest * 0.85);
      ideal.biceps = round1(chest * 0.36);
      ideal.forearm = round1(chest * 0.29);
      ideal.thigh = round1(chest * 0.53);
      ideal.neck = round1(chest * 0.37);
      ideal.calf = round1(chest * 0.34);
    } else if (height) {
      ideal.waist = round1(height * 0.45);
      ideal.chest = round1(ideal.waist / 0.70);
      ideal.hips = round1(ideal.chest * 0.85);
      ideal.biceps = round1(ideal.chest * 0.36);
      ideal.forearm = round1(ideal.chest * 0.29);
      ideal.thigh = round1(ideal.chest * 0.53);
      ideal.neck = round1(ideal.chest * 0.37);
      ideal.calf = round1(ideal.chest * 0.34);
    }

    const waistBase = ideal.waist || latest.waist;
    if (waistBase) ideal.shoulders = round1(waistBase * 1.618);
  }

  const currentWeight = getLatestMeasureValue('weight');
  if (currentWeight) ideal.weight = currentWeight;
  return ideal;
}
function renderIdealGoals() {
  const box = document.getElementById('ideal-goals');
  if (!box) return;
  const profile = getGoalProfile();
  const ideal = getIdealGoals();
  document.querySelectorAll('#goal-profile button').forEach(btn => {
    btn.classList.toggle('active', btn.dataset.profile === profile);
  });
  const note = document.getElementById('goal-formula-note');
  if (note) {
    note.textContent = profile === 'female'
      ? 'Женский расчет: талия от роста и/или бедер, бедра через WHR около 0.72, плечи через баланс к бедрам. Это эстетический ориентир, не медицинская норма.'
      : 'Мужской расчет: классические силовые пропорции от запястья, при отсутствии запястья - от роста и талии; плечи через соотношение к талии.';
  }

  GOAL_FIELDS.forEach(f => {
    const input = document.getElementById('g-' + f.key);
    if (input) input.placeholder = ideal[f.key] ? `~${ideal[f.key]}` : '';
  });

  const rows = GOAL_FIELDS
    .filter(f => ideal[f.key] != null && f.key !== 'weight')
    .map(f => `<div class="ideal-row"><span>${f.label}</span><b>${ideal[f.key]} ${f.unit}</b></div>`)
    .join('');

  const emptyText = profile === 'female'
    ? 'Заполни рост и/или таз/ягодицы. Запястье улучшит расчет шеи, рук и икр.'
    : 'Заполни запястье для классической формулы. Если запястья нет, расчет пойдет от роста и талии.';
  box.innerHTML = rows || `<div class="ideal-empty">${emptyText}</div>`;
}
function applyIdealGoals() {
  const ideal = getIdealGoals();
  if (!Object.keys(ideal).length) {
    alert('Добавь рост, запястье или таз/ягодицы, чтобы посчитать ориентиры.');
    return;
  }
  const goals = getGoals();
  GOAL_FIELDS.forEach(f => {
    if ((goals[f.key] == null || goals[f.key] === '') && ideal[f.key] != null) {
      goals[f.key] = ideal[f.key];
    }
  });
  saveGoals(goals);
  renderMeasures();
}
function renderMeasures() {
  const goals = getGoals();
  GOAL_FIELDS.forEach(f => {
    const el = document.getElementById('g-' + f.key);
    if (el) el.value = goals[f.key] || '';
  });
  renderIdealGoals();

  const container = document.getElementById('measure-charts');
  const measures = getMeasures();
  if (measures.length < 2) {
    container.innerHTML = '<div class="empty-state">Нужно минимум 2 замера для графика.</div>';
    return;
  }
  container.innerHTML = MEASURE_FIELDS.map(f => {
    const pts = measures.filter(m => m[f.key] != null).map(m => ({ x: new Date(m.date), y: m[f.key] }));
    if (pts.length < 2) return '';
    const first = pts[0].y, last = pts[pts.length-1].y;
    const delta = (last - first).toFixed(1);
    const goal = goals[f.key];
    const goalText = goal ? ` · цель ${goal} ${f.unit}` : '';
    return `<div class="chart-card">
      <div class="chart-title">${f.label}${goalText}</div>
      <div class="chart-stats">
        <div><span class="chart-stat-label">Сейчас:</span> <span class="chart-stat-value">${last} ${f.unit}</span></div>
        <div><span class="chart-stat-label">Δ:</span> <span class="chart-stat-value">${delta >= 0 ? '+' : ''}${delta} ${f.unit}</span></div>
      </div>
      ${renderLineChart(pts, f.color, goal)}
    </div>`;
  }).filter(x => x).join('') || '<div class="empty-state">Нужно минимум 2 замера одного параметра.</div>';
}
function renderHealth() {
  renderHealthImportStatus();
  renderHealthOverview();
  renderHealthSleep();
  renderHealthBody();
  renderHealthCharts();
  renderHealthWorkouts();
}
function getLatestHealthWith(keys) {
  return getHealthDaily().slice().reverse().find(row => keys.some(key => row[key] != null)) || null;
}
function getLatestHealthMetric(key) {
  return getLatestHealthDailyForKey(key);
}
function getLatestHealthDailyForKey(key) {
  return getHealthDaily().slice().reverse().find(row => row && row[key] != null) || null;
}
function isMeaningfulActivityDay(row) {
  if (!row) return false;
  return (row.steps || 0) >= 500 ||
    (row.distance_km || 0) >= 0.5 ||
    (row.exercise_minutes || 0) >= 5 ||
    (row.workout_minutes || 0) >= 5;
}
function getLatestActivityMetricRow(key) {
  const rows = getHealthDaily().slice().reverse();
  return rows.find(row => row && row[key] != null && isMeaningfulActivityDay(row)) ||
    rows.find(row => row && row[key] != null) ||
    null;
}
function formatHealthStatDate(row) {
  if (!row || !row.date) return '';
  return new Date(row.date).toLocaleDateString('ru-RU', { day: 'numeric', month: 'short' });
}
function formatHealthValue(row, key, unit = '', transform = null) {
  if (!row || row[key] == null) return '—';
  const value = transform ? transform(row[key]) : row[key];
  if (value == null || value === '') return '—';
  const text = typeof value === 'number'
    ? (Number.isInteger(value) ? String(value) : String(round1(value)).replace('.', ','))
    : String(value);
  return unit ? `${text} ${unit}` : text;
}
function isBurnedEnergyKey(key) {
  return ['active_energy_kcal', 'basal_energy_kcal', 'workout_energy_kcal', 'workout_basal_energy_kcal'].includes(key);
}
function renderHealthStat(row, key, label, unit = '', transform = null) {
  const valueClass = isBurnedEnergyKey(key) ? 'stat-val burned-calories' : 'stat-val';
  return `<div class="stat">
    <div class="${valueClass}">${formatHealthValue(row, key, unit, transform)}</div>
    <div class="stat-lbl">${label}</div>
    <div class="stat-date">${formatHealthStatDate(row)}</div>
  </div>`;
}
function renderHealthOverview() {
  const box = document.getElementById('health-overview');
  if (!box) return;
  const rows = getHealthDaily();
  if (!rows.length) {
    box.innerHTML = '<div class="empty-state">Импортируй Apple Health export.zip, чтобы увидеть данные часов.</div>';
    return;
  }
  const sleepRow = getLatestHealthMetric('sleep_asleep_min');
  const hrvRow = getLatestHealthMetric('hrv_sdnn_ms');
  const restingRow = getLatestHealthMetric('resting_hr_bpm');
  const vo2Row = getLatestHealthMetric('vo2max');
  const stepsRow = getLatestActivityMetricRow('steps');
  const distanceRow = getLatestActivityMetricRow('distance_km');
  const activeRow = getLatestActivityMetricRow('active_energy_kcal');
  const exerciseRow = getLatestActivityMetricRow('exercise_minutes');
  const weightRow = getLatestHealthMetric('body_mass_kg');
  const fatRow = getLatestHealthMetric('body_fat_pct');
  box.innerHTML = `
    <h2>Последнее</h2>
    <div class="stat-grid">
      ${renderHealthStat(sleepRow, 'sleep_asleep_min', 'Сон', 'ч', v => round1(v / 60))}
      ${renderHealthStat(hrvRow, 'hrv_sdnn_ms', 'HRV', 'мс')}
      ${renderHealthStat(restingRow, 'resting_hr_bpm', 'Пульс покоя')}
      ${renderHealthStat(vo2Row, 'vo2max', 'VO2 max')}
      ${renderHealthStat(stepsRow, 'steps', 'Шаги')}
      ${renderHealthStat(distanceRow, 'distance_km', 'Дистанция', 'км')}
      ${renderHealthStat(activeRow, 'active_energy_kcal', 'Активные', 'ккал')}
      ${renderHealthStat(exerciseRow, 'exercise_minutes', 'Exercise', 'мин')}
      ${renderHealthStat(weightRow, 'body_mass_kg', 'Вес Health', 'кг')}
      ${renderHealthStat(fatRow, 'body_fat_pct', 'Жир', '%')}
    </div>`;
}
function renderHealthSleep() {
  const box = document.getElementById('health-sleep');
  if (!box) return;
  const sleep = getLatestHealthWith(['sleep_asleep_min', 'sleep_in_bed_min', 'sleep_awake_min', 'sleep_rem_min', 'sleep_deep_min', 'sleep_core_min']);
  if (!sleep) {
    box.innerHTML = '<div class="empty-state">В Apple Health пока нет данных сна.</div>';
    return;
  }
  const date = new Date(sleep.date).toLocaleDateString('ru-RU', { day: 'numeric', month: 'long' });
  const dateKey = getDateKey(sleep.date);
  const inBedHours = sleep.sleep_in_bed_min ? round1(sleep.sleep_in_bed_min / 60) : '';
  const asleep = sleep.sleep_asleep_min || 0;
  const phases = [
    { key: 'sleep_deep_min', label: 'Глубокий', color: '#4a9eff' },
    { key: 'sleep_rem_min', label: 'REM', color: '#a68bff' },
    { key: 'sleep_core_min', label: 'Core', color: '#5fcf6f' },
    { key: 'sleep_awake_min', label: 'Пробуждения', color: '#ff7eb6' }
  ];
  const bar = phases.map(p => {
    const min = sleep[p.key] || 0;
    const width = asleep ? Math.max(3, min / Math.max(asleep + (sleep.sleep_awake_min || 0), 1) * 100) : 0;
    return min ? `<div title="${p.label}: ${round1(min / 60)} ч" style="width:${width}%;background:${p.color};height:10px;"></div>` : '';
  }).join('');
  const rows = [
    ['Всего сна', formatHealthValue(sleep, 'sleep_asleep_min', 'ч', v => round1(v / 60))],
    ['В кровати', formatHealthValue(sleep, 'sleep_in_bed_min', 'ч', v => round1(v / 60))],
    ['Эффективность', formatHealthValue(sleep, 'sleep_efficiency_pct', '%')],
    ['Пробуждения', `${formatHealthValue(sleep, 'sleep_awake_min', 'мин')} · ${sleep.sleep_awake_count || 0} раз`],
    ['REM', `${formatHealthValue(sleep, 'sleep_rem_min', 'ч', v => round1(v / 60))} · ${formatHealthValue(sleep, 'sleep_rem_pct', '%')}`],
    ['Глубокий', `${formatHealthValue(sleep, 'sleep_deep_min', 'ч', v => round1(v / 60))} · ${formatHealthValue(sleep, 'sleep_deep_pct', '%')}`],
    ['Core', `${formatHealthValue(sleep, 'sleep_core_min', 'ч', v => round1(v / 60))} · ${formatHealthValue(sleep, 'sleep_core_pct', '%')}`]
  ].map(([label, value]) => `<div class="ideal-row"><span>${label}</span><b>${value}</b></div>`).join('');
  box.innerHTML = `<div class="chart-card">
    <div class="chart-title">${date}</div>
    <div class="chart-subtitle">Последняя ночь с данными Apple Watch</div>
    <div style="display:flex;overflow:hidden;border-radius:999px;background:var(--surface-2);border:1px solid var(--line-soft);margin-bottom:12px;">${bar}</div>
    <div class="ideal-goals">${rows}</div>
    <div class="measure-grid" style="margin-top:12px;">
      <div class="measure-field"><label>В кровати, ч</label><input type="number" id="health-in-bed" inputmode="decimal" value="${escapeHTML(inBedHours)}"></div>
      <button class="btn-secondary" style="margin:18px 0 0;" onclick="saveHealthSleepInBed('${dateKey}')">Сохранить</button>
    </div>
  </div>`;
}
function renderHealthBody() {
  const box = document.getElementById('health-body');
  if (!box) return;
  const body = getLatestHealthWith(['body_mass_kg', 'body_fat_pct', 'lean_body_mass_kg', 'body_mass_index', 'waist_cm']);
  const waistMeasure = getLatestMeasureWith(['waist']);
  if (!body && !waistMeasure) {
    box.innerHTML = '<div class="empty-state">В Apple Health пока нет данных состава тела.</div>';
    return;
  }
  const bodyDate = body ? body.date : waistMeasure.date;
  const dateKey = getDateKey(bodyDate);
  const date = new Date(bodyDate).toLocaleDateString('ru-RU', { day: 'numeric', month: 'long' });
  const waistFromMeasure = body && body.waist_cm != null ? null : (waistMeasure && waistMeasure.waist != null ? waistMeasure.waist : null);
  const waistRow = body && body.waist_cm != null ? body : (waistFromMeasure != null ? { date: waistMeasure.date, waist_cm: waistFromMeasure } : body);
  const waistSource = body && body.waist_cm != null
    ? (body.health_sources && body.health_sources.waist_cm ? ` · ${escapeHTML(body.health_sources.waist_cm)}` : '')
    : (waistFromMeasure != null ? ' · замеры' : '');
  const sourceFor = key => body && body.health_sources && body.health_sources[key] ? ` · ${escapeHTML(body.health_sources[key])}` : '';
  const leanCalculated = body && body.lean_body_mass_kg == null && body.body_mass_kg != null && body.body_fat_pct != null
    ? round1(body.body_mass_kg * (1 - body.body_fat_pct / 100))
    : null;
  const leanRow = body && body.lean_body_mass_kg != null ? body : (leanCalculated != null ? { date: body.date, lean_body_mass_kg: leanCalculated } : body);
  const leanSource = body && body.lean_body_mass_kg != null ? sourceFor('lean_body_mass_kg') : (leanCalculated != null ? ' · расчет' : '');
  const leanValue = leanRow && leanRow.lean_body_mass_kg != null ? leanRow.lean_body_mass_kg : '';
  const waistValue = waistRow && waistRow.waist_cm != null ? waistRow.waist_cm : '';
  const rows = [
    ['Вес', `${formatHealthValue(body, 'body_mass_kg', 'кг')}${sourceFor('body_mass_kg')}`],
    ['Жир', `${formatHealthValue(body, 'body_fat_pct', '%')}${sourceFor('body_fat_pct')}`],
    ['Безжировая масса', `${formatHealthValue(leanRow, 'lean_body_mass_kg', 'кг')}${leanSource}`],
    ['BMI', `${formatHealthValue(body, 'body_mass_index')}${sourceFor('body_mass_index')}`],
    ['Талия', `${formatHealthValue(waistRow, 'waist_cm', 'см')}${waistSource}`]
  ].map(([label, value]) => `<div class="ideal-row"><span>${label}</span><b>${value}</b></div>`).join('');
  box.innerHTML = `<div class="chart-card">
    <div class="chart-title">${date}</div>
    <div class="chart-subtitle">Последняя запись состава тела из Apple Health</div>
    <div class="ideal-goals">${rows}</div>
    <div class="measure-grid" style="margin-top:12px;">
      <div class="measure-field"><label>Безжировая, кг</label><input type="number" id="health-lean-mass" inputmode="decimal" value="${escapeHTML(leanValue)}"></div>
      <div class="measure-field"><label>Талия, см</label><input type="number" id="health-waist" inputmode="decimal" value="${escapeHTML(waistValue)}"></div>
    </div>
    <button class="btn-secondary" onclick="saveHealthBodyManual('${dateKey}')">Сохранить состав тела</button>
  </div>`;
}
function recalcHealthDerived(row) {
  if (!row) return;
  if (row.sleep_asleep_min && row.sleep_in_bed_min) row.sleep_efficiency_pct = round1(row.sleep_asleep_min / row.sleep_in_bed_min * 100);
  if (row.sleep_asleep_min) {
    if (row.sleep_rem_min) row.sleep_rem_pct = round1(row.sleep_rem_min / row.sleep_asleep_min * 100);
    if (row.sleep_deep_min) row.sleep_deep_pct = round1(row.sleep_deep_min / row.sleep_asleep_min * 100);
    if (row.sleep_core_min) row.sleep_core_pct = round1(row.sleep_core_min / row.sleep_asleep_min * 100);
  }
}
function upsertHealthDailyValues(dateKey, values, source = 'ручной ввод') {
  if (!dateKey || !isHealthDateAllowed(dateKey)) {
    alert(`Дата должна быть не раньше ${HEALTH_IMPORT_START_DATE}.`);
    return false;
  }
  const rows = getHealthDaily();
  let row = rows.find(item => item.date === dateKey);
  if (!row) {
    row = { date: dateKey };
    rows.push(row);
  }
  Object.entries(values).forEach(([key, value]) => {
    if (value == null || !Number.isFinite(value)) return;
    row[key] = round1(value);
    if (!row.health_sources) row.health_sources = {};
    row.health_sources[key] = source;
  });
  recalcHealthDerived(row);
  saveHealthDaily(rows);
  renderDashboard();
  renderHealth();
  return true;
}
function saveHealthSleepInBed(dateKey) {
  const hours = numberFromInput('health-in-bed');
  if (hours == null || hours <= 0) {
    alert('Введи время в кровати в часах.');
    return;
  }
  if (upsertHealthDailyValues(dateKey, { sleep_in_bed_min: hours * 60 })) alert('Сон обновлен ✓');
}
function saveHealthBodyManual(dateKey) {
  const lean = numberFromInput('health-lean-mass');
  const waist = numberFromInput('health-waist');
  const values = {};
  if (lean != null) values.lean_body_mass_kg = lean;
  if (waist != null) values.waist_cm = waist;
  if (!Object.keys(values).length) {
    alert('Введи безжировую массу или талию.');
    return;
  }
  if (upsertHealthDailyValues(dateKey, values)) alert('Состав тела обновлен ✓');
}
function getHealthChartRange() {
  const range = localStorage.getItem('health_chart_range');
  return ['week', 'month', 'all'].includes(range) ? range : 'month';
}
function setHealthChartRange(range) {
  if (!['week', 'month', 'all'].includes(range)) return;
  localStorage.setItem('health_chart_range', range);
  renderHealthCharts();
}
function renderHealthRangeTabs(active) {
  const tabs = [
    ['week', '1 неделя'],
    ['month', '1 месяц'],
    ['all', 'все время']
  ];
  return `<div class="health-range">${tabs.map(([key, label]) => (
    `<button type="button" class="${active === key ? 'active' : ''}" onclick="setHealthChartRange('${key}')">${label}</button>`
  )).join('')}</div>`;
}
function filterHealthPointsByRange(points, range) {
  const sorted = points.slice().sort((a, b) => a.x - b.x);
  if (range === 'all' || sorted.length < 2) return sorted;
  const days = range === 'week' ? 7 : 31;
  const last = sorted[sorted.length - 1].x.getTime();
  const start = last - (days - 1) * 86400000;
  return sorted.filter(point => point.x.getTime() >= start);
}
function renderHealthCharts() {
  const container = document.getElementById('health-charts');
  if (!container) return;
  const rows = getHealthDaily().slice().sort((a, b) => new Date(a.date) - new Date(b.date));
  if (rows.length < 2) {
    container.innerHTML = '<div class="empty-state">Импортируй Apple Health export.zip, чтобы появились графики часов.</div>';
    return;
  }
  const range = getHealthChartRange();
  const fields = [
    { key: 'sleep_asleep_min', label: 'Сон', desc: 'Сколько часов реально спал за ночь.', unit: 'ч', color: '#8f8f8f', map: v => round1(v / 60) },
    { key: 'sleep_in_bed_min', label: 'В кровати', desc: 'Время от отбоя до подъема, включая пробуждения.', unit: 'ч', color: '#c878ff', map: v => round1(v / 60) },
    { key: 'sleep_awake_min', label: 'Пробуждения', desc: 'Минуты бодрствования внутри сна.', unit: 'мин', color: '#ff7eb6' },
    { key: 'sleep_efficiency_pct', label: 'Эффективность сна', desc: 'Доля сна от общего времени в кровати.', unit: '%', color: '#5fcf6f' },
    { key: 'sleep_deep_min', label: 'Глубокий сон', desc: 'Фаза, которую обычно связывают с физическим восстановлением.', unit: 'ч', color: '#4a9eff', map: v => round1(v / 60) },
    { key: 'sleep_rem_min', label: 'REM сон', desc: 'Фаза, важная для нервной системы, памяти и эмоций.', unit: 'ч', color: '#a68bff', map: v => round1(v / 60) },
    { key: 'sleep_core_min', label: 'Core сон', desc: 'Базовая фаза сна, которая обычно занимает большую часть ночи.', unit: 'ч', color: '#9bdc65', map: v => round1(v / 60) },
    { key: 'hrv_sdnn_ms', label: 'HRV SDNN', desc: 'Маркер восстановления нервной системы: смотреть лучше в динамике.', unit: 'мс', color: '#5fcf6f' },
    { key: 'resting_hr_bpm', label: 'Пульс покоя', desc: 'Низкий относительно твоей нормы часто говорит о лучшем восстановлении.', unit: 'уд/мин', color: '#ff7eb6' },
    { key: 'avg_hr_bpm', label: 'Средний пульс', desc: 'Общий дневной фон нагрузки и восстановления.', unit: 'уд/мин', color: '#ff6b00' },
    { key: 'walking_hr_bpm', label: 'Walking HR', desc: 'Пульс при ходьбе: полезен как спокойный индикатор формы.', unit: 'уд/мин', color: '#ffc857' },
    { key: 'vo2max', label: 'VO2 max', desc: 'Оценка кардио-формы Apple Health.', unit: '', color: '#9bdc65' },
    { key: 'respiratory_rate_bpm', label: 'Дыхание', desc: 'Частота дыхания во сне или за день, если часы ее записали.', unit: '/мин', color: '#a68bff' },
    { key: 'oxygen_saturation_pct', label: 'SpO2', desc: 'Насыщение крови кислородом, полезно смотреть на редкие провалы.', unit: '%', color: '#4a9eff' },
    { key: 'steps', label: 'Шаги', desc: 'Общий объем бытовой активности.', unit: '', color: '#4a9eff' },
    { key: 'distance_km', label: 'Дистанция', desc: 'Сколько километров набрал за день.', unit: 'км', color: '#5fcf6f' },
    { key: 'active_energy_kcal', label: 'Активные калории', desc: 'Энергия активного движения без базового обмена.', unit: 'ккал', color: '#ff9f43' },
    { key: 'basal_energy_kcal', label: 'Базовые калории', desc: 'Оценка энергии, которую тело тратит в покое.', unit: 'ккал', color: '#c878ff' },
    { key: 'exercise_minutes', label: 'Exercise time', desc: 'Минуты активности, которые Apple засчитала как упражнение.', unit: 'мин', color: '#ff7eb6' },
    { key: 'stand_minutes', label: 'Stand time', desc: 'Минуты стояния и легкой активности по данным Apple.', unit: 'мин', color: '#8f8f8f' },
    { key: 'workout_minutes', label: 'Тренировки', desc: 'Длительность тренировок, записанных часами.', unit: 'мин', color: '#ff6b00' },
    { key: 'body_mass_kg', label: 'Вес из Health', desc: 'Вес из Apple Health или подключенных весов.', unit: 'кг', color: '#ffc857' },
    { key: 'body_fat_pct', label: 'Жир из Health', desc: 'Процент жира, если его передали умные весы.', unit: '%', color: '#ff7eb6' },
    { key: 'lean_body_mass_kg', label: 'Безжировая масса', desc: 'Масса тела без жира по данным весов/Health.', unit: 'кг', color: '#5fcf6f' },
    { key: 'body_mass_index', label: 'BMI', desc: 'Индекс массы тела из Apple Health.', unit: '', color: '#a68bff' }
  ];
  const cards = fields.map(f => {
    const allPts = rows
      .filter(r => r[f.key] != null)
      .map(r => ({ x: new Date(r.date), y: f.map ? f.map(r[f.key]) : r[f.key] }));
    const pts = filterHealthPointsByRange(allPts, range);
    if (pts.length < 2) return '';
    const first = pts[0].y, last = pts[pts.length - 1].y;
    const delta = round1(last - first);
    const unit = f.unit ? ` ${f.unit}` : '';
    const valueClass = isBurnedEnergyKey(f.key) ? 'chart-stat-value burned-calories' : 'chart-stat-value';
    return `<div class="chart-card">
      <div class="chart-title">${f.label}</div>
      <div class="chart-subtitle">${f.desc}</div>
      <div class="chart-stats">
        <div><span class="chart-stat-label">Последнее:</span> <span class="${valueClass}">${last}${unit}</span></div>
        <div><span class="chart-stat-label">Δ:</span> <span class="${valueClass}">${delta >= 0 ? '+' : ''}${delta}${unit}</span></div>
      </div>
      ${renderLineChart(pts, f.color, null, { reducePoints: true, maxPoints: 72, highlightExtremes: true })}
    </div>`;
  }).filter(Boolean).join('') || '<div class="empty-state">В Apple Health пока мало точек для графиков восстановления.</div>';
  container.innerHTML = `${renderHealthRangeTabs(range)}${cards}`;
}
function renderHealthWorkouts() {
  const container = document.getElementById('health-workouts');
  if (!container) return;
  const rows = getHealthDaily()
    .filter(r => r.workouts_count || r.workout_minutes)
    .sort((a, b) => new Date(b.date) - new Date(a.date));
  if (!rows.length) {
    container.innerHTML = '<div class="empty-state">В экспорте Apple Health нет тренировок Apple Watch.</div>';
    return;
  }
  const groups = new Map();
  rows.forEach(row => {
    const key = String(row.date).slice(0, 7);
    if (!groups.has(key)) groups.set(key, []);
    groups.get(key).push(row);
  });
  container.innerHTML = Array.from(groups.entries()).map(([monthKey, monthRows]) => {
    const monthDate = new Date(`${monthKey}-01T12:00:00`);
    const monthLabel = monthDate.toLocaleDateString('ru-RU', { month: 'long', year: 'numeric' });
    const totalCount = monthRows.reduce((sum, row) => sum + (row.workouts_count || 0), 0);
    const totalMinutes = round1(monthRows.reduce((sum, row) => sum + (row.workout_minutes || 0), 0));
    const totalEnergy = round1(monthRows.reduce((sum, row) => sum + (row.workout_energy_kcal || 0), 0));
    const energyText = totalEnergy ? ` · <span class="burned-calories">сожжено ${totalEnergy} ккал</span>` : '';
    const workouts = monthRows.map(row => {
      const date = new Date(row.date).toLocaleDateString('ru-RU', { day: 'numeric', month: 'long', weekday: 'short' });
      const types = row.workout_types
        ? Object.entries(row.workout_types)
          .sort((a, b) => b[1] - a[1])
          .map(([name, count]) => `${name}${count > 1 ? ` ×${count}` : ''}`)
          .join(', ')
        : '';
      return `<details class="health-workout-item">
        <summary>
          <div>
            <div class="history-summary-title">${date}</div>
            <div class="history-summary-sub">${row.workouts_count || 0} трен. · ${row.workout_minutes || 0} мин.${row.workout_energy_kcal ? ` · <span class="burned-calories">${row.workout_energy_kcal} ккал</span>` : ''}</div>
          </div>
          <div class="health-workout-chevron">›</div>
        </summary>
        <div class="health-workout-detail">
          <div class="chart-stats">
            <div><span class="chart-stat-label">Тренировки:</span> <span class="chart-stat-value">${row.workouts_count || 0}</span></div>
            <div><span class="chart-stat-label">Минуты:</span> <span class="chart-stat-value">${row.workout_minutes || 0}</span></div>
            ${row.workout_energy_kcal ? `<div><span class="chart-stat-label">Ккал:</span> <span class="chart-stat-value burned-calories">${row.workout_energy_kcal}</span></div>` : ''}
          </div>
          ${types ? `<div class="chart-subtitle">${escapeHTML(types)}</div>` : '<div class="chart-subtitle">Типы тренировок не указаны в экспорте.</div>'}
        </div>
      </details>`;
    }).join('');
    return `<details class="history-day health-workout-month">
      <summary>
        <div>
          <div class="history-summary-title">${monthLabel}</div>
          <div class="history-summary-sub">${totalCount} трен. · ${totalMinutes} мин.${energyText}</div>
        </div>
        <div class="history-chevron">›</div>
      </summary>
      <div class="history-details">
        ${workouts}
      </div>
    </details>`;
  }).join('');
}

// ===== FOOD =====
function formatFoodValue(value, unit = '') {
  if (value == null || !Number.isFinite(Number(value))) return '—';
  const rounded = roundFoodValue(Number(value));
  const text = Number.isInteger(rounded) ? String(rounded) : String(rounded).replace('.', ',');
  return unit ? `${text} ${unit}` : text;
}
function renderMacroBar(day) {
  const proteinKcal = (day.protein_g || 0) * 4;
  const carbsKcal = (day.carbs_g || 0) * 4;
  const fatKcal = (day.fat_g || 0) * 9;
  const total = proteinKcal + carbsKcal + fatKcal;
  if (!total) return '';
  const pct = value => Math.max(2, value / total * 100);
  return `<div class="macro-bar">
    <span class="macro-protein" style="width:${pct(proteinKcal)}%"></span>
    <span class="macro-carbs" style="width:${pct(carbsKcal)}%"></span>
    <span class="macro-fat" style="width:${pct(fatKcal)}%"></span>
  </div>`;
}
const FOOD_MICRO_LABELS = [
  { key: 'fiber_g', label: 'клетч.', unit: 'г' },
  { key: 'sugar_g', label: 'сахар', unit: 'г' },
  { key: 'sodium_mg', label: 'натрий', unit: 'мг' },
  { key: 'potassium_mg', label: 'калий', unit: 'мг' },
  { key: 'calcium_mg', label: 'кальций', unit: 'мг' },
  { key: 'iron_mg', label: 'железо', unit: 'мг' },
  { key: 'magnesium_mg', label: 'магний', unit: 'мг' },
  { key: 'cholesterol_mg', label: 'холест.', unit: 'мг' },
  { key: 'vitamin_c_mg', label: 'вит. C', unit: 'мг' },
  { key: 'vitamin_d_mcg', label: 'вит. D', unit: 'мкг' },
  { key: 'vitamin_b12_mcg', label: 'B12', unit: 'мкг' },
  { key: 'zinc_mg', label: 'цинк', unit: 'мг' }
];
function getFoodMicroParts(row, limit = 6) {
  const parts = FOOD_MICRO_LABELS
    .filter(item => Number(row[item.key]) > 0)
    .map(item => `${item.label} ${formatFoodValue(row[item.key], item.unit)}`);
  return parts.slice(0, limit);
}
function renderFoodMicros(row, limit = 6) {
  const parts = getFoodMicroParts(row, limit);
  return parts.length ? `<div class="food-item-micros">${parts.join(' · ')}</div>` : '';
}
function renderFood() {
  renderFoodOverview();
  renderFoodDays();
}
function renderFoodOverview() {
  const box = document.getElementById('food-overview');
  if (!box) return;
  const rows = getFoodDaily();
  if (!rows.length) {
    box.innerHTML = '<div class="empty-state">Пока нет питания. Импортируй Apple Health export.zip, где Yazio пишет нутриенты и продукты.</div>';
    return;
  }
  const latest = rows[rows.length - 1];
  const date = new Date(latest.date).toLocaleDateString('ru-RU', { day: 'numeric', month: 'long' });
  box.innerHTML = `<div class="chart-card">
    <div class="chart-title">${date}</div>
    <div class="chart-subtitle">Последний день питания из Yazio · ${latest.food_count || 0} продуктов</div>
    <div class="stat-grid">
      <div class="stat"><div class="stat-val">${formatFoodValue(latest.calories_kcal, 'ккал')}</div><div class="stat-lbl">Калории</div></div>
      <div class="stat"><div class="stat-val">${formatFoodValue(latest.protein_g, 'г')}</div><div class="stat-lbl">Белки</div></div>
      <div class="stat"><div class="stat-val">${formatFoodValue(latest.carbs_g, 'г')}</div><div class="stat-lbl">Угли</div></div>
      <div class="stat"><div class="stat-val">${formatFoodValue(latest.fat_g, 'г')}</div><div class="stat-lbl">Жиры</div></div>
    </div>
    ${renderMacroBar(latest)}
    <div class="chart-stats">
      <div><span class="chart-stat-label">Сахар:</span> <span class="chart-stat-value">${formatFoodValue(latest.sugar_g, 'г')}</span></div>
      <div><span class="chart-stat-label">Клетчатка:</span> <span class="chart-stat-value">${formatFoodValue(latest.fiber_g, 'г')}</span></div>
      <div><span class="chart-stat-label">Вода:</span> <span class="chart-stat-value">${formatFoodValue(latest.water_ml, 'мл')}</span></div>
      <div><span class="chart-stat-label">Натрий:</span> <span class="chart-stat-value">${formatFoodValue(latest.sodium_mg, 'мг')}</span></div>
      <div><span class="chart-stat-label">Калий:</span> <span class="chart-stat-value">${formatFoodValue(latest.potassium_mg, 'мг')}</span></div>
    </div>
  </div>`;
}
function renderFoodItem(item) {
  return `<div class="food-item">
    <div class="food-item-name">${escapeHTML(item.name || 'Без названия')}</div>
    <div class="food-item-kcal">${formatFoodValue(item.calories_kcal, 'ккал')}</div>
    <div class="food-item-macros">Б ${formatFoodValue(item.protein_g, 'г')} · Ж ${formatFoodValue(item.fat_g, 'г')} · У ${formatFoodValue(item.carbs_g, 'г')}${item.sugar_g ? ` · сахар ${formatFoodValue(item.sugar_g, 'г')}` : ''}</div>
    ${renderFoodMicros(item, 5)}
  </div>`;
}
function renderFoodDays() {
  const box = document.getElementById('food-days');
  if (!box) return;
  const rows = getFoodDaily().slice().reverse();
  if (!rows.length) {
    box.innerHTML = '<div class="empty-state">Дней питания пока нет.</div>';
    return;
  }
  box.innerHTML = rows.map(row => {
    const date = new Date(row.date).toLocaleDateString('ru-RU', { day: 'numeric', month: 'long', weekday: 'short' });
    const items = (row.items || []).slice().sort((a, b) => (b.calories_kcal || 0) - (a.calories_kcal || 0));
    return `<details class="history-day">
      <summary>
        <div>
          <div class="history-summary-title">${date}</div>
          <div class="history-summary-sub">${formatFoodValue(row.calories_kcal, 'ккал')} · Б ${formatFoodValue(row.protein_g, 'г')} · Ж ${formatFoodValue(row.fat_g, 'г')} · У ${formatFoodValue(row.carbs_g, 'г')} · ${row.food_count || items.length} прод.</div>
        </div>
        <div class="history-chevron">›</div>
      </summary>
      <div class="history-details">
        ${renderMacroBar(row)}
        <div class="chart-stats">
          <div><span class="chart-stat-label">Сахар:</span> <span class="chart-stat-value">${formatFoodValue(row.sugar_g, 'г')}</span></div>
          <div><span class="chart-stat-label">Клетчатка:</span> <span class="chart-stat-value">${formatFoodValue(row.fiber_g, 'г')}</span></div>
          <div><span class="chart-stat-label">Вода:</span> <span class="chart-stat-value">${formatFoodValue(row.water_ml, 'мл')}</span></div>
          <div><span class="chart-stat-label">Натрий:</span> <span class="chart-stat-value">${formatFoodValue(row.sodium_mg, 'мг')}</span></div>
          <div><span class="chart-stat-label">Калий:</span> <span class="chart-stat-value">${formatFoodValue(row.potassium_mg, 'мг')}</span></div>
        </div>
        <div class="food-items">${items.map(renderFoodItem).join('')}</div>
      </div>
    </details>`;
  }).join('');
}

// ===== APPLE HEALTH IMPORT =====
const HEALTH_TYPES = {
  heartRate: 'HKQuantityTypeIdentifierHeartRate',
  restingHR: 'HKQuantityTypeIdentifierRestingHeartRate',
  walkingHR: 'HKQuantityTypeIdentifierWalkingHeartRateAverage',
  hrv: 'HKQuantityTypeIdentifierHeartRateVariabilitySDNN',
  vo2max: 'HKQuantityTypeIdentifierVO2Max',
  respiratoryRate: 'HKQuantityTypeIdentifierRespiratoryRate',
  oxygenSaturation: 'HKQuantityTypeIdentifierOxygenSaturation',
  steps: 'HKQuantityTypeIdentifierStepCount',
  distanceWalkingRunning: 'HKQuantityTypeIdentifierDistanceWalkingRunning',
  activeEnergy: 'HKQuantityTypeIdentifierActiveEnergyBurned',
  basalEnergy: 'HKQuantityTypeIdentifierBasalEnergyBurned',
  exerciseTime: 'HKQuantityTypeIdentifierAppleExerciseTime',
  standTime: 'HKQuantityTypeIdentifierAppleStandTime',
  flightsClimbed: 'HKQuantityTypeIdentifierFlightsClimbed',
  bodyMass: 'HKQuantityTypeIdentifierBodyMass',
  bodyFat: 'HKQuantityTypeIdentifierBodyFatPercentage',
  leanBodyMass: 'HKQuantityTypeIdentifierLeanBodyMass',
  bodyMassIndex: 'HKQuantityTypeIdentifierBodyMassIndex',
  waistCircumference: 'HKQuantityTypeIdentifierWaistCircumference',
  sleep: 'HKCategoryTypeIdentifierSleepAnalysis'
};
const FOOD_TYPES = {
  dietaryEnergy: { type: 'HKQuantityTypeIdentifierDietaryEnergyConsumed', key: 'calories_kcal' },
  protein: { type: 'HKQuantityTypeIdentifierDietaryProtein', key: 'protein_g' },
  carbs: { type: 'HKQuantityTypeIdentifierDietaryCarbohydrates', key: 'carbs_g' },
  fat: { type: 'HKQuantityTypeIdentifierDietaryFatTotal', key: 'fat_g' },
  saturatedFat: { type: 'HKQuantityTypeIdentifierDietaryFatSaturated', key: 'saturated_fat_g' },
  monounsaturatedFat: { type: 'HKQuantityTypeIdentifierDietaryFatMonounsaturated', key: 'monounsaturated_fat_g' },
  polyunsaturatedFat: { type: 'HKQuantityTypeIdentifierDietaryFatPolyunsaturated', key: 'polyunsaturated_fat_g' },
  sugar: { type: 'HKQuantityTypeIdentifierDietarySugar', key: 'sugar_g' },
  fiber: { type: 'HKQuantityTypeIdentifierDietaryFiber', key: 'fiber_g' },
  water: { type: 'HKQuantityTypeIdentifierDietaryWater', key: 'water_ml' },
  sodium: { type: 'HKQuantityTypeIdentifierDietarySodium', key: 'sodium_mg' },
  cholesterol: { type: 'HKQuantityTypeIdentifierDietaryCholesterol', key: 'cholesterol_mg' },
  calcium: { type: 'HKQuantityTypeIdentifierDietaryCalcium', key: 'calcium_mg' },
  iron: { type: 'HKQuantityTypeIdentifierDietaryIron', key: 'iron_mg' },
  magnesium: { type: 'HKQuantityTypeIdentifierDietaryMagnesium', key: 'magnesium_mg' },
  phosphorus: { type: 'HKQuantityTypeIdentifierDietaryPhosphorus', key: 'phosphorus_mg' },
  potassium: { type: 'HKQuantityTypeIdentifierDietaryPotassium', key: 'potassium_mg' },
  zinc: { type: 'HKQuantityTypeIdentifierDietaryZinc', key: 'zinc_mg' },
  copper: { type: 'HKQuantityTypeIdentifierDietaryCopper', key: 'copper_mg' },
  manganese: { type: 'HKQuantityTypeIdentifierDietaryManganese', key: 'manganese_mg' },
  selenium: { type: 'HKQuantityTypeIdentifierDietarySelenium', key: 'selenium_mcg' },
  vitaminA: { type: 'HKQuantityTypeIdentifierDietaryVitaminA', key: 'vitamin_a_mcg' },
  vitaminB6: { type: 'HKQuantityTypeIdentifierDietaryVitaminB6', key: 'vitamin_b6_mg' },
  vitaminB12: { type: 'HKQuantityTypeIdentifierDietaryVitaminB12', key: 'vitamin_b12_mcg' },
  vitaminC: { type: 'HKQuantityTypeIdentifierDietaryVitaminC', key: 'vitamin_c_mg' },
  vitaminD: { type: 'HKQuantityTypeIdentifierDietaryVitaminD', key: 'vitamin_d_mcg' },
  vitaminE: { type: 'HKQuantityTypeIdentifierDietaryVitaminE', key: 'vitamin_e_mg' },
  vitaminK: { type: 'HKQuantityTypeIdentifierDietaryVitaminK', key: 'vitamin_k_mcg' },
  thiamin: { type: 'HKQuantityTypeIdentifierDietaryThiamin', key: 'thiamin_mg' },
  riboflavin: { type: 'HKQuantityTypeIdentifierDietaryRiboflavin', key: 'riboflavin_mg' },
  niacin: { type: 'HKQuantityTypeIdentifierDietaryNiacin', key: 'niacin_mg' },
  folate: { type: 'HKQuantityTypeIdentifierDietaryFolate', key: 'folate_mcg' },
  pantothenicAcid: { type: 'HKQuantityTypeIdentifierDietaryPantothenicAcid', key: 'pantothenic_acid_mg' }
};
const FOOD_TYPE_BY_HEALTH_TYPE = Object.fromEntries(Object.values(FOOD_TYPES).map(item => [item.type, item.key]));
const FOOD_TOTAL_KEYS = [...new Set(Object.values(FOOD_TYPES).map(item => item.key))];
function setHealthStatus(text) {
  const el = document.getElementById('health-import-status');
  if (el) el.textContent = text || '';
}
function renderHealthImportStatus() {
  setHealthStatus('');
}
function decodeXMLAttr(value) {
  return String(value || '')
    .replace(/&quot;/g, '"')
    .replace(/&apos;/g, "'")
    .replace(/&lt;/g, '<')
    .replace(/&gt;/g, '>')
    .replace(/&amp;/g, '&');
}
function parseXMLAttrs(text) {
  const attrs = {};
  String(text || '').replace(/([A-Za-z_:][\w:.-]*)="([^"]*)"/g, (_, key, value) => {
    attrs[key] = decodeXMLAttr(value);
    return '';
  });
  return attrs;
}
function parseAppleDate(value) {
  const m = String(value || '').match(/^(\d{4})-(\d{2})-(\d{2}) (\d{2}):(\d{2}):(\d{2}) ([+-]\d{2})(\d{2})$/);
  if (!m) {
    const d = new Date(value);
    return isNaN(d) ? null : d;
  }
  return new Date(`${m[1]}-${m[2]}-${m[3]}T${m[4]}:${m[5]}:${m[6]}${m[7]}:${m[8]}`);
}
function appleDateKey(value) {
  const raw = String(value || '');
  const m = raw.match(/^(\d{4}-\d{2}-\d{2})/);
  if (m) return m[1];
  return getDateKey(raw);
}
function minutesBetween(start, end) {
  const s = parseAppleDate(start);
  const e = parseAppleDate(end);
  if (!s || !e) return 0;
  return Math.max(0, (e - s) / 60000);
}
function convertHealthValue(value, unit) {
  const n = normalizeNumber(value);
  if (n == null) return null;
  const u = String(unit || '').toLowerCase();
  if (u === 'kj') return n / 4.184;
  if (u === 'sec' || u === 's') return n / 60;
  if (u === 'hr' || u === 'h') return n * 60;
  return n;
}
function convertDistanceValue(value, unit) {
  const n = normalizeNumber(value);
  if (n == null) return null;
  const u = String(unit || '').toLowerCase();
  if (u === 'm' || u === 'meter' || u === 'meters') return n / 1000;
  if (u === 'mi' || u === 'mile' || u === 'miles') return n * 1.60934;
  return n;
}
function convertPercentValue(value) {
  const n = normalizeNumber(value);
  if (n == null) return null;
  return n <= 1 ? n * 100 : n;
}
function convertLengthToCm(value, unit) {
  const n = normalizeNumber(value);
  if (n == null) return null;
  const u = String(unit || '').toLowerCase();
  if (u === 'm' || u === 'meter' || u === 'meters') return n * 100;
  if (u === 'in' || u === 'inch' || u === 'inches') return n * 2.54;
  return n;
}
function convertFoodValue(value, unit, key) {
  const n = normalizeNumber(value);
  if (n == null) return null;
  const u = String(unit || '').toLowerCase();
  if (key === 'calories_kcal') return u === 'kj' ? n / 4.184 : n;
  if (key === 'water_ml') {
    if (u === 'ml' || u === 'milliliter' || u === 'millilitre') return n;
    if (u === 'l' || u === 'liter' || u === 'litre') return n * 1000;
    if (u === 'fl_oz' || u === 'floz') return n * 29.5735;
    return n;
  }
  if (key.endsWith('_mg')) {
    if (u === 'g') return n * 1000;
    if (u === 'mcg' || u === 'µg') return n / 1000;
    return n;
  }
  if (key.endsWith('_mcg')) {
    if (u === 'g') return n * 1000000;
    if (u === 'mg') return n * 1000;
    return n;
  }
  if (u === 'mg') return n / 1000;
  if (u === 'kg') return n * 1000;
  return n;
}
function parseMetadataValue(block, key) {
  const pattern = new RegExp(`<MetadataEntry\\b[^>]*key="${key}"[^>]*value="([^"]*)"`, 'i');
  const match = String(block || '').match(pattern);
  return match ? decodeXMLAttr(match[1]) : '';
}
function roundFoodValue(value) {
  if (value == null || !Number.isFinite(value)) return 0;
  return Math.round(value * 10) / 10;
}
function createHealthAggregator() {
  const days = new Map();
  const foodItems = new Map();
  const seenFoodRecords = new Set();
  const stats = { records: 0, usedRecords: 0, workouts: 0, foodRecords: 0, foodItems: 0 };
  const day = (key) => {
    if (!key || !isHealthDateAllowed(key)) return null;
    if (!days.has(key)) days.set(key, { date: key });
    return days.get(key);
  };
  const addAvg = (d, key, value) => {
    if (!d || value == null || !Number.isFinite(value)) return;
    d[`_${key}_sum`] = (d[`_${key}_sum`] || 0) + value;
    d[`_${key}_count`] = (d[`_${key}_count`] || 0) + 1;
  };
  const addSum = (d, key, value) => {
    if (!d || value == null || !Number.isFinite(value)) return;
    d[key] = (d[key] || 0) + value;
  };
  const addSourceSum = (d, key, value, source) => {
    if (!d || value == null || !Number.isFinite(value)) return;
    const bucket = `_${key}_by_source`;
    const sourceName = source || 'unknown';
    if (!d[bucket]) d[bucket] = {};
    d[bucket][sourceName] = (d[bucket][sourceName] || 0) + value;
  };
  const ignoredEnergySource = (source) => /yazio/i.test(String(source || ''));
  const pickSourceValue = (entries, key) => {
    let usable = entries;
    if (key === 'active_energy_kcal' || key === 'basal_energy_kcal') {
      usable = entries.filter(([source]) => !ignoredEnergySource(source));
    }
    if (!usable.length) usable = entries;
    return usable.sort((a, b) => b[1] - a[1])[0] || null;
  };
  return {
    stats,
    rememberSource(d, key, source) {
      if (!d || !source) return;
      if (!d.health_sources) d.health_sources = {};
      d.health_sources[key] = source;
    },
    addFoodRecord(attrs, block) {
      if (attrs.sourceName !== 'Yazio') return;
      const key = FOOD_TYPE_BY_HEALTH_TYPE[attrs.type];
      if (!key) return;
      const date = appleDateKey(attrs.startDate || attrs.creationDate);
      if (!isHealthDateAllowed(date)) return;
      const value = convertFoodValue(attrs.value, attrs.unit, key);
      if (value == null || !Number.isFinite(value)) return;
      const uuid = parseMetadataValue(block, 'HKExternalUUID') ||
        `${date}|${attrs.startDate || ''}|${attrs.type}|${attrs.value || ''}`;
      const dedupeKey = `${uuid}|${attrs.type}`;
      if (seenFoodRecords.has(dedupeKey)) return;
      seenFoodRecords.add(dedupeKey);
      const name = parseMetadataValue(block, 'HKFoodType') || 'Без названия';
      if (!foodItems.has(uuid)) {
        foodItems.set(uuid, {
          uuid,
          date,
          time: attrs.startDate || attrs.creationDate || '',
          name,
          source: attrs.sourceName
        });
      }
      const item = foodItems.get(uuid);
      if (!item.name || item.name === 'Без названия') item.name = name;
      item[key] = roundFoodValue((item[key] || 0) + value);
      stats.foodRecords++;
    },
    addRecord(attrs) {
      stats.records++;
      const type = attrs.type;
      if (!Object.values(HEALTH_TYPES).includes(type)) return;
      stats.usedRecords++;
      const value = convertHealthValue(attrs.value, attrs.unit);
      if (type === HEALTH_TYPES.sleep) {
        const d = day(appleDateKey(attrs.endDate || attrs.startDate));
        if (!d) return;
        const min = minutesBetween(attrs.startDate, attrs.endDate);
        const state = attrs.value || '';
        if (state.includes('InBed')) addSum(d, 'sleep_in_bed_min', min);
        if (state.includes('Awake')) {
          addSum(d, 'sleep_awake_min', min);
          d.sleep_awake_count = (d.sleep_awake_count || 0) + 1;
        }
        if (state.includes('Asleep')) addSum(d, 'sleep_asleep_min', min);
        if (state.includes('AsleepREM')) addSum(d, 'sleep_rem_min', min);
        if (state.includes('AsleepDeep')) addSum(d, 'sleep_deep_min', min);
        if (state.includes('AsleepCore')) addSum(d, 'sleep_core_min', min);
        return;
      }
      const d = day(appleDateKey(attrs.startDate || attrs.creationDate));
      if (type === HEALTH_TYPES.heartRate) addAvg(d, 'avg_hr_bpm', value);
      if (type === HEALTH_TYPES.restingHR) addAvg(d, 'resting_hr_bpm', value);
      if (type === HEALTH_TYPES.walkingHR) addAvg(d, 'walking_hr_bpm', value);
      if (type === HEALTH_TYPES.hrv) addAvg(d, 'hrv_sdnn_ms', value);
      if (type === HEALTH_TYPES.vo2max) addAvg(d, 'vo2max', value);
      if (type === HEALTH_TYPES.respiratoryRate) addAvg(d, 'respiratory_rate_bpm', value);
      if (type === HEALTH_TYPES.oxygenSaturation) addAvg(d, 'oxygen_saturation_pct', convertPercentValue(attrs.value));
      if (type === HEALTH_TYPES.steps) addSourceSum(d, 'steps', value, attrs.sourceName);
      if (type === HEALTH_TYPES.distanceWalkingRunning) addSourceSum(d, 'distance_km', convertDistanceValue(attrs.value, attrs.unit), attrs.sourceName);
      if (type === HEALTH_TYPES.activeEnergy) addSourceSum(d, 'active_energy_kcal', value, attrs.sourceName);
      if (type === HEALTH_TYPES.basalEnergy) addSourceSum(d, 'basal_energy_kcal', value, attrs.sourceName);
      if (type === HEALTH_TYPES.exerciseTime) addSourceSum(d, 'exercise_minutes', value, attrs.sourceName);
      if (type === HEALTH_TYPES.standTime) addSourceSum(d, 'stand_minutes', value, attrs.sourceName);
      if (type === HEALTH_TYPES.flightsClimbed) addSourceSum(d, 'flights_climbed', value, attrs.sourceName);
      if (type === HEALTH_TYPES.bodyMass) { addAvg(d, 'body_mass_kg', convertHealthValue(attrs.value, attrs.unit)); this.rememberSource(d, 'body_mass_kg', attrs.sourceName); }
      if (type === HEALTH_TYPES.bodyFat) { addAvg(d, 'body_fat_pct', convertPercentValue(attrs.value)); this.rememberSource(d, 'body_fat_pct', attrs.sourceName); }
      if (type === HEALTH_TYPES.leanBodyMass) { addAvg(d, 'lean_body_mass_kg', convertHealthValue(attrs.value, attrs.unit)); this.rememberSource(d, 'lean_body_mass_kg', attrs.sourceName); }
      if (type === HEALTH_TYPES.bodyMassIndex) { addAvg(d, 'body_mass_index', value); this.rememberSource(d, 'body_mass_index', attrs.sourceName); }
      if (type === HEALTH_TYPES.waistCircumference) { addAvg(d, 'waist_cm', convertLengthToCm(attrs.value, attrs.unit)); this.rememberSource(d, 'waist_cm', attrs.sourceName); }
    },
    addWorkoutStatistic(attrs) {
      const d = day(appleDateKey(attrs.startDate || attrs.endDate));
      if (!d) return;
      const type = attrs.type;
      const rawValue = attrs.sum || attrs.average || attrs.value;
      if (type === HEALTH_TYPES.activeEnergy) {
        addSum(d, 'workout_energy_kcal', convertHealthValue(rawValue, attrs.unit || 'kcal'));
      }
      if (type === HEALTH_TYPES.basalEnergy) {
        addSum(d, 'workout_basal_energy_kcal', convertHealthValue(rawValue, attrs.unit || 'kcal'));
      }
      if (type === HEALTH_TYPES.distanceWalkingRunning) {
        addSum(d, 'workout_distance_km', convertDistanceValue(rawValue, attrs.unit));
      }
      if (type === HEALTH_TYPES.heartRate && attrs.average != null) {
        addAvg(d, 'workout_avg_hr_bpm', convertHealthValue(attrs.average, attrs.unit));
      }
    },
    addWorkout(attrs) {
      stats.workouts++;
      const d = day(appleDateKey(attrs.startDate));
      if (!d) return;
      const duration = convertHealthValue(attrs.duration, attrs.durationUnit || 'min') || minutesBetween(attrs.startDate, attrs.endDate);
      addSum(d, 'workout_minutes', duration);
      d.workouts_count = (d.workouts_count || 0) + 1;
      const kcal = convertHealthValue(attrs.totalEnergyBurned, attrs.totalEnergyBurnedUnit || 'Cal');
      if (kcal != null) addSum(d, '_workout_header_energy_kcal', kcal);
      const type = String(attrs.workoutActivityType || '').replace(/^HKWorkoutActivityType/, '');
      if (type) {
        if (!d.workout_types) d.workout_types = {};
        d.workout_types[type] = (d.workout_types[type] || 0) + 1;
      }
    },
    dayCount() {
      return days.size;
    },
    finalize() {
      const rows = Array.from(days.values()).sort((a, b) => a.date.localeCompare(b.date));
      rows.forEach(d => {
        ['avg_hr_bpm', 'resting_hr_bpm', 'walking_hr_bpm', 'hrv_sdnn_ms', 'vo2max', 'respiratory_rate_bpm', 'oxygen_saturation_pct', 'body_mass_kg', 'body_fat_pct', 'lean_body_mass_kg', 'body_mass_index', 'waist_cm', 'workout_avg_hr_bpm'].forEach(key => {
          const count = d[`_${key}_count`] || 0;
          if (count) d[key] = round1(d[`_${key}_sum`] / count);
          delete d[`_${key}_sum`];
          delete d[`_${key}_count`];
        });
        ['steps', 'distance_km', 'active_energy_kcal', 'basal_energy_kcal', 'exercise_minutes', 'stand_minutes', 'flights_climbed'].forEach(key => {
          const bucket = d[`_${key}_by_source`];
          if (bucket) {
            const picked = pickSourceValue(Object.entries(bucket), key);
            if (picked) {
              d[key] = picked[1];
              if (!d.health_sources) d.health_sources = {};
              d.health_sources[key] = picked[0];
            }
          }
          delete d[`_${key}_by_source`];
        });
        if (d.workout_energy_kcal == null && d._workout_header_energy_kcal != null) {
          d.workout_energy_kcal = d._workout_header_energy_kcal;
        }
        delete d._workout_header_energy_kcal;
        ['steps', 'distance_km', 'active_energy_kcal', 'basal_energy_kcal', 'exercise_minutes', 'stand_minutes', 'flights_climbed', 'sleep_in_bed_min', 'sleep_asleep_min', 'sleep_awake_min', 'sleep_rem_min', 'sleep_deep_min', 'sleep_core_min', 'workout_minutes', 'workout_energy_kcal', 'workout_basal_energy_kcal', 'workout_distance_km', 'workout_avg_hr_bpm'].forEach(key => {
          if (d[key] != null) d[key] = round1(d[key]);
        });
        if (d.sleep_asleep_min && d.sleep_in_bed_min) d.sleep_efficiency_pct = round1(d.sleep_asleep_min / d.sleep_in_bed_min * 100);
        if (d.sleep_asleep_min) {
          if (d.sleep_rem_min) d.sleep_rem_pct = round1(d.sleep_rem_min / d.sleep_asleep_min * 100);
          if (d.sleep_deep_min) d.sleep_deep_pct = round1(d.sleep_deep_min / d.sleep_asleep_min * 100);
          if (d.sleep_core_min) d.sleep_core_pct = round1(d.sleep_core_min / d.sleep_asleep_min * 100);
        }
      });
      const byDate = new Map();
      Array.from(foodItems.values()).forEach(item => {
        if (!item.date || !isHealthDateAllowed(item.date)) return;
        const clean = {
          uuid: item.uuid,
          name: item.name || 'Без названия',
          time: item.time || '',
        };
        FOOD_TOTAL_KEYS.forEach(key => { clean[key] = roundFoodValue(item[key] || 0); });
        if (!FOOD_TOTAL_KEYS.some(key => clean[key])) return;
        if (!byDate.has(item.date)) byDate.set(item.date, { date: item.date, source: 'Yazio', items: [] });
        byDate.get(item.date).items.push(clean);
      });
      const foodRows = Array.from(byDate.values()).sort((a, b) => a.date.localeCompare(b.date));
      foodRows.forEach(day => {
        day.items.sort((a, b) => (a.time || '').localeCompare(b.time || '') || (b.calories_kcal || 0) - (a.calories_kcal || 0));
        FOOD_TOTAL_KEYS.forEach(key => {
          day[key] = roundFoodValue(day.items.reduce((sum, item) => sum + (item[key] || 0), 0));
        });
        day.food_count = day.items.length;
      });
      stats.foodItems = foodRows.reduce((sum, day) => sum + day.items.length, 0);
      return { rows, foodRows };
    }
  };
}
function processHealthXMLText(text, aggregator) {
  const interesting = Object.values(HEALTH_TYPES);
  text.replace(/<Record\b([^>]*?)>([\s\S]*?)<\/Record>/g, (block, attrsText) => {
    const attrs = parseXMLAttrs(attrsText);
    if (interesting.includes(attrs.type)) aggregator.addRecord(attrs);
    aggregator.addFoodRecord(attrs, block);
    return '';
  });
  text.replace(/<Record\b([^>]*?)\/>/g, (tag, attrsText) => {
    const attrs = parseXMLAttrs(attrsText);
    if (interesting.includes(attrs.type)) aggregator.addRecord(attrs);
    aggregator.addFoodRecord(attrs, tag);
    return '';
  });
  text.replace(/<Workout\b([^>]*?)>([\s\S]*?)<\/Workout>/g, (block, attrsText, body) => {
    aggregator.addWorkout(parseXMLAttrs(attrsText));
    body.replace(/<WorkoutStatistics\b([^>]*?)(?:\/>|>)/g, (_, statAttrsText) => {
      aggregator.addWorkoutStatistic(parseXMLAttrs(statAttrsText));
      return '';
    });
    return '';
  });
}
function getUnclosedBlockStart(text, tag) {
  const open = text.lastIndexOf(`<${tag}`);
  if (open < 0) return -1;
  const close = text.lastIndexOf(`</${tag}>`);
  if (open < close) return -1;
  const end = text.indexOf('>', open);
  if (end >= 0 && text[end - 1] === '/') return -1;
  return open;
}
function findSafeXMLCut(text) {
  const unclosedStarts = [getUnclosedBlockStart(text, 'Record'), getUnclosedBlockStart(text, 'Workout')]
    .filter(index => index >= 0);
  const limit = unclosedStarts.length ? Math.min(...unclosedStarts) : text.length;
  if (limit <= 0) return 0;
  const chunk = text.slice(0, limit);
  const candidates = [
    chunk.lastIndexOf('</Record>') >= 0 ? chunk.lastIndexOf('</Record>') + '</Record>'.length : 0,
    chunk.lastIndexOf('</Workout>') >= 0 ? chunk.lastIndexOf('</Workout>') + '</Workout>'.length : 0,
    chunk.lastIndexOf('/>') >= 0 ? chunk.lastIndexOf('/>') + 2 : 0
  ];
  return Math.max(...candidates);
}
async function parseHealthXMLStream(stream, sizeHint = 0) {
  const reader = stream.getReader();
  const decoder = new TextDecoder();
  const aggregator = createHealthAggregator();
  let tail = '';
  let loaded = 0;
  let lastStatusAt = 0;
  while (true) {
    const { value, done } = await reader.read();
    if (done) break;
    loaded += value.byteLength || 0;
    tail += decoder.decode(value, { stream: true });
    const cut = findSafeXMLCut(tail);
    if (cut > 0) {
      processHealthXMLText(tail.slice(0, cut), aggregator);
      tail = tail.slice(cut);
    }
    const now = Date.now();
    if (now - lastStatusAt > 500) {
      const pct = sizeHint ? ` · ${Math.min(99, Math.round(loaded / sizeHint * 100))}%` : '';
      setHealthStatus(`Читаю Apple Health${pct}. Найдено дней: ${aggregator.dayCount()}`);
      lastStatusAt = now;
    }
  }
  tail += decoder.decode();
  processHealthXMLText(tail, aggregator);
  const finalized = aggregator.finalize();
  return { rows: finalized.rows, foodRows: finalized.foodRows, stats: aggregator.stats };
}
function readU16(view, offset) { return view.getUint16(offset, true); }
function readU32(view, offset) { return view.getUint32(offset, true); }
function findZipEOCD(view) {
  const min = Math.max(0, view.byteLength - 66000);
  for (let i = view.byteLength - 22; i >= min; i--) {
    if (readU32(view, i) === 0x06054b50) return i;
  }
  return -1;
}
async function getXMLStreamFromZip(file) {
  if (typeof DecompressionStream === 'undefined') {
    throw new Error('Этот браузер не умеет распаковывать ZIP внутри сайта. Загрузи распакованный export.xml или открой в современном Safari/Chrome.');
  }
  const buffer = await file.arrayBuffer();
  const view = new DataView(buffer);
  const eocd = findZipEOCD(view);
  if (eocd < 0) throw new Error('Не нашел структуру ZIP. Возможно файл поврежден.');
  const entries = [];
  let offset = readU32(view, eocd + 16);
  const total = readU16(view, eocd + 10);
  const decoder = new TextDecoder();
  for (let i = 0; i < total && offset < view.byteLength; i++) {
    if (readU32(view, offset) !== 0x02014b50) break;
    const method = readU16(view, offset + 10);
    const compressedSize = readU32(view, offset + 20);
    const uncompressedSize = readU32(view, offset + 24);
    const nameLen = readU16(view, offset + 28);
    const extraLen = readU16(view, offset + 30);
    const commentLen = readU16(view, offset + 32);
    const localOffset = readU32(view, offset + 42);
    const nameBytes = new Uint8Array(buffer, offset + 46, nameLen);
    const name = decoder.decode(nameBytes);
    entries.push({ name, method, compressedSize, uncompressedSize, localOffset });
    offset += 46 + nameLen + extraLen + commentLen;
  }
  const xmlEntries = entries.filter(e => /\.xml$/i.test(e.name) && !/export_cda/i.test(e.name));
  const entry = (xmlEntries.length ? xmlEntries : entries.filter(e => /\.xml$/i.test(e.name)))
    .sort((a, b) => b.uncompressedSize - a.uncompressedSize)[0];
  if (!entry) throw new Error('В ZIP не найден export.xml.');
  if (readU32(view, entry.localOffset) !== 0x04034b50) throw new Error('Не смог открыть XML внутри ZIP.');
  const nameLen = readU16(view, entry.localOffset + 26);
  const extraLen = readU16(view, entry.localOffset + 28);
  const dataStart = entry.localOffset + 30 + nameLen + extraLen;
  const blob = file.slice(dataStart, dataStart + entry.compressedSize);
  if (entry.method === 0) return { stream: blob.stream(), size: entry.uncompressedSize, entryName: entry.name };
  if (entry.method !== 8) throw new Error(`ZIP использует неподдерживаемое сжатие (${entry.method}).`);
  return {
    stream: blob.stream().pipeThrough(new DecompressionStream('deflate-raw')),
    size: entry.uncompressedSize,
    entryName: entry.name
  };
}
async function importAppleHealthFile(file) {
  if (!file) return;
  try {
    setHealthStatus('Открываю файл Apple Health...');
    const isZip = /\.zip$/i.test(file.name);
    const source = isZip
      ? await getXMLStreamFromZip(file)
      : { stream: file.stream(), size: file.size, entryName: file.name };
    setHealthStatus(`Нашел ${source.entryName}. Читаю XML...`);
    const result = await parseHealthXMLStream(source.stream, source.size);
    if (!result.rows.length && !result.foodRows.length) {
      setHealthStatus('XML прочитан, но нужные данные Apple Health/Yazio не найдены.');
      alert('Не нашел сон/HRV/пульс/шаги/питание в этом файле.');
      return;
    }
    saveHealthDaily(result.rows);
    saveFoodDaily(result.foodRows || []);
    const allDates = [...(result.rows || []), ...(result.foodRows || [])].map(row => row.date).sort();
    saveHealthImportMeta({
      file: file.name,
      xml_entry: source.entryName,
      imported_at: new Date().toISOString(),
      days: result.rows.length,
      food_days: (result.foodRows || []).length,
      food_items: result.stats.foodItems || 0,
      records_seen: result.stats.records,
      records_used: result.stats.usedRecords,
      food_records: result.stats.foodRecords || 0,
      workouts: result.stats.workouts,
      limited_from: HEALTH_IMPORT_START_DATE,
      range_start: allDates[0] || null,
      range_end: allDates[allDates.length - 1] || null
    });
    renderDashboard();
    renderHealth();
    renderFood();
    initSettings();
    alert(`Импорт готов: Health ${result.rows.length} дн., еда ${result.foodRows.length} дн. / ${result.stats.foodItems || 0} продуктов с ${HEALTH_IMPORT_START_DATE}.`);
  } catch (e) {
    setHealthStatus(e.message || 'Не получилось импортировать Apple Health.');
    alert(e.message || 'Не получилось импортировать Apple Health.');
  }
}

// ===== SETTINGS =====
function initSettings() {
  const s = getSettings();
  document.getElementById('toggle-timer').classList.toggle('on', !!s.timer);
  document.getElementById('toggle-autoclose').classList.toggle('on', !!s.autoclose);
  document.getElementById('start-date').value = getStartDate();
  const progVersion = document.getElementById('prog-version');
  if (progVersion) progVersion.textContent = getProgram().version;
  applySectionVisibility();
  renderHealthImportStatus();
}
function toggleSetting(key) {
  const s = getSettings();
  s[key] = !s[key];
  saveSettings(s);
  document.getElementById('toggle-' + key).classList.toggle('on', s[key]);
}

// ===== PROGRAM EDITOR =====
function openProgramEditor() {
  editorDay = "upperA";
  renderProgramEditor();
  document.getElementById('modal').classList.add('active');
}
function renderProgramEditor() {
  const program = getProgram();
  const body = document.getElementById('modal-body');
  document.getElementById('modal-title').textContent = `Программа v${program.version}`;
  const dayKeys = Object.keys(program.days);
  const dayLabels = { upperA: "Upper A", upperB: "Upper B", lower: "Lower" };
  
  body.innerHTML = `
    <div class="program-editor">
      <div class="program-editor-top">
        <div class="editor-day-tab">
          ${dayKeys.map(k => `<button class="${k === editorDay ? 'active' : ''}" onclick="switchEditorDay('${k}')">${dayLabels[k] || k}</button>`).join('')}
        </div>
        <div class="editor-field">
          <label for="day-name-input">Название дня</label>
          <input class="editor-input" type="text" id="day-name-input" value="${escapeHTML(program.days[editorDay].name)}" onchange="updateDayName(this.value)">
        </div>
        <div class="editor-hint" style="margin-top:10px;">Таймер берёт длительность из поля «Отдых, сек». Кнопка «⇄ Замена» в тренировке показывает варианты из поля «Замены».</div>
      </div>
      <div class="editor-section-title">
        <span>Упражнения</span>
        <span>${program.days[editorDay].exercises.length} шт.</span>
      </div>
      <div id="editor-exercises">
        ${program.days[editorDay].exercises.map((ex, i) => renderEditorExercise(ex, i)).join('')}
      </div>
      <button class="btn-secondary" onclick="addEditorExercise()">+ Добавить упражнение</button>
      <button class="btn-primary" onclick="closeProgramEditor()">Готово</button>
    </div>
  `;
}
function renderEditorExercise(ex, idx) {
  return `
    <div class="editor-ex">
      <div class="editor-ex-head">
        <div class="editor-ex-num">#${idx + 1}</div>
        <div class="editor-ex-actions">
          <button onclick="moveEditorEx(${idx}, -1)" aria-label="Выше">↑</button>
          <button onclick="moveEditorEx(${idx}, 1)" aria-label="Ниже">↓</button>
          <button class="del" onclick="deleteEditorEx(${idx})" aria-label="Удалить">×</button>
        </div>
      </div>
      <div class="editor-field">
        <label>Название</label>
        <input class="editor-input" type="text" placeholder="Жим штанги" value="${escapeHTML(ex.name)}" onchange="updateEditorEx(${idx}, 'name', this.value)">
      </div>
      <div class="editor-field" style="margin-top:10px;">
        <label>Алиасы истории</label>
        <input class="editor-input" type="text" placeholder="Старые названия через запятую" value="${escapeHTML((ex.aliases || []).join(', '))}" onchange="updateEditorEx(${idx}, 'aliases', parseNameList(this.value))">
        <div class="editor-hint">Если переименуешь упражнение, старое название попадет сюда, и графики/прошлые подходы не потеряются.</div>
      </div>
      <div class="editor-field" style="margin-top:10px;">
        <label>Цель подходов</label>
        <input class="editor-input" type="text" placeholder="3×8-10, RIR 2" value="${escapeHTML(ex.target || '')}" onchange="updateEditorEx(${idx}, 'target', this.value)">
      </div>
      <div class="editor-grid" style="margin-top:10px;">
        <div class="editor-field">
          <label>Подходы</label>
          <input class="editor-input num" type="number" value="${ex.sets}" onchange="updateEditorEx(${idx}, 'sets', parseInt(this.value)||0)">
        </div>
        <div class="editor-field">
          <label>Отдых после подхода, сек</label>
          <input class="editor-input num" type="number" step="15" value="${ex.rest || 90}" onchange="updateEditorEx(${idx}, 'rest', parseInt(this.value)||90)">
        </div>
        <div class="editor-field">
          <label>Повт. мин</label>
          <input class="editor-input num" type="number" value="${ex.reps_min || ''}" onchange="updateEditorEx(${idx}, 'reps_min', parseInt(this.value)||0)">
        </div>
        <div class="editor-field">
          <label>Повт. макс</label>
          <input class="editor-input num" type="number" value="${ex.reps_max || ''}" onchange="updateEditorEx(${idx}, 'reps_max', parseInt(this.value)||0)">
        </div>
      </div>
      <div class="editor-field" style="margin-top:10px;">
        <label>Замены для кнопки «⇄ Замена»</label>
        <input class="editor-input" type="text" placeholder="Через запятую" value="${escapeHTML((ex.swaps || []).join(', '))}" onchange="updateEditorEx(${idx}, 'swaps', parseNameList(this.value))">
      </div>
    </div>
  `;
}
function switchEditorDay(d) { editorDay = d; renderProgramEditor(); }
function updateDayName(v) { const p = getProgram(); p.days[editorDay].name = v; saveProgram(p); }
function updateEditorEx(idx, field, value) {
  const p = getProgram();
  const ex = p.days[editorDay].exercises[idx];
  if (!ex) return;
  if (field === 'name') {
    const oldName = String(ex.name || '').trim();
    const newName = String(value || '').trim();
    if (!newName) return;
    if (oldName && normalizeExerciseName(oldName) !== normalizeExerciseName(newName)) {
      ex.aliases = cleanExerciseAliases([...(ex.aliases || []), oldName], newName);
    }
    ex.name = newName;
  } else if (field === 'aliases') {
    ex.aliases = cleanExerciseAliases(value, ex.name);
  } else if (field === 'swaps') {
    ex.swaps = parseNameList(Array.isArray(value) ? value.join(',') : value);
  } else {
    ex[field] = value;
  }
  saveProgram(p);
  if (field === 'name') renderProgramEditor();
}
function moveEditorEx(idx, dir) {
  const p = getProgram();
  const ex = p.days[editorDay].exercises;
  const ni = idx + dir;
  if (ni < 0 || ni >= ex.length) return;
  [ex[idx], ex[ni]] = [ex[ni], ex[idx]];
  saveProgram(p);
  renderProgramEditor();
}
function deleteEditorEx(idx) {
  if (!confirm('Удалить упражнение из программы?')) return;
  const p = getProgram();
  p.days[editorDay].exercises.splice(idx, 1);
  saveProgram(p);
  renderProgramEditor();
}
function addEditorExercise() {
  const p = getProgram();
  p.days[editorDay].exercises.push({
    name: "Новое упражнение", aliases: [], target: "3×10, RIR 1", sets: 3, reps_min: 10, reps_max: 12, rest: 90, swaps: []
  });
  saveProgram(p);
  renderProgramEditor();
}
function closeProgramEditor() { closeModal(); }
function newProgramVersion() {
  if (!confirm('Создать новую версию программы? Старая история сохранится, можно будет редактировать с нуля.')) return;
  const p = getProgram();
  p.version = (p.version || 1) + 1;
  saveProgram(p);
  alert(`Программа теперь v${p.version}. Открой редактор и измени упражнения.`);
  initSettings();
}

// ===== EXPORT / IMPORT =====
function getExportPayload() {
  return {
    app: 'trenya',
    backup_version: 2,
    history: getHistory(),
    measures: getMeasures(),
    apple_health_daily: getHealthDaily(),
    yazio_food_daily: getFoodDaily(),
    apple_health_import: getHealthImportMeta(),
    goals: getGoals(),
    program: getProgram(),
    start_date: getStartDate(),
    settings: getSettings(),
    exported_at: new Date().toISOString()
  };
}
function downloadJSONFile(filename, payload) {
  const data = JSON.stringify(payload, null, 2);
  const blob = new Blob([data], { type: 'application/json;charset=utf-8' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = filename;
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  setTimeout(() => URL.revokeObjectURL(url), 1000);
}
function downloadData() {
  const stamp = new Date().toISOString().split('T')[0];
  downloadJSONFile(`trenya-backup-${stamp}.json`, getExportPayload());
}
function getWorkoutSummaryForAI(workout) {
  const exercises = (workout.exercises || []).map(ex => {
    const sets = (ex.sets || []).filter(setHasLiftData).map(s => ({
      weight_kg: normalizeNumber(s.weight),
      reps: parseInt(s.reps, 10) || null,
      rir: s.rir || null,
      drop: dropSetHasData(s) ? {
        weight_kg: normalizeNumber(s.drop.weight),
        reps: parseInt(s.drop.reps, 10) || null
      } : null
    }));
    return {
      name: ex.name,
      target: ex.target || null,
      tonnage_kg: round1((ex.sets || []).reduce((sum, s) => sum + getSetVolume(s), 0)),
      sets,
      note: ex.note || null
    };
  });
  return {
    date: getDateKey(workout.date),
    day: workout.day,
    day_name: workout.dayName,
    week: workout.week || null,
    program_version: workout.programVersion || null,
    total_tonnage_kg: round1(exercises.reduce((sum, ex) => sum + (ex.tonnage_kg || 0), 0)),
    exercises,
    note: workout.note || null
  };
}
function getAIExportPayload() {
  const history = getHistory();
  const health = getHealthDaily();
  const food = getFoodDaily();
  return {
    schema: 'trenya-ai-analysis-v1',
    generated_at: new Date().toISOString(),
    instruction: 'Проанализируй тренировки, прогрессию, восстановление, замеры и возможные связи между нагрузкой, сном, HRV и пульсом покоя. Не ставь диагнозы.',
    summary: {
      workouts_count: history.length,
      first_workout: history[0] ? getDateKey(history[0].date) : null,
      last_workout: history[history.length - 1] ? getDateKey(history[history.length - 1].date) : null,
      body_measures_count: getMeasures().length,
      apple_health_days: health.length,
      apple_health_range: health.length ? { start: health[0].date, end: health[health.length - 1].date } : null,
      yazio_food_days: food.length,
      yazio_food_range: food.length ? { start: food[0].date, end: food[food.length - 1].date } : null
    },
    program: getProgram(),
    workouts: history.map(getWorkoutSummaryForAI),
    body_measures: getMeasures(),
    goals: getGoals(),
    apple_health_daily: health,
    yazio_food_daily: food,
    apple_health_import: getHealthImportMeta()
  };
}
function downloadAIExport() {
  const stamp = new Date().toISOString().split('T')[0];
  downloadJSONFile(`trenya-ai-export-${stamp}.json`, getAIExportPayload());
}
function importDataFile(file) {
  if (!file) return;
  const reader = new FileReader();
  reader.onload = () => {
    try {
      importData(JSON.parse(reader.result));
    } catch (e) {
      alert('Не получилось прочитать JSON-файл.');
    }
  };
  reader.onerror = () => alert('Не получилось открыть файл.');
  reader.readAsText(file);
}
function importData(data) {
  const has = (key) => Object.prototype.hasOwnProperty.call(data, key);
  if (!data || typeof data !== 'object' || !['history','measures','goals','program','start_date','settings','apple_health_daily','yazio_food_daily'].some(has)) {
    alert('Это не похоже на backup-файл Трени.');
    return;
  }
  if (!confirm('Импорт заменит текущие данные в этом браузере. Продолжить?')) return;
  if (has('history')) saveHistory(Array.isArray(data.history) ? data.history : []);
  if (has('measures')) saveMeasures(Array.isArray(data.measures) ? data.measures : []);
  if (has('apple_health_daily')) saveHealthDaily(Array.isArray(data.apple_health_daily) ? data.apple_health_daily : []);
  if (has('yazio_food_daily')) saveFoodDaily(Array.isArray(data.yazio_food_daily) ? data.yazio_food_daily : []);
  if (has('apple_health_import')) saveHealthImportMeta(data.apple_health_import && typeof data.apple_health_import === 'object' ? data.apple_health_import : null);
  if (has('goals')) saveGoals(data.goals && typeof data.goals === 'object' ? data.goals : {});
  if (has('program')) saveProgram(data.program && typeof data.program === 'object' ? data.program : DEFAULT_PROGRAM);
  if (has('start_date')) localStorage.setItem('start_date', data.start_date || new Date().toISOString().split('T')[0]);
  if (has('settings')) saveSettings(data.settings && typeof data.settings === 'object' ? data.settings : getSettings());
  alert('Импорт готов. Страница перезагрузится.');
  location.reload();
}
function resetAll() {
  if (!confirm('Точно удалить ВСЕ данные?')) return;
  if (!confirm('Серьёзно? История, замеры, программа — всё потеряется.')) return;
  localStorage.clear();
  location.reload();
}
function enforceHealthDateLimit() {
  const raw = readJSON('apple_health_daily', []);
  const filtered = filterHealthRows(raw);
  const rawFood = readJSON('yazio_food_daily', []);
  const filteredFood = filterHealthRows(rawFood);
  if (Array.isArray(raw) && raw.length !== filtered.length) {
    saveHealthDaily(filtered);
    const meta = getHealthImportMeta();
    if (meta && filtered.length) {
      saveHealthImportMeta({
        ...meta,
        days: filtered.length,
        range_start: filtered[0].date,
        range_end: filtered[filtered.length - 1].date,
        limited_from: HEALTH_IMPORT_START_DATE
      });
    }
  }
  if (Array.isArray(rawFood) && rawFood.length !== filteredFood.length) saveFoodDaily(filteredFood);
}

// ===== INIT =====
getProgram(); // ensure default saved
enforceHealthDateLimit();
initTapAnimations();
initSetSwipeGestures();
applySectionVisibility();
renderDashboard();
animateScreen(document.getElementById('screen-dashboard'));
restoreTimerState();
window.addEventListener('beforeunload', (event) => {
  if (!hasWorkoutInput()) return;
  saveWorkoutDraft();
  event.preventDefault();
  event.returnValue = '';
});

if ("serviceWorker" in navigator) {
  window.addEventListener("load", () => {
    let refreshingForUpdate = false;
    navigator.serviceWorker.addEventListener("controllerchange", () => {
      if (refreshingForUpdate || sessionStorage.getItem("sw-refreshing")) return;
      refreshingForUpdate = true;
      sessionStorage.setItem("sw-refreshing", "1");
      location.reload();
    });
    navigator.serviceWorker.register("./sw.js").then(reg => {
      reg.update().catch(() => {});
      if (reg.waiting) reg.waiting.postMessage({ type: "SKIP_WAITING" });
      reg.addEventListener("updatefound", () => {
        const worker = reg.installing;
        if (!worker) return;
        worker.addEventListener("statechange", () => {
          if (worker.state === "installed" && navigator.serviceWorker.controller) {
            worker.postMessage({ type: "SKIP_WAITING" });
          }
        });
      });
    }).catch(() => {});
    window.addEventListener("pageshow", () => sessionStorage.removeItem("sw-refreshing"));
  });
}
</script>
</body>
</html>
