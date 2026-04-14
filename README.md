Ось детальний розв'язок усіх завдань з колоквіуму. 

Головне правило цього завдання, яке написано на самому початку (Uwaga!): **після кожного додавання файлів до `stage` (тобто після кожної команди `git add`) обов'язково треба перевіряти їх статус за допомогою `git status`**. Я додав ці перевірки у код нижче.

Для файлів з твоїм іменем та ініціалами я використав **Anhelina_Chyruk** та гілку **AC**, а також сьогоднішню дату.

### Zadanie 1

```bash
# 1. Створення репозиторію з головною гілкою main
mkdir kolokwium
cd kolokwium
git init -b main

# 2. Створення README.md, додавання заголовку та списку команд
echo "# Zadanie 1" > README.md
echo "Wykorzystane komendy: git init -b main, echo, git add, git status, git commit, git remote add, git push" >> README.md

# Перевірка статусу перед додаванням (як вимагає Uwaga)
git status

# Додавання до stage і обов'язкова перевірка статусу!
git add README.md
git status

# 3. Створення коміту з повідомленням
git commit -m "Zadanie 1"

# 4. Відправка змін до віддаленого репозиторію
# Замість <URL_TWOJEGO_REPO> встав посилання на свій GitHub/GitLab (наприклад, https://github.com/login/repo.git)
git remote add origin <URL_TWOJEGO_REPO>
git push -u origin main
```

---

### Zadanie 2

```bash
# 1. Створення файлу з твоїм іменем та прізвищем
touch Anhelina_Chyruk.txt

# 2. Створення файлу з сьогоднішньою датою
touch 2026-04-14.txt

# 3. Створення нової гілки з твоїми ініціалами (AC) та перехід на неї
git checkout -b AC

# 4. Перевірка списку доступних гілок
git branch

# 5. Додавання ТІЛЬКИ файлу з іменем та прізвищем до нової гілки
git status
git add Anhelina_Chyruk.txt
git status
git commit -m "Dodano plik z imieniem i nazwiskiem"

# 6. Оновлення файлу README.md
echo "## Zadanie 2" >> README.md
echo "Wykorzystane komendy: touch, git checkout -b, git branch, git status, git add, git commit, git push" >> README.md

# Додавання README до stage і перевірка статусу
git status
git add README.md
git status
git commit -m "Zaktualizowano README dla Zadania 2"

# 7. Відправка змін до віддаленого репозиторію (на новій гілці)
git push -u origin AC
```

---

### Zadanie 3

*Примітка: Не забудь робити скріншоти кожної дії та зберігати їх, щоб потім додати до `README`, як вказано в завданні!*

```bash
# 1. Додавання вказаного email до конфігурації репозиторію
git config user.email "KrystianSzwedoKul"

# (Можеш перевірити, чи він додався, командою: git config user.email)
```

**2. Створення Pull Request:**
Зазвичай це **не робиться в терміналі**. Тобі потрібно:
1. Зайти на сайт GitHub (або платформи, яку ви використовуєте).
2. Відкрити свій репозиторій.
3. Ти побачиш жовту/зелену підказку **"Compare & pull request"** біля гілки `AC`. Натисни її.
4. Натисни кнопку **"Create pull request"**, щоб злити (merge) гілку `AC` у гілку `main`. 
*(Якщо на комп'ютерах в університеті встановлено GitHub CLI, команда в терміналі виглядала б так: `gh pr create --base main --head AC --title "Merge AC to main"`, але краще роби через браузер).*

```bash
# 3. Додавання коментаря до файлу з іменем та прізвищем
echo "Komentarz dodany do pliku" >> Anhelina_Chyruk.txt

# Додавання файлу до stage та перевірка
git status
git add Anhelina_Chyruk.txt
git status
git commit -m "Dodano komentarz do pliku Anhelina_Chyruk"

# Відправка змін, щоб їх було видно в репозиторії
git push origin AC
```
