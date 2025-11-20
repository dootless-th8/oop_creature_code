# Creature Battle Project (OOP + Git Branching Practice)

This project is designed to help me learn **object-oriented programming** in Python — especially **inheritance** — while also practicing key **Git concepts** like branching, merging, conflict resolution, and version history.

I will begin with a base class (`Creature`) and create additional subclasses on separate Git branches to simulate a real development workflow.

---

## Learning Objectives

### Python / OOP
- Understand and implement **classes**
- Use **inheritance** to extend behaviors
- Override and extend methods (e.g., `attack()`)
- Practice writing simple test code in `main`

### Git / Version Control
- Create and switch branches
- Merge branches into `main`
- Resolve merge conflicts
- View commit history (`git log --graph --all`)


---

## Project Structure
``` bash
oop_creature_code/
│
├── Creature_code/
│   ├── creature_simulation.py # Base class + subclasses
│
└── README.md
```

## Class Overview
- ### Base Class: Creature
- Attributes: name, hp, attack_power
- Methods:
    - attack(target)
    - is_alive()
    - __str__()

- ### Subclasses
- 1. SwimmingCreature
    - Adds attribute: depth
    - Method: dive_to(depth)
    - Overrides attack() to include underwater behavior

- 2. FlyingCreature
    - Adds attribute: altitude
    - Method: fly_to(altitude)
    - Overrides attack() to include aerial behavior

- 3. FireCreature
    - Adds attribute: fire_level
    - Method: emit_fire(level)
    - Overrides attack() to include fire emission effects

## Run the program
* ### Create a test run or run the program like the following code:
    ```python
    # Test: Dead creature cannot attack
    ghost = Creature("Ghost", 0, 10)
    knight = Creature("Knight", 50, 7)
    print("Test 5: Ghost tries to attack Knight")
    ghost.attack(knight)
    print(f"Knight HP should remain 50 → Actual: {knight.hp}")
    print()
    ```
    ```python
    # Test: Flying Creature
    print("=== FlyingCreature Tests ===\n")
    hawk = FlyingCreature("Sky Hawk", 50, 8)
    hawk.fly_to(120)
    print(f"Altitude should be 120 → Actual: {hawk.altitude}")

    dummy = Creature("Practice Dummy", 40, 0)
    hawk.attack(dummy)
    print(f"Dummy HP should be 32 → Actual: {dummy.hp}")
    dummy.attack(hawk)
    print()
    print("=== Tests Completed ===")
    print()
    ```
