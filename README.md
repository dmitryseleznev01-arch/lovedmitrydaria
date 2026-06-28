<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Дмитрий & Дарья | Свадьба 18.07.2026</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', 'Times New Roman', serif;
            background: #faf7f2;
            color: #2c1f14;
            display: flex;
            justify-content: center;
            padding: 30px 15px;
            background-image: radial-gradient(circle at 30% 10%, #f5efe8 0%, #faf7f2 90%);
        }

        .invitation {
            max-width: 820px;
            width: 100%;
            background: #ffffff;
            padding: 45px 40px 50px;
            border-radius: 28px;
            box-shadow: 0 25px 70px rgba(60, 40, 25, 0.13);
            border: 1px solid #e8ddd2;
        }

        /* Декоративные линии */
        .divider {
            width: 80px;
            height: 2px;
            background: #d4b896;
            margin: 20px auto;
            border-radius: 4px;
        }

        .divider-long {
            width: 140px;
            height: 2px;
            background: #e5d5c4;
            margin: 30px auto;
        }

        .divider-gold {
            width: 60px;
            height: 3px;
            background: #c9a87c;
            margin: 16px auto;
            border-radius: 6px;
        }

        /* Заголовки */
        .subtitle {
            font-size: 13px;
            letter-spacing: 5px;
            text-transform: uppercase;
            color: #b2977a;
            text-align: center;
            margin-bottom: 8px;
        }

        h1 {
            font-size: 52px;
            font-weight: 400;
            color: #1f140c;
            text-align: center;
            letter-spacing: 1px;
        }

        .ampersand {
            font-size: 56px;
            color: #c7a67e;
            font-weight: 300;
            display: inline-block;
            margin: 0 12px;
        }

        .names {
            font-size: 40px;
            font-weight: 400;
            color: #1f140c;
            text-align: center;
            letter-spacing: 3px;
        }

        .names-small {
            font-size: 28px;
            font-weight: 400;
            color: #1f140c;
            text-align: center;
            letter-spacing: 2px;
        }

        /* Дата */
        .date-block {
            text-align: center;
            margin: 28px 0 20px;
        }

        .date-block .day {
            font-size: 58px;
            font-weight: 600;
            color: #b49a7a;
            letter-spacing: 2px;
        }

        .date-block .month-year {
            font-size: 28px;
            color: #3e2c1b;
            letter-spacing: 6px;
            font-weight: 300;
        }

        .date-block .day-of-week {
            font-size: 16px;
            color: #b49a7a;
            letter-spacing: 4px;
            text-transform: uppercase;
            margin-top: 4px;
        }

        /* Сетка календаря */
        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 2px;
            max-width: 360px;
            margin: 12px auto 10px;
            font-size: 14px;
            text-align: center;
        }

        .calendar-grid .weekday {
            font-size: 11px;
            text-transform: uppercase;
            color: #b49a7a;
            letter-spacing: 1px;
            padding: 4px 0;
            font-weight: 600;
        }

        .calendar-grid .day-cell {
            padding: 6px 0;
            border-radius: 50%;
            color: #3e2c1b;
            font-size: 14px;
        }

        .calendar-grid .day-cell.active {
            background: #d4b896;
            color: #fff;
            font-weight: 600;
            border-radius: 50%;
        }

        .calendar-grid .day-cell.empty {
            color: #d4c8bc;
        }

        .month-label {
            text-align: center;
            font-size: 18px;
            color: #3e2c1b;
            letter-spacing: 4px;
            font-weight: 400;
            margin-top: 6px;
        }

        /* Карточки */
        .card {
            background: #f9f5ef;
            border-radius: 18px;
            padding: 28px 25px;
            margin: 28px 0;
            border-left: 4px solid #d4b896;
        }

        .card h3 {
            font-size: 22px;
            font-weight: 400;
            color: #1f140c;
            margin-bottom: 12px;
            letter-spacing: 1px;
        }

        .card p {
            font-size: 17px;
            line-height: 1.7;
            color: #3e2c1b;
        }

        .card .icon {
            font-size: 26px;
            margin-right: 10px;
        }

        /* Программа дня */
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 14px;
            margin: 15px 0 5px;
        }

        .timeline-item {
            display: flex;
            align-items: flex-start;
            gap: 18px;
            padding-bottom: 14px;
            border-bottom: 1px solid #eee5db;
        }

        .timeline-item:last-child {
            border-bottom: none;
            padding-bottom: 0;
        }

        .timeline-item .time {
            font-weight: 600;
            color: #b49a7a;
            min-width: 70px;
            font-size: 16px;
        }

        .timeline-item .event {
            font-size: 16px;
            color: #2c1f14;
        }

        .timeline-item .event small {
            display: block;
            font-size: 13px;
            color: #b49a7a;
            font-style: italic;
            margin-top: 2px;
        }

        /* Дресс-код */
        .dress-code {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            justify-content: center;
            margin: 12px 0 6px;
        }

        .dress-code span {
            display: inline-block;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            border: 2px solid #ddd0c0;
        }

        .dress-code .dc-gold { background: #d4b896; }
        .dress-code .dc-cream { background: #f5ede4; }
        .dress-code .dc-green { background: #7d8b71; }
        .dress-code .dc-beige { background: #d9c8b0; }

        /* Таймер */
        .timer {
            display: flex;
            justify-content: center;
            gap: 16px;
            flex-wrap: wrap;
            margin: 18px 0 10px;
        }

        .timer-item {
            text-align: center;
            background: #f9f5ef;
            padding: 12px 22px;
            border-radius: 14px;
            min-width: 70px;
        }

        .timer-item .number {
            font-size: 32px;
            font-weight: 600;
            color: #1f140c;
        }

        .timer-item .label {
            font-size: 11px;
            text-transform: uppercase;
            color: #b49a7a;
            letter-spacing: 1px;
        }

        /* Пожелания */
        .wish-list {
            display: flex;
            flex-direction: column;
            gap: 14px;
            margin: 12px 0 6px;
        }

        .wish-item {
            padding: 12px 18px;
            background: #fcf9f6;
            border-radius: 14px;
            border: 1px solid #ede5db;
            font-size: 16px;
            color: #3e2c1b;
        }

        .wish-item .emoji {
            margin-right: 12px;
        }

        /* Форма (стилизованная) */
        .form-group {
            margin-bottom: 18px;
        }

        .form-group label {
            display: block;
            font-size: 15px;
            font-weight: 500;
            color: #2c1f14;
            margin-bottom: 6px;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 14px 18px;
            border: 1px solid #e0d5c8;
            border-radius: 14px;
            font-size: 16px;
            font-family: 'Georgia', serif;
            background: #fcf9f6;
            transition: 0.3s;
            color: #2c1f14;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            border-color: #d4b896;
            outline: none;
            box-shadow: 0 0 0 3px rgba(212, 184, 150, 0.2);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 80px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 18px;
        }

        .checkbox-group {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 8px;
            margin: 6px 0 8px;
        }

        .checkbox-group label {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 15px;
            font-weight: 400;
            color: #3e2c1b;
            cursor: pointer;
        }

        .checkbox-group input[type="checkbox"] {
            width: 18px;
            height: 18px;
            accent-color: #d4b896;
        }

        .btn-submit {
            background: #d4b896;
            color: #fff;
            border: none;
            padding: 16px 40px;
            font-size: 18px;
            font-weight: 500;
            border-radius: 60px;
            cursor: pointer;
            transition: 0.3s;
            font-family: 'Georgia', serif;
            letter-spacing: 1px;
            width: 100%;
            box-shadow: 0 6px 20px rgba(212, 184, 150, 0.3);
        }

        .btn-submit:hover {
            background: #c4a07a;
            transform: translateY(-2px);
        }

        .btn-submit:active {
            transform: translateY(0);
        }

        .radio-group {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin: 4px 0 10px;
        }

        .radio-group label {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 16px;
            font-weight: 400;
            color: #3e2c1b;
            cursor: pointer;
        }

        .radio-group input[type="radio"] {
            width: 18px;
            height: 18px;
            accent-color: #d4b896;
        }

        /* Футер */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid #ede5db;
        }

        .footer .big-names {
            font-size: 36px;
            letter-spacing: 6px;
            color: #1f140c;
        }

        .footer .big-names span {
            color: #b49a7a;
        }

        .footer .date-footer {
            font-size: 16px;
            color: #b49a7a;
            letter-spacing: 4px;
            margin-top: 6px;
        }

        .footer .see-you {
            font-size: 13px;
            letter-spacing: 4px;
            text-transform: uppercase;
            color: #b49a7a;
            margin-bottom: 10px;
        }

        /* Адаптивность */
        @media (max-width: 640px) {
            .invitation {
                padding: 25px 18px 30px;
            }

            h1 {
                font-size: 32px;
            }

            .names {
                font-size: 28px;
            }

            .names-small {
                font-size: 22px;
            }

            .ampersand {
                font-size: 36px;
                margin: 0 6px;
            }

            .date-block .day {
                font-size: 40px;
            }

            .date-block .month-year {
                font-size: 22px;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .checkbox-group {
                grid-template-columns: 1fr 1fr;
            }

            .timeline-item {
                flex-direction: column;
                gap: 4px;
            }

            .timeline-item .time {
                min-width: auto;
            }

            .timer {
                gap: 10px;
            }

            .timer-item {
                padding: 8px 14px;
                min-width: 60px;
            }

            .timer-item .number {
                font-size: 24px;
            }

            .footer .big-names {
                font-size: 26px;
            }

            .radio-group {
                gap: 12px;
            }
        }

        @media (max-width: 420px) {
            .checkbox-group {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <div class="invitation">

        <!-- ===== Верхняя часть ===== -->
        <div class="subtitle">Свадебное приглашение</div>

        <div style="text-align: center; margin: 6px 0 4px;">
            <span class="names-small">Дмитрий</span>
        </div>
        <div style="text-align: center; font-size: 40px; color: #c7a67e; font-weight: 300; line-height: 1;">&</div>
        <div style="text-align: center; margin: 2px 0 10px;">
            <span class="names-small">Дарья</span>
        </div>

        <div class="divider"></div>

        <!-- ===== Дата ===== -->
        <div class="date-block">
            <div class="day">18</div>
            <div class="month-year">июля 2026</div>
            <div class="day-of-week">Суббота</div>
        </div>

        <div class="divider"></div>

        <!-- ===== Приветствие ===== -->
        <div class="card" style="background: #fcf9f6; border-left-color: #c9a87c;">
            <p style="font-size: 20px; font-style: italic; text-align: center; color: #2c1f14;">
                Дорогие гости, мы приглашаем вас<br>
                <strong>на нашу свадьбу</strong>
            </p>
            <p style="text-align: center; margin-top: 12px; font-size: 16px; color: #5a4030;">
                Вы получили это сообщение, а значит, мы спешим поделиться с вами радостной новостью – у нас скоро свадьба!
            </p>
            <p style="text-align: center; margin-top: 10px; font-size: 16px; color: #5a4030;">
                Мы приглашаем вас разделить с нами радость этого особенного события и стать частью нашей семейной истории. Ваше присутствие сделает наш день еще более значимым и незабываемым.
            </p>
        </div>

        <!-- ===== Календарь ===== -->
        <div style="text-align: center;">
            <div style="font-size: 14px; color: #b49a7a; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 2px;">Дата проведения свадьбы</div>
            <div class="calendar-grid">
                <div class="weekday">Пн</div>
                <div class="weekday">Вт</div>
                <div class="weekday">Ср</div>
                <div class="weekday">Чт</div>
                <div class="weekday">Пт</div>
                <div class="weekday">Сб</div>
                <div class="weekday">Вс</div>

                <div class="day-cell empty">1</div>
                <div class="day-cell empty">2</div>
                <div class="day-cell empty">3</div>
                <div class="day-cell empty">4</div>
                <div class="day-cell empty">5</div>
                <div class="day-cell">6</div>
                <div class="day-cell">7</div>

                <div class="day-cell">8</div>
                <div class="day-cell">9</div>
                <div class="day-cell">10</div>
                <div class="day-cell">11</div>
                <div class="day-cell">12</div>
                <div class="day-cell">13</div>
                <div class="day-cell">14</div>

                <div class="day-cell">15</div>
                <div class="day-cell">16</div>
                <div class="day-cell">17</div>
                <div class="day-cell active">18</div>
                <div class="day-cell">19</div>
                <div class="day-cell">20</div>
                <div class="day-cell">21</div>

                <div class="day-cell">22</div>
                <div class="day-cell">23</div>
                <div class="day-cell">24</div>
                <div class="day-cell">25</div>
                <div class="day-cell">26</div>
                <div class="day-cell">27</div>
                <div class="day-cell">28</div>

                <div class="day-cell">29</div>
                <div class="day-cell">30</div>
                <div class="day-cell">31</div>
                <div class="day-cell empty"></div>
                <div class="day-cell empty"></div>
                <div class="day-cell empty"></div>
                <div class="day-cell empty"></div>
            </div>
            <div class="month-label">Июль</div>
        </div>

        <!-- ===== Место проведения ===== -->
        <div class="card">
            <h3>📍 Место проведения</h3>
            <p><strong>15:30</strong></p>
            <p>Арзамасский район, с. Чернуха, ул. Ленина, д. 53А</p>
            <p style="margin-top: 8px; font-size: 15px; color: #5a4030;">
                Для вашего удобства мы подготовили карту. Надеемся, что вы легко найдете место проведения свадьбы и порадуете нас своим присутствием!
            </p>
        </div>

        <!-- ===== Программа дня ===== -->
        <div class="card">
            <h3>🎉 Программа дня</h3>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="time">12:40</div>
                    <div class="event">
                        Церемония бракосочетания
                        <small>На всякий случай приготовьте платочки для трогательного момента</small>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time">15:30</div>
                    <div class="event">
                        Сбор гостей, фуршет
                        <small>Собираясь на мероприятие, просим взять с собой ваши прекрасные улыбки и хорошее настроение</small>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time">16:00</div>
                    <div class="event">
                        Начало банкета
                        <small>Время вкусной еды, танцев и развлечений</small>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time">21:30</div>
                    <div class="event">
                        Свадебный торт
                        <small>Сладкая традиция, которую мы не можем обойти стороной</small>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time">22:30</div>
                    <div class="event">
                        Фейерверк
                        <small>Незабываемое завершение этого волшебного дня</small>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time">23:00</div>
                    <div class="event">
                        Окончание вечера
                        <small>К сожалению, даже такой прекрасный вечер может закончиться</small>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== Дресс-код ===== -->
        <div class="card" style="text-align: center;">
            <h3>👗 Поддержите наш дресс-код</h3>
            <p>Нам будет очень приятно, если вы поддержите цветовую гамму торжества и выберете наряды в соответствии с цветовой палитрой нашей свадьбы.</p>
            <div class="dress-code">
                <span class="dc-gold"></span>
                <span class="dc-cream"></span>
                <span class="dc-green"></span>
                <span class="dc-beige"></span>
            </div>
        </div>

        <!-- ===== Таймер ===== -->
        <div style="text-align: center; margin: 30px 0 20px;">
            <div style="font-size: 16px; color: #b49a7a; letter-spacing: 2px; text-transform: uppercase;">До свадьбы осталось</div>
            <div class="timer">
                <div class="timer-item"><div class="number">20</div><div class="label">Дней</div></div>
                <div class="timer-item"><div class="number">01</div><div class="label">Часов</div></div>
                <div class="timer-item"><div class="number">08</div><div class="label">Минут</div></div>
                <div class="timer-item"><div class="number">19</div><div class="label">Секунд</div></div>
            </div>
        </div>

        <!-- ===== Пожелания ===== -->
        <div class="card" style="background: #fcf9f6;">
            <h3>💝 Пожелания от всего сердца</h3>
            <p style="font-size: 17px; margin-bottom: 12px;">Этот день станет по-настоящему особенным благодаря вам. Мы собрали для вас несколько тёплых пожеланий.</p>
            <div class="wish-list">
                <div class="wish-item">
                    <span class="emoji">💌</span> Если вы задумались о подарке – самым приятным для нас будет «букет» в конверте. Такой подарок точно не завянет и поможет воплотить наши мечты в жизнь.
                </div>
                <div class="wish-item">
                    <span class="emoji">👶</span> Формат нашего торжества не предполагает детской зоны, и мы хотим, чтобы каждый мог спокойно отдохнуть и повеселиться. Поэтому будем признательны, если мамы и папы оставят деток дома в надёжных руках.
                </div>
                <div class="wish-item">
                    <span class="emoji">💐</span> Цветы – это прекрасно, но, чтобы не переживать за их судьбу после праздника, мы будем рады, если вместо букета вы подарите бутылочку вашего любимого напитка. Это добавит ещё больше тепла нашему вечеру!
                </div>
                <div class="wish-item">
                    <span class="emoji">💋</span> Мы знаем, как сильно эмоции переполняют в этот день, но просим воздержаться от криков «горько», ведь поцелуй – это искренний знак чувств, он не бывает по заказу. Если кто-то не сдержится, будьте готовы пополнить наш семейный бюджет штрафом в размере 1000 рублей. 😊
                </div>
                <div class="wish-item" style="background: #f5ede4; border-color: #d4b896; text-align: center; font-size: 18px;">
                    ❤️ Ваше присутствие – лучший подарок для нас!
                </div>
            </div>
        </div>

        <!-- ===== Форма для гостей ===== -->
        <div class="card" style="background: #fcf9f6; border-left-color: #c9a87c;">
            <h3>📝 Вопросы для гостей</h3>

            <form id="weddingForm">

                <div class="form-group">
                    <label>Введите Ваше имя и фамилию *</label>
                    <input type="text" placeholder="Например: Иван Петров" required>
                </div>

                <div class="form-group">
                    <label>Присутствие *</label>
                    <div class="radio-group">
                        <label><input type="radio" name="attendance" value="yes" checked> Я с удовольствием приду</label>
                        <label><input type="radio" name="attendance" value="no"> К сожалению, не смогу присутствовать</label>
                    </div>
                </div>

                <div class="form-group">
                    <label>Так же уточните Ваши предпочтения в горячих блюдах:</label>
                    <div class="radio-group">
                        <label><input type="radio" name="food" value="meat"> Мясо</label>
                        <label><input type="radio" name="food" value="fish"> Рыба</label>
                    </div>
                </div>

                <div class="form-group">
                    <label>Музыкальные композиции, которые хотели бы услышать на празднике</label>
                    <input type="text" placeholder="Напишите 1-2 песни">
                </div>

                <div class="form-group">
                    <label>Мы хотим, чтобы свадьба прошла весело, поэтому просим Вас выбрать алкоголь, который Вы предпочитаете:</label>
                    <div class="checkbox-group">
                        <label><input type="checkbox"> Шампанское</label>
                        <label><input type="checkbox"> Красное сухое вино</label>
                        <label><input type="checkbox"> Красное полусладкое вино</label>
                        <label><input type="checkbox"> Белое полусладкое вино</label>
                        <label><input type="checkbox"> Белое сухое вино</label>
                        <label><input type="checkbox"> Виски</label>
                        <label><input type="checkbox"> Коньяк</label>
                        <label><input type="checkbox"> Водка</label>
                        <label><input type="checkbox"> Ром</label>
                        <label><input type="checkbox"> Джин</label>
                        <label><input type="checkbox"> Текила</label>
                        <label><input type="checkbox"> Безалкогольные напитки</label>
                    </div>
                </div>

                <button type="submit" class="btn-submit">Отправить</button>
            </form>
        </div>

        <!-- ===== Финал ===== -->
        <div class="footer">
            <div class="see-you">See you soon</div>
            <p style="font-size: 17px; color: #2c1f14; margin: 6px 0 12px;">
                Будем рады видеть вас на нашем празднике
            </p>
            <div class="big-names">
                ДМИТРИЙ <span>&</span> ДАРЬЯ
            </div>
            <div class="date-footer">
                18.07.2026
            </div>
        </div>

    </div>

    <script>
        // Простое сообщение при отправке формы
        document.getElementById('weddingForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Спасибо! Ваш ответ сохранён. Мы ждём вас на свадьбе! ❤️');
            this.reset();
        });
    </script>

</body>
</html>
