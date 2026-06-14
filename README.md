<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kaufvertragsstörungen | Lernportal</title>

  <style>
    :root {
      --bg-1: #f4f7fb;
      --bg-2: #e8eef7;
      --primary: #244c7c;
      --primary-dark: #163252;
      --accent: #f2a541;
      --green: #2f855a;
      --red: #b83232;
      --card: #ffffff;
      --text: #1f2937;
      --muted: #64748b;
      --border: #dbe3ef;
      --shadow: 0 18px 45px rgba(24, 49, 83, 0.14);
      --radius: 24px;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(242, 165, 65, 0.20), transparent 32%),
        linear-gradient(135deg, var(--bg-1), var(--bg-2));
      min-height: 100vh;
    }

    .page {
      width: min(1180px, calc(100% - 32px));
      margin: 0 auto;
      padding: 32px 0 56px;
    }

    header {
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      color: white;
      border-radius: var(--radius);
      padding: 42px;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }

    header::after {
      content: "";
      position: absolute;
      width: 260px;
      height: 260px;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.08);
      right: -80px;
      top: -80px;
    }

    .label {
      display: inline-block;
      background: rgba(255, 255, 255, 0.16);
      border: 1px solid rgba(255, 255, 255, 0.28);
      color: white;
      padding: 8px 14px;
      border-radius: 999px;
      font-size: 0.9rem;
      font-weight: 700;
      margin-bottom: 18px;
    }

    h1 {
      margin: 0;
      font-size: clamp(2rem, 5vw, 4rem);
      line-height: 1.05;
      letter-spacing: -1px;
    }

    .subtitle {
      margin: 18px 0 0;
      max-width: 760px;
      color: #e6eef8;
      font-size: 1.1rem;
      line-height: 1.6;
    }

    .section-title {
      margin: 44px 0 18px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .section-title span {
      width: 42px;
      height: 42px;
      border-radius: 14px;
      background: var(--primary);
      color: white;
      display: grid;
      place-items: center;
      font-weight: 800;
      box-shadow: 0 10px 24px rgba(36, 76, 124, 0.22);
    }

    .section-title h2 {
      margin: 0;
      font-size: 1.55rem;
      color: var(--primary-dark);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .grid.two {
      grid-template-columns: repeat(2, 1fr);
    }

    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 24px;
      box-shadow: 0 12px 30px rgba(24, 49, 83, 0.08);
      display: flex;
      flex-direction: column;
      min-height: 260px;
      transition: transform 0.18s ease, box-shadow 0.18s ease, border-color 0.18s ease;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow);
      border-color: rgba(36, 76, 124, 0.35);
    }

    .number {
      width: 42px;
      height: 42px;
      border-radius: 14px;
      background: #edf4ff;
      color: var(--primary);
      display: grid;
      place-items: center;
      font-weight: 900;
      margin-bottom: 18px;
    }

    .card h3 {
      margin: 0 0 10px;
      font-size: 1.15rem;
      color: var(--primary-dark);
    }

    .card p {
      margin: 0 0 22px;
      color: var(--muted);
      line-height: 1.5;
      font-size: 0.96rem;
    }

    .card .spacer {
      flex: 1;
    }

    .tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 18px;
    }

    .tag {
      font-size: 0.78rem;
      font-weight: 700;
      padding: 6px 10px;
      border-radius: 999px;
      background: #eef6f1;
      color: var(--green);
    }

    .tag.orange {
      background: #fff3df;
      color: #a35e00;
    }

    .tag.red {
      background: #fff0f0;
      color: var(--red);
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      width: 100%;
      text-decoration: none;
      background: var(--primary);
      color: white;
      border-radius: 14px;
      padding: 13px 16px;
      font-weight: 800;
      transition: background 0.18s ease, transform 0.18s ease;
    }

    .button:hover {
      background: var(--primary-dark);
      transform: scale(1.01);
    }

    .button.secondary {
      background: var(--accent);
      color: #2b1a00;
    }

    .button.secondary:hover {
      background: #dd8f25;
    }

    .button.disabled {
      background: #cbd5e1;
      color: #64748b;
      pointer-events: none;
      cursor: not-allowed;
    }

    .info-box {
      margin-top: 28px;
      background: rgba(255, 255, 255, 0.72);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 22px 24px;
      color: var(--muted);
      line-height: 1.55;
    }

    .info-box strong {
      color: var(--primary-dark);
    }

    footer {
      margin-top: 36px;
      text-align: center;
      color: var(--muted);
      font-size: 0.92rem;
    }

    @media (max-width: 980px) {
      .grid {
        grid-template-columns: repeat(2, 1fr);
      }

      header {
        padding: 34px;
      }
    }

    @media (max-width: 640px) {
      .page {
        width: min(100% - 22px, 1180px);
        padding-top: 18px;
      }

      header {
        padding: 28px 22px;
        border-radius: 20px;
      }

      .grid,
      .grid.two {
        grid-template-columns: 1fr;
      }

      .card {
        min-height: auto;
      }
    }
  </style>
</head>

