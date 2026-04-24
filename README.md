<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>Памятка игрока · Инсбрукский суд, 1485</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Cormorant+Garamond:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Cormorant Garamond', Garamond, serif;
      background-color: #0D0D0D;
      background-image: radial-gradient(circle at 30% 20%, #403B33 0%, #0a0907 100%);
      min-height: 100vh;
      padding: 1.8rem 1.2rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      color: #403B33;
    }

    .container {
      max-width: 1600px;
      width: 100%;
    }

    .header {
      text-align: center;
      margin-bottom: 2.5rem;
    }

    .header h1 {
      font-family: 'Cinzel', serif;
      font-weight: 600;
      font-size: 2.2rem;
      letter-spacing: 2px;
      color: #D9BFA0;
      text-shadow: 0 4px 12px #000000, 0 0 0 2px #BF8A49;
      word-break: break-word;
    }

    .header .line {
      width: 140px;
      height: 3px;
      background: linear-gradient(90deg, transparent, #BF8A49, #A69677, #BF8A49, transparent);
      margin: 0.8rem auto 0;
    }

    .main-content {
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem;
    }

    .grid-section {
      flex: 3;
      min-width: 280px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.8rem;
    }

    /* БЛОК ЗАМЕТОК */
    .notes-section {
      flex: 1;
      min-width: 260px;
      display: flex;
      flex-direction: column;
      gap: 1.8rem;
    }

    .notes-card {
      background: rgba(166, 150, 119, 0.15);
      backdrop-filter: blur(4px);
      border: 1.5px solid #BF8A49;
      border-radius: 24px;
      padding: 1.6rem 1.4rem;
      box-shadow: 0 12px 28px -8px #000000, inset 0 0 0 1px #A69677;
      color: #D9BFA0;
      transition: box-shadow 0.25s;
      border-left: 6px solid #BF8A49;
    }

    .notes-card:hover {
      box-shadow: 0 18px 32px -8px black, 0 0 0 2px #BF8A49, inset 0 0 0 1px #D9BFA0;
    }

    .notes-title {
      font-family: 'Cinzel', serif;
      font-size: 1.8rem;
      margin-bottom: 1.2rem;
      color: #D9BFA0;
      display: flex;
      align-items: center;
      gap: 8px;
      border-bottom: 1px dashed #BF8A49;
      padding-bottom: 8px;
    }

    .notes-textarea {
      width: 100%;
      min-height: 180px;
      background: rgba(12, 12, 12, 0.7);
      border: 1px solid #A69677;
      border-radius: 16px;
      padding: 1rem;
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.1rem;
      color: #F3E9D2;
      resize: vertical;
      margin-bottom: 1rem;
      line-height: 1.5;
      backdrop-filter: blur(2px);
    }

    .notes-textarea:focus {
      outline: 2px solid #BF8A49;
      border-color: #D9BFA0;
    }

    .notes-buttons {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
      margin-bottom: 10px;
    }

    .notes-btn {
      font-family: 'Cinzel', serif;
      background: #403B33;
      border: 1px solid #BF8A49;
      color: #D9BFA0;
      padding: 8px 16px;
      border-radius: 40px;
      font-weight: 600;
      letter-spacing: 1px;
      cursor: pointer;
      transition: 0.2s;
      box-shadow: 0 2px 5px #00000040;
    }

    .notes-btn:hover {
      background: #BF8A49;
      color: #0D0D0D;
      border-color: #D9BFA0;
    }

    .notes-hint {
      font-size: 0.9rem;
      color: #c0b19a;
      font-style: italic;
      margin-top: 8px;
      display: flex;
      align-items: center;
      gap: 4px;
    }

    /* карточка персонажа (выпадающий список) */
    .character-selector {
      background: rgba(166, 150, 119, 0.15);
      backdrop-filter: blur(4px);
      border: 1.5px solid #BF8A49;
      border-radius: 24px;
      padding: 1.6rem 1.4rem;
      box-shadow: 0 12px 28px -8px #000000, inset 0 0 0 1px #A69677;
      color: #D9BFA0;
      border-left: 6px solid #BF8A49;
    }

    .character-selector select {
      width: 100%;
      padding: 12px;
      font-family: 'Cinzel', serif;
      font-size: 1.1rem;
      background: #1f1c17;
      color: #D9BFA0;
      border: 1px solid #BF8A49;
      border-radius: 16px;
      margin-bottom: 1rem;
      cursor: pointer;
    }

    .character-details {
      font-size: 0.95rem;
      line-height: 1.5;
      max-height: 400px;
      overflow-y: auto;
      padding-right: 6px;
    }

    .character-details p {
      margin-bottom: 6px;
    }

    .character-details strong {
      color: #BF8A49;
      font-family: 'Cinzel', serif;
    }

    .character-details .section-title {
      font-family: 'Cinzel', serif;
      font-size: 1.2rem;
      margin: 14px 0 6px;
      color: #BF8A49;
      border-bottom: 1px solid #A69677;
    }

    .character-details .master-info {
      margin-top: 12px;
      padding: 12px;
      background: rgba(191, 138, 73, 0.12);
      border-radius: 12px;
      border-left: 3px solid #BF8A49;
    }

    .character-details .master-info p {
      margin-bottom: 12px;
      font-style: italic;
      color: #c0b19a;
    }

    .character-details input {
      width: 100%;
      background: transparent;
      border: none;
      border-bottom: 1px dashed #BF8A49;
      font-family: 'Cormorant Garamond', serif;
      font-size: 1rem;
      color: #D9BFA0;
      padding: 4px 0;
      margin-top: 6px;
      margin-bottom: 12px;
      outline: none;
    }

    .character-details input:focus {
      border-bottom-color: #D9BFA0;
    }

    /* блок характеристик с правилами */
    .stats-block {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin: 12px 0;
    }
    
    .stat-item {
      flex: 1;
      min-width: 60px;
    }
    
    .stat-item label {
      display: block;
      font-size: 0.8rem;
      color: #A69677;
      margin-bottom: 4px;
    }
    
    .stat-item input {
      width: 100%;
      text-align: center;
      font-size: 1.2rem;
      font-weight: bold;
      margin: 0;
      padding: 6px 0;
    }
    
    .stats-rules {
      background: rgba(191, 138, 73, 0.08);
      padding: 10px 12px;
      border-radius: 12px;
      margin: 12px 0;
      font-size: 0.9rem;
      border-left: 2px solid #BF8A49;
    }
    
    .stats-rules summary {
      cursor: pointer;
      font-weight: bold;
      color: #D9BFA0;
      display: flex;
      align-items: center;
      gap: 6px;
    }
    
    .stats-rules details[open] summary {
      margin-bottom: 8px;
    }

    /* карточка */
    .card {
      background-color: rgba(217, 191, 160, 0.92);
      backdrop-filter: blur(2px);
      border-radius: 24px;
      padding: 1.6rem 1.3rem 1.5rem;
      box-shadow: 0 15px 30px -6px #000000, inset 0 0 0 1px #A69677;
      transition: all 0.25s ease;
      border-left: 6px solid #BF8A49;
      display: flex;
      flex-direction: column;
      opacity: 0;
      transform: translateY(14px);
      animation: cardFadeIn 0.5s cubic-bezier(0.2, 0.9, 0.3, 1) forwards;
      cursor: pointer;
    }

    .card:nth-child(1) { animation-delay: 0.05s; }
    .card:nth-child(2) { animation-delay: 0.12s; }
    .card:nth-child(3) { animation-delay: 0.19s; }
    .card:nth-child(4) { animation-delay: 0.26s; }
    .card:nth-child(5) { animation-delay: 0.33s; }
    .card:nth-child(6) { animation-delay: 0.40s; }

    @keyframes cardFadeIn {
      0% { opacity: 0; transform: translateY(14px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .card:hover {
      transform: scale(1.02);
      box-shadow: 0 22px 36px -8px #000000, 0 0 0 2px #BF8A49, inset 0 0 0 1px #D9BFA0;
    }

    .card-header {
      display: flex;
      flex-direction: column;
    }

    .icon-title {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 8px;
    }

    .icon-title span {
      font-size: 2.7rem;
      line-height: 1;
      color: #403B33;
    }

    .icon-title h2 {
      font-family: 'Cinzel', serif;
      font-weight: 600;
      font-size: 1.7rem;
      color: #1f1c17;
      letter-spacing: 0.5px;
      border-bottom: 2px dashed #BF8A49;
      padding-bottom: 4px;
    }

    .short-desc {
      font-size: 1.15rem;
      font-weight: 500;
      margin: 0.4rem 0 1rem;
      color: #2f2a22;
      font-style: italic;
    }

    .expand-toggle {
      font-family: 'Cinzel', serif;
      font-size: 0.95rem;
      text-transform: uppercase;
      letter-spacing: 2px;
      color: #403B33;
      background: none;
      border: 1.5px solid #BF8A49;
      border-radius: 40px;
      padding: 0.4rem 1.3rem;
      align-self: flex-start;
      transition: 0.25s;
      background-color: rgba(191, 138, 73, 0.15);
      cursor: pointer;
      font-weight: 700;
      margin-top: 2px;
    }

    .expand-toggle:hover {
      background-color: #BF8A49;
      color: #0D0D0D;
      border-color: #403B33;
    }

    .card-expanded {
      max-height: 0;
      opacity: 0;
      overflow: hidden;
      transition: max-height 0.55s ease-in-out, opacity 0.35s ease, margin 0.25s;
      margin-top: 0;
    }

    .card.expanded .card-expanded {
      max-height: 1600px;
      opacity: 1;
      margin-top: 1.4rem;
    }

    .rule-table {
      width: 100%;
      border-collapse: collapse;
      font-size: 1rem;
      margin-bottom: 1.2rem;
    }

    .rule-table td {
      padding: 8px 6px;
      border-bottom: 1px dotted #a69677b0;
      color: #1f1a14;
    }

    .rule-table tr:last-child td { border-bottom: none; }
    .rule-table td:first-child { font-weight: 700; width: 48%; }

    .badge-group {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin: 10px 0 5px;
    }

    .badge {
      background: #403B33;
      color: #D9BFA0;
      padding: 6px 16px;
      border-radius: 40px;
      font-size: 0.9rem;
      font-weight: 600;
      font-family: 'Cinzel', serif;
      letter-spacing: 0.8px;
      border: 1px solid #BF8A49;
      cursor: pointer;
      transition: 0.2s;
      box-shadow: 0 2px 6px #00000040;
    }

    .badge:hover {
      background: #BF8A49;
      color: #0a0907;
      border-color: #D9BFA0;
    }

    .collapse-btn {
      background: transparent;
      border: 1.5px solid #403B33;
      color: #1f1a14;
      font-family: 'Cinzel', serif;
      font-size: 0.85rem;
      padding: 5px 16px;
      border-radius: 40px;
      cursor: pointer;
      align-self: flex-start;
      margin-top: 8px;
      transition: 0.2s;
      font-weight: 600;
    }

    .collapse-btn:hover {
      background: #403B33;
      color: #D9BFA0;
      border-color: #BF8A49;
    }

    /* попап */
    .popup-overlay {
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background-color: rgba(0,0,0,0.45);
      backdrop-filter: blur(3px);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.25s;
    }

    .popup-overlay.active {
      opacity: 1;
      pointer-events: auto;
    }

    .popup-card {
      background: #D9BFA0;
      max-width: 520px;
      width: 90%;
      max-height: 85vh;
      overflow-y: auto;
      border-radius: 28px;
      box-shadow: 0 40px 60px -10px black, 0 0 0 2px #BF8A49, inset 0 0 0 1px #A69677;
      padding: 2rem 1.6rem;
      color: #0D0D0D;
      position: relative;
      font-family: 'Cormorant Garamond', serif;
      transform: scale(0.9);
      transition: transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
      border-left: 10px solid #403B33;
    }

    .active .popup-card { transform: scale(1); }
    .popup-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;
      font-family: 'Cinzel', serif;
    }
    .popup-header h3 { font-size: 1.8rem; font-weight: 700; color: #1a1510; }
    .popup-close {
      background: none; border: none; font-size: 2.4rem; cursor: pointer;
      color: #403B33; transition: 0.15s; line-height: 1;
    }
    .popup-close:hover { color: #0D0D0D; transform: scale(1.15); }
    .popup-content { font-size: 1.1rem; line-height: 1.5; }
    .popup-content ul, .popup-content ol { padding-left: 1.8rem; margin: 0.8rem 0; }
    .popup-content table { width: 100%; border-collapse: collapse; margin-top: 8px; }
    .popup-content td { padding: 8px 4px; border-bottom: 1px dashed #403B33; }

    .footer {
      text-align: center;
      margin-top: 2.5rem;
      color: #D9BFA0;
      font-size: 1.3rem;
      font-style: italic;
      border-top: 2px solid #BF8A49;
      padding-top: 2rem;
      font-weight: 500;
      text-shadow: 0 2px 5px black;
    }
    .footer span { font-size: 2rem; margin-left: 8px; font-style: normal; }

    /* адаптив */
    @media (max-width: 1100px) {
      .grid { grid-template-columns: repeat(2, 1fr); }
    }
    @media (max-width: 800px) {
      .main-content { flex-direction: column; }
      .grid { grid-template-columns: 1fr; }
      body { padding: 1rem 0.8rem; }
    }

    /* скрытие информации до выбора */
    .character-selector .secret-content {
      display: none;
    }
    .character-selector.has-selection .secret-content {
      display: block;
    }
    .no-selection-message {
      display: block;
    }
    .character-selector.has-selection .no-selection-message {
      display: none;
    }
  </style>
</head>
<body>
<div class="container">
  <div class="header">
    <h1>⚖︎ Памятка игрока<br>«Инсбрукский суд, 1485»</h1>
    <div class="line"></div>
  </div>

  <div class="main-content">
    <!-- Сетка карточек (6 штук) -->
    <div class="grid-section">
      <div class="grid" id="cardGrid"></div>
    </div>

    <!-- Блок с заметками и персонажем -->
    <div class="notes-section">
      <!-- Выбор персонажа -->
      <div class="character-selector" id="charSelectorBlock">
        <div class="notes-title"><span>웃</span> Твой персонаж</div>
        <select id="charSelect">
          <option value="">— Выбери архетип —</option>
          <option value="inquisitor">Инквизитор Генрих Крамер</option>
          <option value="defender">Защитник Иоганн Мерварт</option>
          <option value="representative">Представитель эрцгерцога</option>
          <option value="councillor">Городской советник</option>
          <option value="priest">Местный священник</option>
          <option value="medic">Итальянский лекарь</option>
          <option value="tavern">Тавернщик</option>
          <option value="patron">Богатый покровитель</option>
          <option value="crafter">Ремесленник (мастер цеха)</option>
          <option value="helena">Хелена Шоберин (обвиняемая)</option>
          <option value="barbel">Бербель Хиффайзен (обвиняемая)</option>
          <option value="margareta">Маргарета Грюнепахин (свидетель)</option>
          <option value="judge">Судья</option>
        </select>
        <div class="character-details" id="charDetails">
          <p class="no-selection-message" style="opacity:0.7; font-style:italic;">Выбери персонажа, чтобы увидеть его базовые характеристики.</p>
        </div>
        <div style="margin-top:12px;">
          <button class="notes-btn" id="saveCharBtn" style="width:100%;">📥︎ Сохранить персонажа</button>
        </div>
      </div>

      <!-- Заметки -->
      <div class="notes-card">
        <div class="notes-title"><span>✎</span> Мои заметки</div>
        <textarea id="playerNotes" class="notes-textarea" placeholder="Здесь можно записать свои цели, подозрения, план действий на суд, важные улики или слухи..."></textarea>
        <div class="notes-buttons">
          <button class="notes-btn" id="saveNotesBtn">📥︎ Сохранить</button>
          <button class="notes-btn" id="clearNotesBtn">⛌ Очистить</button>
        </div>
        <div class="notes-hint">
          <span>🔓︎</span> Заметки сохраняются только в этом браузере и на этом устройстве.
        </div>
      </div>
    </div>
  </div>

  <div class="footer">
    «Слова имеют вес. Слухи решают судьбы. Истина — в твоих руках.» <span>⚖︎</span>
  </div>
</div>

<!-- Мини-попап -->
<div class="popup-overlay" id="popupOverlay">
  <div class="popup-card" id="popupCard">
    <div class="popup-header">
      <h3 id="popupTitle">📜 Заголовок</h3>
      <button class="popup-close" id="popupCloseBtn">&times;</button>
    </div>
    <div class="popup-content" id="popupContent">…</div>
  </div>
</div>

<script>
  (function(){
    // ---------- ДАННЫЕ 6 КАРТОЧЕК ДЛЯ ИГРОКА ----------
    const cardsData = [
      { // 0: Твой персонаж
        icon: '웃', title: 'Твой персонаж',
        short: 'Личная цель, секрет, деньги, влияние и репутация.',
        table: [
          ['Личная цель','Написана в твоей карточке — стремись к ней любыми средствами.'],
          ['Секрет','Скрывай от других — это твоё оружие. Раскрытие может стоить репутации или жизни.'],
          ['Деньги (пфенниги)','Можно тратить на слухи, улики, подкуп, наём свидетеля.'],
          ['Влияние (3–8)','Насколько к твоим словам прислушиваются. Чем выше — тем весомее голос.'],
          ['Репутация (начинается с 10)','Твоё доброе имя. Если упадёт до 0 — тебя никто не слушает, в суде твои слова игнорируют.']
        ],
        badges: [
          { label: '↓ Как теряется репутация', popupTitle: 'Потеря репутации', 
            content: '<ul><li>Публичное разоблачение лжи — 2d4</li><li>Противоречие самому себе — 1d6</li><li>Кража (поймали) — 1d6</li><li>Проигрыш в состязании с важным лицом — 1d4 (тет-а-тет) / 2d4 (прилюдно)</li></ul>' },
          { label: '↑ Как восстановить', popupTitle: 'Восстановление репутации', 
            content: '<ul><li>Совершить публичный благородный поступок — 1d4</li><li>Оказать услугу влиятельному лицу — по решению Мастера</li><li>Доказать свою правоту в суде — может восстановить до 2d4</li></ul>' },
          { label: '✧ Использовать влияние', popupTitle: 'Как использовать влияние', 
            content: '<p>При высоком влиянии (6-8) ты можешь:<br>• Требовать документы у чиновников<br>• Поручиться за другого персонажа<br>• Влиять на мнение судьи<br>• Защищать свидетелей от запугивания</p><p>При низком влиянии (3-4) — ищи союзников, передавай информацию тем, кого слушают.</p>' }
        ]
      },
      { // 1: Броски и навыки
        icon: '☼', title: 'Броски и навыки',
        short: 'Как бросать кубики, модификаторы, преимущество и помеха.',
        table: [
          ['Проверка','1d20 + модификатор + 2 (если это твой навык)'],
          ['Состязание','Оба бросают d20, побеждает больший результат'],
          ['Преимущество','Бросай дважды, бери лучший (есть поддержка, доказательства)'],
          ['Помеха','Бросай дважды, бери худший (спешка, клевета, плохая репутация)']
        ],
        badges: [
          { label: '⁝⁝ Таблица модификаторов', popupTitle: 'Модификаторы характеристик', 
            content: '<table><tr><td>1-3</td><td>-3</td></tr><tr><td>4-5</td><td>-2</td></tr><tr><td>6-7</td><td>-1</td></tr><tr><td>8-12</td><td>0</td></tr><tr><td>13-14</td><td>+1</td></tr><tr><td>15-16</td><td>+2</td></tr><tr><td>17-18</td><td>+3</td></tr><tr><td>19-20</td><td>+4</td></tr></table>' },
          { label: '⚙︎ Твои навыки', popupTitle: 'Примеры навыков', 
            content: '<ul><li>Красноречие (CHA) — убеждать</li><li>Обман (CHA) — лгать</li><li>Знание законов (INT) — понимать процедуры</li><li>Проницательность (WIS) — видеть ложь</li><li>Внимательность (WIS) — находить улики</li><li>Скрытность (DEX) — красть, тайно передавать</li><li>Запугивание (STR/CHA) — давить</li></ul>' },
          { label: '✦ Вдохновение', popupTitle: 'Что такое вдохновение', 
            content: '<p>Мастер даёт вдохновение за яркий отыгрыш, драматический риск или верность характеру. Можно потратить, чтобы получить преимущество на один бросок. Не накапливается бесконечно — используй в ключевой момент!</p>' }
        ]
      },
      { // 2: Слухи
        icon: '👂︎', title: 'Слухи',
        short: 'Как распускать, проверять, продавать слухи и что бывает за ложь.',
        table: [
          ['Разыграть слух','Харизма (Убеждение), СЛ 12. Успех — слух идёт в народ.'],
          ['Проверить слух','Интеллект или Мудрость, СЛ 12. Мастер скажет: правда, ложь, искажение.'],
          ['Продать слух','3 пфеннига (если ещё не разыгран). Харизма СЛ 10–15.'],
          ['Передать слух','Отдай карточку другому игроку — он сможет разыграть её как свою.'],
          ['Украсть карточку','Ловкость (Скрытность) против Мудрости цели. Провал — потеря 1d6 репутации.']
        ],
        badges: [
          { label: '⛌ Крит. провал (1)', popupTitle: 'Критический провал слуха', 
            content: '<p>Потеря 1d4 репутации, слух не распространяется. Над тобой могут посмеяться в городе.</p>' },
          { label: '⊘ Поймали на лжи', popupTitle: 'Последствия лжи', 
            content: '<p>Если ложь доказана — потеря 1d6 репутации + помеха на все проверки Харизмы до конца игры. Твоему слову больше не верят.</p>' },
          { label: '❗︎ Важно!', popupTitle: 'Правила слухов', 
            content: '<p>• Слух разыгрывается один раз — не повторяй его.<br>• Никому не показывай свою карточку слуха!<br>• Проверить твои слова можно, только получив доступ к карточке или проведя расследование.</p>' }
        ]
      },
      { // 3: Улики
        icon: '⌕', title: 'Улики',
        short: 'Как находить, использовать в суде, красть и подделывать.',
        table: [
          ['Найти улику','Опиши где ищешь, бросок Мудрости (Внимательность) или Интеллекта (Анализ). СЛ 5–20.'],
          ['Предъявить в суде','Назови улику и объясни, что она доказывает. Судья примет к рассмотрению.'],
          ['Украсть улику','Ловкость (Скрытность) против Мудрости цели. Провал — потеря 1d6 репутации.'],
          ['Подделать улику','Интеллект (Обман или Анализ), СЛ 15. Работает как косвенная улика.'],
          ['Уничтожить','Если есть физический доступ. Если узнают — потеря 1d6 репутации.']
        ],
        badges: [
          { label: '⚖︎ Виды улик', popupTitle: 'Сила улик в суде', 
            content: '<ul><li><strong>Косвенная</strong> — +1 к проверке Харизмы (странный порошок, слухи).</li><li><strong>Прямая</strong> — +2 к Харизме, сильно склоняет судью (восковая фигура, письмо).</li><li><strong>Опровергающая</strong> — отменяет одну прямую улику противника (показания гончара о подбросе).</li></ul>' },
          { label: '⌕ Где искать', popupTitle: 'Локации для поиска улик', 
            content: '<p>Под порогом, в подушке, в канцелярии, в тюрьме, у свидетелей, в доме инквизитора, в церковных книгах, в таверне.</p>' },
          { label: '✧ Совет', popupTitle: 'Тактика с уликами', 
            content: '<p>Прибереги опровергающую улику для ответа на самый сильный аргумент противника. Не выкладывай все козыри сразу — оставь что-то для прений.</p>' }
        ]
      },
      { // 4: Твой козырь
        icon: '♧', title: 'Твой козырь',
        short: 'Уникальная способность — один раз за игру, без броска.',
        table: [
          ['Как использовать','1. Зачитай вариант из карточки козыря. 2. Опиши действие. 3. Мастер объявляет результат.'],
          ['Срабатывает','Автоматически, бросок не нужен. Но ситуация должна соответствовать описанию козыря.'],
          ['Материальный козырь','Если у тебя папская булла, письмо, документ — его можно украсть. Будь осторожен!']
        ],
        badges: [
          { label: '⎗ Примеры козырей', popupTitle: 'Козыри архетипов', 
            content: '<ul><li><strong>Инквизитор</strong> — папская булла (арест, отвод судьи)</li><li><strong>Защитник</strong> — финансовая поддержка (до 10 пф)</li><li><strong>Обвиняемые</strong> — тайны знати/соседей (шантаж)</li><li><strong>Судья</strong> — отклонить аргумент</li><li><strong>Лекарь</strong> — медицинское заключение</li></ul>' },
          { label: '🔓︎ Если козырь украли', popupTitle: 'Потеря козыря', 
            content: '<p>Если твой материальный козырь украли — ты теряешь возможность его использовать. Компенсации нет. Храни важные документы при себе или у надежного союзника.</p>' },
          { label: '✧ Когда использовать', popupTitle: 'Тактика козыря', 
            content: '<p>Используй в критический момент:<br>• Когда судья колеблется<br>• Чтобы переломить ход допроса<br>• Для спасения от ложного обвинения<br>Не откладывай на «потом» — неиспользованный козырь сгорает в конце игры.</p>' }
        ]
      },
      { // 5: Деньги и суд
        icon: '$', title: 'Деньги и суд',
        short: 'Цены, порядок суда, золотые правила.',
        table: [
          ['Купить слух','3 пфеннига'],
          ['Купить улику','3–15 пф (в зависимости от важности)'],
          ['Нанять глашатая','4 пф — распространит слух за тебя'],
          ['Нанять свидетеля','3–5 пф — даст нужные показания'],
          ['Подкупить стражника','1–2 пф — пропустит, передаст записку'],
          ['Доступ к документам','1–3 пф — копия протокола или записи']
        ],
        badges: [
          { label: '⚖︎ Порядок суда', popupTitle: 'Как проходит суд', 
            content: '<ol><li>Открытие — судья объявляет обвиняемых</li><li>Слово обвинителю (3-5 мин)</li><li>Слово защитнику (3-5 мин)</li><li>Допрос свидетелей — вызывай своих!</li><li>Прения — итоговые речи (2-3 мин)</li><li>Приговор</li></ol><p>Не перебивай, жди своей очереди. Если судья говорит «Соблюдайте порядок» — слушайся.</p>' },
          { label: '♔ Три золотых правила', popupTitle: 'Правила игрока', 
            content: '<p><strong>1. Слова имеют вес.</strong> Сказанное вслух может стать слухом и повлиять на суд. Ложь опасна — могут поймать.</p><p><strong>2. Используй свои секреты.</strong> Ты знаешь то, чего не знают другие. Это твоё оружие для шантажа и союзов.</p><p><strong>3. Действуй в образе.</strong> Чем ярче отыгрыш, тем интереснее игра и больше шансов получить вдохновение.</p>' },
          { label: '✧ Что говорить в суде', popupTitle: 'Подготовка к суду', 
            content: '<p>• Готовь речь заранее — запиши 2-3 ключевых аргумента.<br>• Ссылайся на конкретные улики и свидетельства.<br>• Указывай на процедурные нарушения инквизитора.<br>• Апеллируй к авторитету епископа, эрцгерцога, городского совета.<br>• Если ты обвиняемый — держись уверенно, отрицай всё, требуй доказательств.</p>' }
        ]
      }
    ];

    // ---------- ДАННЫЕ ПЕРСОНАЖЕЙ (базовая информация) ----------
    const characters = {
      inquisitor: {
        name: 'Инквизитор Генрих Крамер',
        role: 'Обвинитель, главный антагонист',
        influence: 8,
        money: '7 пфеннигов',
        stats: { int: 15, wis: 12, cha: 15, dex: 10 },
        skills: 'Богословие, Знание законов, Красноречие',
        resource: 'Папская булла «Summis desiderantes affectibus» (копия)',
        publicInfo: 'Доминиканский инквизитор, присланный папой. Убеждены, что ведьмы существуют и их надо искоренять. Уже провели процессы в других городах.'
      },
      defender: {
        name: 'Защитник Иоганн Мерварт',
        role: 'Защитник обвиняемых',
        influence: 6,
        money: '5 пфеннигов (плюс доступ к средствам покровителя)',
        stats: { int: 16, wis: 13, cha: 14, dex: 9 },
        skills: 'Знание законов, Красноречие, Проницательность',
        resource: 'Письмо от семей обвиняемых, копии показаний',
        publicInfo: 'Лиценциат канонического права, доктор медицины. Назначены защищать обвиняемых.'
      },
      representative: {
        name: 'Представитель эрцгерцога Сигизмунда',
        role: 'Наблюдатель, защитник политической стабильности',
        influence: 7,
        money: '10 пфеннигов',
        stats: { int: 14, wis: 12, cha: 16, dex: 10 },
        skills: 'Связи в городе, Проницательность, Красноречие',
        resource: 'Доступ к информации о придворных интригах',
        publicInfo: 'Придворный, посланный эрцгерцогом следить за порядком.'
      },
      councillor: {
        name: 'Городской советник',
        role: 'Представитель городского самоуправления',
        influence: 6,
        money: '10 пфеннигов',
        stats: { int: 14, wis: 13, cha: 14, dex: 11 },
        skills: 'Знание законов, Связи в городе, Проницательность',
        resource: 'Доступ к городским документам',
        publicInfo: 'Член городского совета, заботитесь о порядке и стабильности.'
      },
      priest: {
        name: 'Местный священник',
        role: 'Церковный авторитет, противник радикальных методов',
        influence: 5,
        money: '5 пфеннигов',
        stats: { int: 13, wis: 16, cha: 13, dex: 10 },
        skills: 'Богословие, Проницательность, Красноречие',
        resource: 'Доступ к церковным документам',
        publicInfo: 'Приходской священник, знающий свою паству.'
      },
      medic: {
        name: 'Итальянский лекарь',
        role: 'Медицинский эксперт',
        influence: 4,
        money: '5 пфеннигов',
        stats: { int: 15, wis: 16, cha: 10, dex: 11 },
        skills: 'Медицина, Проницательность, Внимательность',
        resource: 'Набор трав, связи при дворе, знание ядов',
        publicInfo: 'Вы прибыли из Италии - родины лучших врачей Европы. Учились в Падуе или Болонье. Вас пригласили ко двору эрцгерцога. Когда рыцарь Йорг Шписс тяжело заболел, вас позвали к его постели.'
      },
      tavern: {
        name: 'Тавернщик',
        role: 'Источник слухов и информации',
        influence: 4,
        money: '5 пфеннигов',
        stats: { int: 12, wis: 13, cha: 16, dex: 11 },
        skills: 'Связи в городе, Проницательность, Скрытность',
        resource: 'Знание слухов, доступ к информации',
        publicInfo: 'Владелец таверны «Золотой крест», куда заходят все горожане.'
      },
      patron: {
        name: 'Богатый покровитель Ульрих фон Шландерсберг',
        role: 'Придворный, тайный покровитель защиты',
        influence: 7,
        money: '10 пфеннигов',
        stats: { int: 14, wis: 12, cha: 16, dex: 10 },
        skills: 'Связи в городе, Проницательность, Красноречие',
        resource: 'Доступ к эрцгерцогу, финансовая поддержка защитника',
        publicInfo: 'Влиятельный придворный из окружения эрцгерцога Сигизмунда. При дворе вас знают как надёжного советника.'
      },
      crafter: {
        name: 'Ремесленник (мастер цеха)',
        role: 'Представитель горожан',
        influence: 5,
        money: '3 пфеннига',
        stats: { int: 12, wis: 14, cha: 13, dex: 13 },
        skills: 'Связи в городе, Запугивание, Проницательность',
        resource: 'Поддержка цеха',
        publicInfo: 'Уважаемый мастер, владелец мастерской.'
      },
      helena: {
        name: 'Хелена Шоберин',
        role: 'Главная обвиняемая',
        influence: 3,
        money: '2 пфеннига',
        stats: { int: 12, wis: 14, cha: 16, dex: 10 },
        skills: 'Обман, Проницательность, Связи в городе',
        resource: 'Знание компромата на богатых горожан',
        publicInfo: 'Горожанка, замужем. Обвиняетесь в убийстве рыцаря Йорга Шписса и неуважении к инквизитору. О вас ходят самые разные слухи - одни считают вас ведьмой, другие - жертвой клеветы.'
      },
      barbel: {
        name: 'Бербель Хиффайзен',
        role: 'Обвиняемая, травница',
        influence: 3,
        money: '2 пфеннига',
        stats: { int: 13, wis: 15, cha: 13, dex: 11 },
        skills: 'Медицина, Обман, Проницательность',
        resource: 'Знание народной медицины',
        publicInfo: 'Молодая женщина, травница. Обвиняетесь в том, что учили других колдовству. Вы не ведьма, вы просто помогаете людям травами.'
      },
      margareta: {
        name: 'Маргарета Грюнепахин',
        role: 'Ключевой свидетель против Бербель',
        influence: 4,
        money: '3 пфеннига',
        stats: { int: 12, wis: 14, cha: 14, dex: 12 },
        skills: 'Обман, Проницательность, Скрытность',
        resource: 'Личная история болезни',
        publicInfo: 'Жительница Инсбрука, бывшая служанка Бербель Хиффайзен.'
      },
      judge: {
        name: 'Судья',
        role: 'Председатель суда, арбитр',
        influence: 8,
        money: '8 пфеннигов',
        stats: { int: 15, wis: 15, cha: 13, dex: 9 },
        skills: 'Знание законов, Проницательность, Красноречие',
        resource: 'Право выносить окончательное решение',
        publicInfo: 'Уважаемый человек, назначенный вести это дело. Ваша задача - справедливый суд.'
      }
    };

    const grid = document.getElementById('cardGrid');
    const popupOverlay = document.getElementById('popupOverlay');
    const popupTitle = document.getElementById('popupTitle');
    const popupContent = document.getElementById('popupContent');
    const popupCloseBtn = document.getElementById('popupCloseBtn');

    function renderCards() {
      let html = '';
      cardsData.forEach((card, idx) => {
        html += `
          <div class="card" data-card-index="${idx}">
            <div class="card-header">
              <div class="icon-title">
                <span>${card.icon}</span>
                <h2>${card.title}</h2>
              </div>
              <div class="short-desc">${card.short}</div>
              <div class="expand-toggle" data-action="expand">▼ Развернуть</div>
            </div>
            <div class="card-expanded">
              <table class="rule-table">
                ${card.table.map(row => `<tr><td>${row[0]}</td><td>${row[1]}</td></tr>`).join('')}
              </table>
              <div class="badge-group">
                ${card.badges.map((b, i) => 
                  `<span class="badge" data-badge-index="${i}" data-card="${idx}">${b.label}</span>`
                ).join('')}
              </div>
              <button class="collapse-btn" data-action="collapse">▲ Свернуть</button>
            </div>
          </div>
        `;
      });
      grid.innerHTML = html;
    }
    renderCards();

    grid.addEventListener('click', (e) => {
      const card = e.target.closest('.card');
      if (!card) return;
      const expandBtn = e.target.closest('[data-action="expand"]');
      const collapseBtn = e.target.closest('[data-action="collapse"]');
      
      if (expandBtn && !card.classList.contains('expanded')) {
        document.querySelectorAll('.card.expanded').forEach(c => c.classList.remove('expanded'));
        card.classList.add('expanded');
        e.stopPropagation();
        return;
      }
      if (collapseBtn) {
        card.classList.remove('expanded');
        e.stopPropagation();
        return;
      }
      const badge = e.target.closest('.badge');
      if (badge) {
        e.stopPropagation();
        const cardIdx = badge.dataset.card;
        const badgeIdx = badge.dataset.badgeIndex;
        if (cardIdx !== undefined && badgeIdx !== undefined) {
          const badgeData = cardsData[cardIdx].badges[badgeIdx];
          openPopup(badgeData.popupTitle, badgeData.content);
        }
        return;
      }
      if (!card.classList.contains('expanded')) {
        document.querySelectorAll('.card.expanded').forEach(c => c.classList.remove('expanded'));
        card.classList.add('expanded');
      }
    });

    function openPopup(title, content) {
      popupTitle.innerHTML = title;
      popupContent.innerHTML = content;
      popupOverlay.classList.add('active');
    }
    function closePopup() { popupOverlay.classList.remove('active'); }
    popupCloseBtn.addEventListener('click', closePopup);
    popupOverlay.addEventListener('click', (e) => { if (e.target === popupOverlay) closePopup(); });
    document.addEventListener('keydown', (e) => { if (e.key === 'Escape') closePopup(); });
    document.querySelector('.popup-card').addEventListener('click', (e) => e.stopPropagation());

    // ---------- ЛОГИКА ЗАМЕТОК (localStorage) ----------
    const notesTextarea = document.getElementById('playerNotes');
    const saveBtn = document.getElementById('saveNotesBtn');
    const clearBtn = document.getElementById('clearNotesBtn');
    const STORAGE_KEY = 'insbrukPlayerNotes';

    function loadNotes() {
      const saved = localStorage.getItem(STORAGE_KEY);
      if (saved !== null) {
        notesTextarea.value = saved;
      }
    }

    function saveNotes() {
      localStorage.setItem(STORAGE_KEY, notesTextarea.value);
      alert('✓ Заметки сохранены в этом браузере');
    }

    function clearNotes() {
      if (confirm('Удалить все заметки?')) {
        notesTextarea.value = '';
        localStorage.removeItem(STORAGE_KEY);
      }
    }

    saveBtn.addEventListener('click', saveNotes);
    clearBtn.addEventListener('click', clearNotes);
    loadNotes();

    // ---------- ЛОГИКА ПЕРСОНАЖА ----------
    const charSelect = document.getElementById('charSelect');
    const charDetails = document.getElementById('charDetails');
    const saveCharBtn = document.getElementById('saveCharBtn');
    const charSelectorBlock = document.getElementById('charSelectorBlock');
    const CHAR_STORAGE_KEY = 'insbrukSelectedCharacterV3';
    const CHAR_FIELDS_KEY = 'insbrukCharacterFieldsV3';
    const CHAR_STATS_KEY = 'insbrukCharacterStatsV3';

    function loadFields() {
      const savedFields = localStorage.getItem(CHAR_FIELDS_KEY);
      if (savedFields) return JSON.parse(savedFields);
      return {};
    }

    function saveFields(fields) {
      localStorage.setItem(CHAR_FIELDS_KEY, JSON.stringify(fields));
    }

    function loadStats() {
      const savedStats = localStorage.getItem(CHAR_STATS_KEY);
      if (savedStats) return JSON.parse(savedStats);
      return {};
    }

    function saveStats(stats) {
      localStorage.setItem(CHAR_STATS_KEY, JSON.stringify(stats));
    }

    function displayCharacter(charKey) {
      if (!charKey || !characters[charKey]) {
        charSelectorBlock.classList.remove('has-selection');
        charDetails.innerHTML = '<p class="no-selection-message" style="opacity:0.7; font-style:italic;">Выбери персонажа, чтобы увидеть его базовые характеристики.</p>';
        return;
      }
      charSelectorBlock.classList.add('has-selection');
      const c = characters[charKey];
      const savedFields = loadFields();
      const savedStats = loadStats();
      
      // используем сохранённые статы или рекомендуемые
      const stats = savedStats[charKey] || c.stats;
      
      let html = `
        <p><strong>${c.name}</strong></p>
        <p><strong>Роль:</strong> ${c.role}</p>
        <p><strong>Влияние:</strong> ${c.influence} &nbsp;|&nbsp; <strong>Деньги:</strong> ${c.money}</p>
        
        <div class="section-title">
          <span>⚑ Характеристики</span>
        </div>
        <div class="stats-rules">
          <details>
            <summary><span>⚑</span> Правила распределения</summary>
            <p style="margin-top:8px;">У вас есть 20 очков (или 15, в зависимости от архетипа) для распределения между четырьмя характеристиками: Интеллект (INT), Мудрость (WIS), Харизма (CHA), Ловкость (DEX). Начальное значение каждой — 8. Вы можете повысить характеристики, тратя очки.</p>
            <p>Модификатор характеристики = (Значение - 10) / 2 (округление вниз). Чем выше модификатор, тем лучше вы справляетесь с задачами, связанными с этой характеристикой.</p>
          </details>
        </div>
        <div class="stats-block">
          <div class="stat-item">
            <label>INT (Интеллект)</label>
            <input type="number" id="statInt" min="8" max="20" value="${stats.int}" step="1">
          </div>
          <div class="stat-item">
            <label>WIS (Мудрость)</label>
            <input type="number" id="statWis" min="8" max="20" value="${stats.wis}" step="1">
          </div>
          <div class="stat-item">
            <label>CHA (Харизма)</label>
            <input type="number" id="statCha" min="8" max="20" value="${stats.cha}" step="1">
          </div>
          <div class="stat-item">
            <label>DEX (Ловкость)</label>
            <input type="number" id="statDex" min="8" max="20" value="${stats.dex}" step="1">
          </div>
        </div>
        
        <p><strong>Рекомендуемые навыки:</strong> ${c.skills}</p>
        <div class="section-title">Особый ресурс</div>
        <p>${c.resource}</p>
        <div class="section-title">Публичная информация</div>
        <p>${c.publicInfo}</p>
        <div class="secret-content">
          <div class="master-info">
            <p><strong>⚔︎ Информация от Мастера</strong><br><em>После выбора персонажа Мастер выдаст тебе карточку со скрытой целью, секретом, козырем и слабостью. Запиши их в поля ниже, чтобы не забыть.</em></p>
          </div>
          <div class="section-title">⚔︎ Скрытая цель</div>
          <input type="text" id="fieldGoal" placeholder="Впиши полученную от Мастера цель..." value="${savedFields.goal || ''}">
          <div class="section-title">⚔︎ Секрет</div>
          <input type="text" id="fieldSecret" placeholder="Впиши полученный от Мастера секрет..." value="${savedFields.secret || ''}">
          <div class="section-title">⚔︎ Козырь</div>
          <input type="text" id="fieldKozir" placeholder="Впиши полученный от Мастера козырь..." value="${savedFields.kozir || ''}">
          <div class="section-title">⚔︎ Слабость</div>
          <input type="text" id="fieldWeakness" placeholder="Впиши полученную от Мастера слабость..." value="${savedFields.weakness || ''}">
        </div>
        <div style="margin-top: 20px;">
          <p><strong>✎ Черта характера:</strong></p>
          <input type="text" id="fieldTrait" placeholder="Опиши характер..." value="${savedFields.trait || ''}">
          <p><strong>✎ Идеал:</strong></p>
          <input type="text" id="fieldIdeal" placeholder="Во что верит персонаж..." value="${savedFields.ideal || ''}">
          <p><strong>✎ Привязанность:</strong></p>
          <input type="text" id="fieldBond" placeholder="Что дорого персонажу..." value="${savedFields.bond || ''}">
        </div>
      `;
      charDetails.innerHTML = html;

      const fieldGoal = document.getElementById('fieldGoal');
      const fieldSecret = document.getElementById('fieldSecret');
      const fieldKozir = document.getElementById('fieldKozir');
      const fieldWeakness = document.getElementById('fieldWeakness');
      const fieldTrait = document.getElementById('fieldTrait');
      const fieldIdeal = document.getElementById('fieldIdeal');
      const fieldBond = document.getElementById('fieldBond');
      const statInt = document.getElementById('statInt');
      const statWis = document.getElementById('statWis');
      const statCha = document.getElementById('statCha');
      const statDex = document.getElementById('statDex');
      
      const autoSaveFields = () => {
        const fields = {
          goal: fieldGoal?.value || '',
          secret: fieldSecret?.value || '',
          kozir: fieldKozir?.value || '',
          weakness: fieldWeakness?.value || '',
          trait: fieldTrait?.value || '',
          ideal: fieldIdeal?.value || '',
          bond: fieldBond?.value || ''
        };
        saveFields(fields);
      };
      
      const autoSaveStats = () => {
        const allStats = loadStats();
        allStats[charKey] = {
          int: parseInt(statInt?.value) || 8,
          wis: parseInt(statWis?.value) || 8,
          cha: parseInt(statCha?.value) || 8,
          dex: parseInt(statDex?.value) || 8
        };
        saveStats(allStats);
      };
      
      fieldGoal?.addEventListener('input', autoSaveFields);
      fieldSecret?.addEventListener('input', autoSaveFields);
      fieldKozir?.addEventListener('input', autoSaveFields);
      fieldWeakness?.addEventListener('input', autoSaveFields);
      fieldTrait?.addEventListener('input', autoSaveFields);
      fieldIdeal?.addEventListener('input', autoSaveFields);
      fieldBond?.addEventListener('input', autoSaveFields);
      
      statInt?.addEventListener('input', autoSaveStats);
      statWis?.addEventListener('input', autoSaveStats);
      statCha?.addEventListener('input', autoSaveStats);
      statDex?.addEventListener('input', autoSaveStats);
    }

    function loadCharacter() {
      const savedChar = localStorage.getItem(CHAR_STORAGE_KEY);
      if (savedChar && characters[savedChar]) {
        charSelect.value = savedChar;
        displayCharacter(savedChar);
      }
    }

    function saveCharacter() {
      const selected = charSelect.value;
      if (!selected) {
        alert('Сначала выбери персонажа!');
        return;
      }
      localStorage.setItem(CHAR_STORAGE_KEY, selected);
      alert('✓ Персонаж сохранён в этом браузере');
    }

    charSelect.addEventListener('change', (e) => {
      displayCharacter(e.target.value);
    });

    saveCharBtn.addEventListener('click', saveCharacter);

    loadCharacter();
  })();
</script>
</body>
</html>
