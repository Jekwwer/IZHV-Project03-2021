# IZHV-Exercise03-2021

Solution for the 3rd assignment from the course _'[IZHV (Introduction to Game Development)](https://www.fit.vut.cz/study/course/250838/)'_ for the academic year 2021/22 at VUT FIT. \
Řešení 3. úkolu z předmětu _'[IZHV (Základy herního vývoje)](https://www.fit.vut.cz/study/course/250838/.cs)'_ pro akademický rok 2021/22 na VUT FIT.

## Task: Entity Control

**Overview:**

In this exercise, you will enhance a 3D Unity game by implementing various behaviors, integrating the Unity Input System, and adding local multiplayer functionalities.

[Full Assignment Description](http://cphoto.fit.vutbr.cz/ludo/courses/izhv/exercises/e3/)

---

**Instructions:**

1. **Setup:**

   - Download the project template from the Materials section.
   - Ensure you're working in 3D view, as this template is built for 3D gameplay.
   - Familiarize yourself with the default control scheme:
     - **WASD**: Movement
     - **Mouse**: Aiming
     - **Left Mouse Button**: Shoot
     - **Space**: Switch Mode of Fire

2. **Gun and Enemy Behavior:**

   _Gun Behavior_:

   - Navigate to `Scripts/Game/Gun.cs`.
   - Observe that bullets currently spawn at the origin rather than the gun's position. Correct this by modifying the `ShootGun` method (line 187).
   - Implement a secondary firing mode, activated by `<SPACE>`. This mode should distinctly differ from the primary firing mode.

   _Enemy Behavior_:

   - Activate the `EnemySpawner` and `MultipleSpawners` in the scene.
   - Notice that spawned enemies lack interesting behavior. Your task is to make them pursue the nearest player.
   - Implement a simple AI in the `FixedUpdate` method within `Scripts/Game/Enemy.cs` (line 60), allowing enemies to follow players.

3. **Alternative Control Scheme:**

   - Go to `Input/PlayerInput.inputactions` and create a secondary control scheme.
   - Add secondary bindings for primary actions using the following:
     - **Left Stick**: Movement
     - **Right Stick**: Aiming
     - **South Button/Right Trigger**: Shoot
     - **North Button**: Switch Mode of Fire
   - If you lack a controller, activate the `VirtualController` under the Canvas GameObject or use keyboard alternatives (e.g., UHJK for movement).
   - Ensure the `PlayerInput` Component on `Prefabs/Player.prefab` supports all available schemes and has auto-switching enabled.
   - If issues arise, consider re-importing assets via the right-click menu in the Project/Assets window.

4. **Local Multiplayer:**

   - Adjust the game to allow the new control scheme to cater to multiple players simultaneously instead of controlling the main player.
   - Introduce the Player Input Manager Component to the scene. Player additions and removals are managed automatically.
   - To detect player joining or exiting, refer to the `Settings` script at `Scripts/Game/Settings.cs` (line 100).
   - The secondary player should spawn when any button in the secondary control scheme is pressed.
   - For additional guidance, consult Unity's official documentation on local multiplayer.

## Result

TBD

## Evaluation

Total points: **6/6**
