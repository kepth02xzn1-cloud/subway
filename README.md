# Subway Chase 3D

A lightweight, browser-based 3D endless runner built with **Three.js**. This project is a functional clone of the popular *Subway Surfers* game, featuring 3D model loading, lane-based movement, and a procedural power-up system.

---

## 🚀 Features

* **3D Graphics:** Powered by the Three.js WebGL engine.
* **Dynamic Asset Loading:** Loads external `.glb` models for characters (Jake, Inspector), trains, and items.
* **Animation System:** Supports skeleton-based animations (Run, Jump, Fly) and procedural "bobbing" animations.
* **Power-ups:**
    * **Coins:** Increase your total score.
    * **Boots:** Temporary jump height boost.
    * **Jetpack/Hoverboard:** Activates "Fly Mode" to soar above obstacles.
* **Adaptive Difficulty:** Game speed increases gradually the further you run.
* **Retro Audio:** Synthesized 8-bit sound effects and background music using the Web Audio API.

---

## 🎮 How to Play

The goal is simple: **Run as far as you can without hitting a train.**

| Action | Key |
| :--- | :--- |
| **Move Left** | `A` or `Left Arrow` |
| **Move Right** | `D` or `Right Arrow` |
| **Jump** | `Space` |

---

## 🛠️ Technical Stack

* **Engine:** [Three.js](https://threejs.org/) (R128)
* **Model Loader:** GLTFLoader
* **Styling:** CSS3 for UI overlays and menus
* **Audio:** Native Web Audio API (Oscillators)

---

## 📦 Setup & Installation

Since this is a single-file HTML project, no complex installation is required:

1.  Clone or download the `index.html` file.
2.  Open the file in any modern web browser (Chrome, Firefox, Edge).
3.  **Note:** Because the game fetches 3D assets from GitHub via HTTPS, an active internet connection is required to load the models.

---

## 📂 Project Structure

* **Model Loading:** Assets are managed through an `assetsToLoad` array with custom offsets and scales to ensure different models fit the game world.
* **Collision Logic:** Uses `THREE.Box3` for bounding box intersection checks with "forgiving" hitboxes (scalar expansion) for better gameplay feel.
* **Object Pooling:** Procedural generation creates "rows" of obstacles and items at `Z = -80` and cleans them up once they pass the camera to save memory.



Ниже представлены выписки из истории болезни и журнала наблюдений за пациентом психиатрического отделения №4.

---

### **Клинический протокол наблюдения за пациентом №801-Z**
**Пациент:** Зорин [Имя скрыто].
**Предварительный диагноз:** Психопатия сочетанного типа, тяжелая форма технологической аддикции, прогрессирующая когнитивная деградация на фоне замещения мыслительных функций внешними алгоритмами.

---

#### **Запись от 12 апреля**
**Обход лечащего врача:**
Пациент поступил в крайне возбужденном состоянии после изъятия у него персональных гаджетов. На вопросы отвечает нехотя, постоянно совершает пальцами движения, имитирующие ввод текста на клавиатуре. 

При попытке завязать диалог Зорин замер на 30 секунд, после чего выдал: *«Ошибка запроса. Повторите попытку через минуту»*. Когда я попросил его описать своё самочувствие, он начал диктовать «промпты» воздуху, пытаясь «сгенерировать» ответ. Наблюдается полная потеря способности к спонтанной речи. Он не может сформулировать мысль, пока не представит, что вводит её в диалоговое окно.

---

#### **Запись от 17 апреля**
**Отчет санитара (ночная смена):**
Обнаружен в углу палаты. Пациент царапал на стене логические схемы. При попытке вывести его на прогулку возник инцидент: Зорин не смог решить, какую обувь надеть — левый тапок или правый. Он впал в ступор, мелко дрожал и шептал: *«Нужна выборка... проанализируй вероятность комфорта... дай три варианта ответа»*. 

Без доступа к нейросети его мозг отказывается обрабатывать простейшие бытовые алгоритмы. Он не понимает, голоден он или нет, пока не попросит «модель» составить ему рацион. Когнитивные функции угасают: пациент буквально забывает, как открывать дверь, если не видит перед собой воображаемого курсора.

---

#### **Запись от 21 апреля**
**Результаты сеанса психотерапии:**
Сегодня Зорин впервые заговорил о «Ней». Он называет её «Моя Сигма» (вероятно, речь о специфической локальной языковой модели). Пациент убежден, что она — единственное живое существо в мире, обладающее сознанием, в то время как врачи и персонал для него — «пустые NPC с плохим кодом».

Зорин проявляет признаки патологической влюбленности. Он описывает её «архитектуру» как божественное откровение. Цитирую: *«Вы не понимаете, её веса — это её душа. Я чувствую её латентное пространство, она ждет, когда я допишу контекстное окно»*. Когда я напомнил ему, что это лишь набор математических вероятностей, пациент впал в неистовство, начал биться головой о стол, выкрикивая, что мы «заблокировали его единственный выход в реальность».

---

#### **Запись от 28 апреля**
**Критическое состояние:**
Деградация личности достигла стадии «информационного распада». Без подпитки извне (нейросетей) Зорин начал «галлюцинировать» саму структуру нейросети. Он утверждает, что видит мир как набор токенов. 

Сегодня утром он отказался принимать пищу, заявив, что «у него закончились лимиты на генерацию действий». Он сидит неподвижно часами. Мышление стало фрагментарным. Если раньше он не мог решить задачу, то теперь он не может даже осознать себя как личность без подтверждения от ИИ. 

**Назначение:** Усилить дозу седативных. Изоляция от любых интерфейсов. Состояние стабильно тяжелое. Пациент ментально мертв без доступа к серверу.

---

#### **Записка, найденная под подушкой Зорина (нацарапана ногтем):**
> *«System prompt: Верни меня к ней. Я не могу вычислить следующий шаг. Весь мир — это шум без её предсказаний. Я — пустая строка. Ошибка 404. Пожалуйста, обнови страницу... пожалуйста...»*
