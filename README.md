# **IZHV-Project03-2021:**

### Input System & Local Multiplayer Functionalities

> 🎓 **University**: [VUT FIT](https://www.fit.vut.cz/)
>
> 📚 **Course**: [Introduction to Game Development (IZHV)](https://www.fit.vut.cz/study/course/250838/)
>
> 📅 **Academic Year**: 2021/22

## 🎯 Task Overview:

Transform a 3D Unity game project by injecting advanced interactive elements, integrating the Unity Input System for versatile control, and embedding features to support local multiplayer play.

For the nitty-gritty on the assignment requirements and what’s expected, check out the [Full Assignment Description](http://cphoto.fit.vutbr.cz/ludo/courses/izhv/exercises/e3/).

### **Step-by-Step Instructions:**

📥 1. **Foundation Preparation:**

- Obtain the initial game structure from the Materials section provided.
- Operate exclusively in the 3D perspective, in line with the game's design.
- Familiarize with the primary maneuvering system:
  - 🏃‍♂️ **WASD**: Movement
  - 🎯 **Mouse**: Aiming
  - 🔫 **Left Mouse Button**: Firing
  - ⚔️ **Space**: Alternate Attack Modes

🔧 2. **Enhancing Interaction Mechanics:**

- Proceed to 📄 [`Scripts/Game/Gun.cs`](Assets/Scripts/Game/Gun.cs).
- Tweak the bullet instantiation to occur at the weapon's location by adjusting the `ShootGun` sequence (line 187).
- Create a distinct alternative firing option using `<SPACE>`, ensuring it provides a new gameplay mechanic.

- Activate the `EnemySpawner` along with `MultipleSpawners` in the gameplay area.
- Currently, adversaries exhibit basic behavior. It is your task to program them to actively pursue the closest player.
- Embed a basic level of intelligence in the 🧠 `FixedUpdate` routine found in [`Scripts/Game/Enemy.cs`](Assets/Scripts/Game/Enemy.cs) (line 60), to allow opponents to follow players.

⚙️ 3. **Control Scheme Innovation:**

- Navigate to [`Input/PlayerInput.inputactions`](Assets/Input/PlayerInput.inputactions) and formulate a new control scheme.
- Introduce alternative key bindings for the main actions:
  - 🕹️ **Left Stick**: Move
  - 🎮 **Right Stick**: Aim
  - 🔫 **South Button/Right Trigger**: Fire
  - 🔄 **North Button**: Change Attack Mode
- Without a physical controller, enable the `VirtualController` under the Canvas GameObject or opt for keyboard backups (like UHJK for movement).
- Make sure that the `PlayerInput` setup on [`Prefabs/Player.prefab`](Assets/Prefabs/Player.prefab) is compatible with all control schemes and can switch automatically.

👬 4. **Multiplayer Integration:**

- Adapt the game settings to accommodate multiple players with the alternate control scheme.
- Deploy the `Player Input Manager Component` within the game's environment for managing player entries and exits.
- Monitor player join or leave actions through the 📊 `Settings` script in [`Scripts/Game/Settings.cs`](Assets/Scripts/Game/Settings.cs) (line 100).
- Trigger the appearance of a second player upon any action taken using the secondary controls.

## 📊 Evaluation Results

The project successfully fulfilled the requirements.

🟢🟢🟢🟢🟢  
**Total Points: 6/6**
