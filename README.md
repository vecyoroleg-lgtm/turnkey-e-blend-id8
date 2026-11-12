# TurnKey E Blend for iDrive 8

Український калькулятор доливу бензину й E85 до повного бака. Введи місткість і залишок у літрах, поточну концентрацію етанолу, склад обох видів пального та цільовий відсоток. Розрахунок використовує введені вручну дані.

## Встановлення

У MGU Store відкрий **Settings → Add source**, введи `vecyoroleg-lgtm/turnkey-e-blend-id8` і вибери **Releases**. Можна також додати адресу [catalog.json](https://raw.githubusercontent.com/vecyoroleg-lgtm/turnkey-e-blend-id8/main/catalog.json) як HTTPS-джерело. Вибери **TurnKey E Blend → Install** і перезапусти iDrive, якщо Store запропонує.

## Версія 0.1.0

Бета для ID8. Перевірено формулу, навігацію в імітації RHMI та збирання пакета лінкером Store з тестовим донором. Запуск на фізичному MGU ID8 ще не перевірено.

[Вихідний код і ресурси](TurnKey-E-Blend-ID8-0.1.0-GitHub.zip) містять оригінальну атрибуцію та ліцензії. Формула адаптована з [TurnKey E Blend](https://github.com/HasMan/turnkey-ethanol-blend). MGU Store збирає пакет із SDK головного блока.
