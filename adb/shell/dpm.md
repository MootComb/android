*   **`adb shell dpm is-operation-safe 123`**: "Подскажите, безопасно ли сейчас выполнять операцию сброса к заводским настройкам? Не возникнет ли конфликтов с текущими политиками?" 🤷‍♂️
    *   Пример: `adb shell dpm is-operation-safe 5` (где `5` - это *возможный* код операции "сброс к заводским настройкам". **Важно:** Этот код может быть другим!)

**
*   **`adb shell dpm is-operation-safe-by-reason 456`**: "Учитывая определенные обстоятельства, например, срочность, допустимо ли сейчас выполнить данное действие?" 🤨
    *   Пример: `adb shell dpm is-operation-safe-by-reason 101` (где `101` - это *возможный* код причины "пользователь подтвердил действие". **Важно:** Этот код может быть другим!)


*   **`adb shell dpm set-operation-safe 123 456`**: "Я понимаю, что данная операция может быть небезопасной, но ввиду определенных обстоятельств, я беру на себя ответственность за ее выполнение. Прошу систему считать ее безопасной." 😈
    *   Пример: `adb shell dpm set-operation-safe 2 200` (где `2` - *возможный* код операции "установка приложения из неизвестного источника", а `200` - *возможный* код причины "пользователь подтвердил установку и берет на себя ответственность". **Важно:** Эти коды могут быть другими!)


*   **`adb shell dpm list-owners`**: "Прошу предоставить список приложений, обладающих правами владельца устройства или профиля." 🧐
    *   Пример: `adb shell dpm list-owners` (просто выводит список владельцев)


*   **`adb shell dpm list-policy-exempt-apps`**: "Прошу предоставить список приложений, для которых не действуют определенные политики безопасности." 🙄
    *   Пример: `adb shell dpm list-policy-exempt-apps` (просто выводит список приложений, которым можно нарушать правила)


*   **`adb shell dpm set-active-admin com.example.myapp/.MyAdminReceiver`**: "Назначить указанное приложение администратором устройства, предоставив ему соответствующие полномочия." 👮‍♂️
    *   Пример: `adb shell dpm set-active-admin com.example.myapp/.MyAdminReceiver` (где `com.example.myapp/.MyAdminReceiver` - это имя компонента приложения, который станет администратором)


*   **`adb shell dpm set-device-owner com.example.myapp/.MyDeviceOwnerReceiver`**: "Назначить указанное приложение владельцем устройства, предоставив ему максимальные права управления." 👑
    *   Пример: `adb shell dpm set-device-owner com.example.myapp/.MyDeviceOwnerReceiver` (где `com.example.myapp/.MyDeviceOwnerReceiver` - это имя компонента приложения, которое станет владельцем устройства)


*   **`adb shell dpm set-profile-owner com.example.myapp/.MyProfileOwnerReceiver`**: "Назначить указанное приложение владельцем профиля, предоставив ему контроль над настройками и политиками профиля." 💼
    *   Пример: `adb shell dpm set-profile-owner com.example.myapp/.MyProfileOwnerReceiver` (где `com.example.myapp/.MyProfileOwnerReceiver` - это имя компонента приложения, которое станет владельцем профиля)


*   **`adb shell dpm remove-active-admin com.example.myapp/.MyAdminReceiver`**: "Удалить указанное приложение из списка активных администраторов устройства." 🚪
    *   Пример: `adb shell dpm remove-active-admin com.example.myapp/.MyAdminReceiver` (где `com.example.myapp/.MyAdminReceiver` - это имя компонента приложения, которое нужно удалить из администраторов)


*   **`adb shell dpm clear-freeze-period-record`**: "Очистить записи о периодах заморозки обновлений, чтобы сбросить историю и повторить тестирование." 🔄
    *   Пример: `adb shell dpm clear-freeze-period-record` (просто очищает историю "заморозок")


*   **`adb shell dpm force-network-logs`**: "Принудительно собрать и предоставить сетевые логи для анализа сетевой активности приложений." 🕵️‍♂️
    *   Пример: `adb shell dpm force-network-logs` (просто заставляет систему выдать сетевые логи)


*   **`adb shell dpm force-security-logs`**: "Принудительно собрать и предоставить логи безопасности для анализа событий безопасности на устройстве." 🚨
    *   Пример: `adb shell dpm force-security-logs` (просто заставляет систему выдать логи безопасности)


*   **`adb shell dpm mark-profile-owner-on-organization-owned-device com.example.myapp/.MyProfileOwnerReceiver`**: "Отметить владельца профиля как управляющего корпоративным устройством, предоставив ему доступ к идентификаторам устройства." 🤝
    *   Пример: `adb shell dpm mark-profile-owner-on-organization-owned-device com.example.myapp/.MyProfileOwnerReceiver` (где `com.example.myapp/.MyProfileOwnerReceiver` - это имя компонента приложения, которое является владельцем профиля на корпоративном устройстве)