<body>
  <main class="page">

    <header>
      <div class="label">Lernplattform ÖB | Wirtschaftsschule</div>
      <h1>Kaufvertragsstörungen</h1>
      <p class="subtitle">
        Digitale Lernbausteine, Übungsportale und Materialien zur Unterrichtssequenz.
        Die Schülerinnen und Schüler arbeiten sich Schritt für Schritt durch typische
        Störungen beim Kaufvertrag und sichern ihr Wissen mit interaktiven Aufgaben.
      </p>
    </header>

    <section>
      <div class="section-title">
        <span>1</span>
        <h2>Kaufvertragsstörungen</h2>
      </div>

      <div class="grid">

        <article class="card">
          <div class="number">01</div>
          <div class="tag-row">
            <span class="tag">Lernportal</span>
            <span class="tag orange">Einführung</span>
          </div>
          <h3>Einführung: Mangelhafte Lieferung</h3>
          <p>
            Startseite zur Erarbeitung der mangelhaften Lieferung mit Grundlagen,
            Fachbegriffen und ersten Aufgaben.
          </p>
          <div class="spacer"></div>
          <a class="button" href="https://6fd9k54kzb-ux.github.io/HeiSop256.github.io/02_lernportal_mangelhafte_lieferung_ueberarbeitet.html">
            Lernportal öffnen →
          </a>
        </article>

        <article class="card">
          <div class="number">02</div>
          <div class="tag-row">
            <span class="tag">Editor</span>
            <span class="tag orange">Mängelrüge</span>
          </div>
          <h3>Die erste Mängelrüge</h3>
          <p>
            Digitaler Editor zum Verfassen einer ersten Mängelrüge.
            Die Lernenden üben Aufbau, Sprache und fachlich korrekte Forderungen.
          </p>
          <div class="spacer"></div>
          <a class="button" href="https://6fd9k54kzb-ux.github.io/HeiSop256.github.io/04_maengelruege-editor.html">
            Editor öffnen →
          </a>
        </article>

        <article class="card">
          <div class="number">03</div>
          <div class="tag-row">
            <span class="tag">E-Mail-Postfach</span>
            <span class="tag orange">Nacherfüllung</span>
          </div>
          <h3>Mängelrüge und erfolglose Nacherfüllung</h3>
          <p>
            Weiterführung des Falls: Die Nacherfüllung scheitert.
            Die Schülerinnen und Schüler prüfen weitere Rechte des Käufers.
          </p>
          <div class="spacer"></div>
          <a class="button" href="https://6fd9k54kzb-ux.github.io/HeiSop256.github.io/02_email_postfach_maengelruege_aktualisiert_10_06_2026.html">
            Fall öffnen →
          </a>
        </article>

        <article class="card">
          <div class="number">04</div>
          <div class="tag-row">
            <span class="tag">Intranet</span>
            <span class="tag orange">Zahlungsverzug</span>
          </div>
          <h3>Firmen-Intranet zum Zahlungsverzug</h3>
          <p>
            Lernumgebung zur Verkäuferperspektive: fällige Zahlung erkennen,
            Verzugszinsen berechnen und Mahnung vorbereiten.
          </p>
          <div class="spacer"></div>
          <a class="button" href="https://6fd9k54kzb-ux.github.io/Z10-WSH-Kaufvertragsstoerungen/02_zahlungsverzug_02_portal_ueberarbeitet(1).html">
            Intranet öffnen →
          </a>
        </article>

      </div>
    </section>

    <section>
      <div class="section-title">
        <span>2</span>
        <h2>Zugang zum Übungsportal für die 3. Schulaufgabe</h2>
      </div>

      <div class="grid two">

        <article class="card">
          <div class="number">A</div>
          <div class="tag-row">
            <span class="tag">Übungsportal</span>
            <span class="tag orange">3. Schulaufgabe</span>
          </div>
          <h3>Kaufvertragsstörungen</h3>
          <p>
            Übungsbereich zur Wiederholung der zentralen Inhalte:
            mangelhafte Lieferung, Mängelrüge, Nacherfüllung, Rücktritt,
            Minderung und Zahlungsverzug.
          </p>
          <div class="spacer"></div>

          <!-- HIER später den passenden Link einsetzen -->
          <a class="button disabled" href="#" aria-disabled="true">
            Link noch einfügen
          </a>
        </article>

        <article class="card">
          <div class="number">B</div>
          <div class="tag-row">
            <span class="tag">Übungsportal</span>
            <span class="tag orange">3. Schulaufgabe</span>
          </div>
          <h3>Verkaufspreiskalkulation</h3>
          <p>
            Übungsbereich zur Verkaufspreiskalkulation mit wiederholbaren Aufgaben
            zur Vorbereitung auf die Schulaufgabe.
          </p>
          <div class="spacer"></div>

          <!-- HIER später den passenden Link einsetzen -->
          <a class="button disabled" href="#" aria-disabled="true">
            Link noch einfügen
          </a>
        </article>

      </div>
    </section>

    <div class="info-box">
      <strong>Hinweis für GitHub:</strong>
      Diese Datei kann als <strong>index.html</strong> im Hauptverzeichnis des Repositories
      gespeichert werden. Danach ist sie automatisch die Startseite deiner GitHub-Pages-Seite.
      Die beiden grauen Buttons im Bereich „3. Schulaufgabe“ sind Platzhalter und können später
      mit den fertigen Links ersetzt werden.
    </div>

    <footer>
      © Lernportal Kaufvertragsstörungen | Wirtschaftsschule
    </footer>

  </main>
</body>
</html>
