<h1 align="center">Dungeon Saga</h1>

**Dungeon Saga** is a **turn-based strategy game** where players can choose from **three heroes** — **Knight**, **Assassin**, or **Wizard** — each with unique stats and a one-time **special ability** that can change the tide of battle.

Your goal?  
**Survive every encounter, defeat all enemies, and conquer the final boss.**

---

## ⚔️ Features
- 🎮 **Three Playable Heroes**
  - **Knight** – High defense and balanced attack.
  - **Assassin** – Agile and deadly with critical strikes.
  - **Wizard** – Uses powerful spells with strategic mana management.
- 🧠 **Turn-Based Combat System**
  - Plan each move carefully; every turn counts.
- 🌟 **Hero Abilities**
  - Each hero has a **unique one-time special skill** to use strategically.
- 💀 **Boss Battles**
  - Face challenging enemies and the ultimate boss at the end.

---

## Object-Oriented Principles
## 🔐 1. Encapsulation
**Definition:**
Encapsulation means restricting direct access to an object’s internal data and exposing it through methods.
**✔ How the code demonstrates it:**
* All attributes in `Enemy` and `Hero` are declared `private` or `protected`.
* Access is provided only through getter methods:
```java
public String getName() { return name; }
public int getHp() { return hp; }
```
* Methods such as:
```java
public void takeDamage(int dmg)
public void restoreToFull()
```

safely modify the object’s internal state.

**🔎 Why it matters:**
Encapsulation prevents unwanted external modification and preserves data integrity.

---

## 🎭 2. Abstraction

**Definition:**
Abstraction means focusing on what an object does, not how it does it.

**✔ How the code demonstrates it:**

* The `Hero` class is declared abstract:

```java
public abstract class Hero
```

* It defines abstract behavior:

```java
public abstract void useSpecial(Enemy enemy);
```

* Common hero features like HP, attack, blocking, and special skill tracking are all handled within the abstract base class.

**🔎 Why it matters:**
Abstraction simplifies the design and forces subclasses to define their own unique behavior.

---

## 🧬 3. Inheritance

**Definition:**
Inheritance allows child classes to reuse and extend behavior from a parent class.

**✔ How the code demonstrates it:**

* `Knight` and `Wizard` both extend the `Hero` class:

```java
public class Knight extends Hero { ... }
public class Wizard extends Hero { ... }
```

* They automatically inherit:

  * HP, attack, name fields
  * Damage system (`takeDamage`)
  * Special usage tracking
  * Block system
  * Getter methods

**🔎 Why it matters:**
Inheritance reduces duplicate code and organizes objects into meaningful hierarchies.

---

## 🔄 4. Polymorphism

**Definition:**
Polymorphism allows different objects to be treated as the same type while exhibiting unique behavior.

**✔ How the code demonstrates it:**

* Each subclass provides its own version of the `useSpecial` method:

```java
@Override
public void useSpecial(Enemy enemy) { ... }
```

* Example behaviors:

  * `Knight` deals damage and enables block
  * `Wizard` heals itself instead

* Both can be used interchangeably:

```java
Hero hero = new Knight();
hero.useSpecial(enemy); // Knight's behavior

hero = new Wizard();
hero.useSpecial(enemy); // Wizard's behavior
```

**🔎 Why it matters:**
Polymorphism makes the game system flexible and expandable — new hero types are easy to add.

---
## 🏃 How to Run

1. **Clone the repository**  
```bash
git clone https://github.com/dnlaldrn/OOP_Dungeon-Saga.git
```

2. **Navigate to the source folder**  
```bash
cd OOP_Dungeon-Saga/src
```

3. **Compile all Java files**  
```bash
javac *.java
```

4. **Run the game**  
```bash
java DungeonSagaMain
```
---
## 🗂️ File Structure

```
OOP_Dungeon-Saga/
├── src/                   # Source code files (Java classes)
│   ├── DungeonSagaMain.java
│   ├── Hero.java
│   ├── Knight.java
│   ├── Wizard.java
│   ├── Assassin.java
│   ├── Enemy.java
│   └── (other game classes)
├── images/                # Character images and assets
│   ├── manjares.jpg
│   ├── laganzon.jpg
│   └── sayson.jpg
├── README.md              # Project README file
└── LICENSE                # License file (if applicable)
```

---

## Example Output
```
Choose Action:
1) Attack
2) Defend
3) Special
Input: 1
White Beast takes 25 damage!
                                                                     /
                                                                    /
                                                                   /
                                               _____,    _..-=-=-=/=-====--,
                                            _.'a   /  .-',___,..=/-=--==-'`
                                          ( _     \ /  //___/-=-/-=----'
                                           ` `\    /  //---/--=/----=-'
                                        ,-.    | / \_//-_.'==-/=---='
                                       (.-.`\  | |'../-'=-=-=/=--'
                    /7                  (' `\`\| //_|-\.`;-~/```~,        _
         .-.       //                        \ | \_,_,_\.' /      \     .'_`\
        (* *)     //                           \          / ,    , \    || `\\
         '.'     //                             \    /   /.--\    \ '._.'/  / |
 _.^._-"""''"""-//                               /  /`--/'   \ \   |`'---'   \/
|  |  |"|   |''//                               / /'   /      \ ;-. \
|==+==| |   |  '                             __/ /    /      __) \ ) `|
|_ | _| |___|                               ((='--;) /       (,___/(,_/
  'v'  /     \                                      /
      /  / \  '                                    /
     /  /   | |                                   /
    /  /    | |
   _' '.   ." ".. 
  '""""     """"
```

---

## Team Contributors

<table>
  <tr>
    <th>Angry Birds Members</th>
    <th>Name</th>
    <th>GitHub</th>
  </tr>
  <tr>
    <td><p align="center">
    <img src="images/laganzon.jpg" width="120"></p></td>
    <td>Laganzon, Adrian G. </td>
    <td><a href="https://github.com/DIAN0402">DIAN0402</a></td>
  </tr>
  <tr>
    <td>
    <p align="center">
    <img src="images/manjares.jpg" width="120"></p></td>
    <td>Manjares, Daniel Aldreen C.</td>
    <td><a href="https://github.com/dnlaldrn">dnlaldrn</a></td>
  </tr>

  <tr>
    <td>
    <p align="center">
    <img src="images/sayson.jpg" width="120"></p></td>
    <td>Sayson, Ian Gabriel F.</td>
    <td><a href="https://github.com/gaabbb314">gaabbb314</a></td>
  </tr>
</table>
