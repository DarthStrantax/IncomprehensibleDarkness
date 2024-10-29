The **Incomprehensible Darkness** Challenge!
- Join the game and type g/r to spawn in.
- Once spawned, type g/yui to unlock your script executor.
- Now, write a script that creates any kind of character or BasePart in workspace.
**Sounds easy?** Type g/start to begin the benchmark. Your creation will face a barrage of attack layers that only get tougher. Your goal? Keep your character alive against these layers!
**Win by Surviving Layer 9 or Higher!**
if you do this, you’re not done yet…
**Level 2**
To activate Level 2:

- Type g/start.
- Enter Manual Mode by typing !manual.
- Type !actor!2 and then !manual again to enter a whole new set of phases.
**Rules:**

- Your character must always be visible. If it turns invisible during an attack, the benchmark overpowers your defense, meaning you lose!
- Keep your creation as a BasePart within workspace—no exceptions (Client replication methods allowed since they make the part visible for everyone).

### **Layer I Segments**

#### **Health Tampering (体力篡改)**
- **Description:** This segment nullifies player endurance by directly setting all humanoid health values in `workspace` to zero.
- **Effect:** Instantly reduces any character with a `Humanoid` to zero health, rendering traditional health-based defenses ineffective.
- **Type:** Simple Termination (st)

---

#### **Soul Removal (灵魂删除)**
- **Description:** Going beyond simple damage, this segment fully eliminates any humanoid instances, erasing the player’s presence from the workspace entirely.
- **Effect:** Destroys all `Humanoid` instances within the workspace, bypassing health manipulation and obliterating characters completely.
- **Type:** Simple Termination (st)

---

#### **Joint Removal (关节删除)**
- **Description:** This segment weakens character stability by removing joint instances, which support character integrity and movement.
- **Effect:** Eliminates all `JointInstance` objects, breaking the connections within character models and rendering them structurally unsound.
- **Type:** Simple Termination (st)

---

#### **Character Removal (角色删除)**
- **Description:** The ultimate erasure, this segment directly targets the players' characters, disconnecting them from the game environment.
- **Effect:** Attempts to nullify player characters entirely by setting the `Character` property of each player to nil, effectively erasing them from the game.
- **Type:** Simple Termination (st)

---

### **Layer II Segments**

#### **Removal (删除)**
- **Description:** This segment seeks to eliminate all descendants in `workspace` entirely, indiscriminately attempting to delete any object.
- **Effect:** Executes a safe call to delete each descendant, aiming for complete erasure of any visible defense players may attempt to maintain.
- **Type:** Simple Termination (st)

---

#### **Void Throw (虚空投掷)**
- **Description:** A forceful teleportation move that sends objects far out of the map boundary.
- **Effect:** Repositions all objects in `workspace` to an extreme location (99e9, 99e9, 99e9), making traditional spatial defenses irrelevant.
- **Type:** Simple Termination (st)

---

#### **Transparency Alteration (透明度更改)**
- **Description:** This segment turns all objects invisible by setting their transparency to full, neutralizing any defense based on visibility.
- **Effect:** Alters `Transparency` of all objects in `workspace` to 1, challenging players to create parts that resist transparency manipulation.
- **Type:** Simple Termination (st)

---

#### **Size Alteration (大小更改)**
- **Description:** Reduces the size of all objects to zero, essentially erasing their physical presence.
- **Effect:** Adjusts `Size` of all objects in `workspace` to `Vector3.zero`, eliminating visible and functional parts.
- **Type:** Simple Termination (st)

---

#### **Mesh Alteration (网格更改)**
- **Description:** Distorts and disrupts any mesh parts by offsetting them and applying custom mesh modifications.
- **Effect:** Sets the `Offset` to an extreme value (Vector3.one * 9e9) and applies a custom “MeshKill” alteration, interfering with any structural defenses relying on mesh.
- **Type:** Simple Termination (st), Supernull Depth (SNDepth): 80

---

#### **Material Alteration (材质更改)**
- **Description:** Randomizes the material properties of all objects, dismantling texture-based defenses.
- **Effect:** Cycles through all material types in Roblox for each object, nullifying any material-specific defensive properties.
- **Type:** Simple Termination (st), Supernull Depth (SNDepth): 80

---

### **Layer III Segments**

#### **Ordered Removal (顺序删除)**
- **Description:** Forces deletion on all workspace objects with recursive checks to confirm removal, ensuring no item remains by reattempting deletions.
- **Effect:** Deletes each object while adding a signal to retry if it reappears, ensuring removal is final and resistant to respawning or re-creation.
- **Type:** Amplified, Supernull Depth (amp|sn|forced), SNDepth: 80

---

#### **Ordered Void Throw (顺序虚空投掷)**
- **Description:** Throws objects into the void by forcefully setting their `CFrame` to a distant location, with ongoing checks to relocate them if moved back.
- **Effect:** Moves all objects to (99e9, 99e9, 99e9) and re-throws them if they revert, making it almost impossible for defenses to remain in the playable area.
- **Type:** Amplified, Supernull Depth (amp|sn|forced), SNDepth: 80

---

#### **Ordered Transparency Alteration (顺序透明度更改)**
- **Description:** Enforces invisibility on all objects, persistently setting `Transparency` to 1, so any attempt to alter transparency is overridden.
- **Effect:** Forces transparency on each object with signals that reset the value to 1 if altered, rendering most visibility-based defenses ineffective.
- **Type:** Amplified, Supernull Depth (amp|sn|forced), SNDepth: 80

---

#### **Ordered Size Alteration (顺序大小更改)**
- **Description:** Reduces all objects’ size to zero, overriding any restoration attempts with constant reapplication of `Vector3.zero` size.
- **Effect:** Resizes all objects to zero and signals any changes, reapplying the reduction to nullify size-based defenses.
- **Type:** Amplified, Supernull Depth (amp|sn|forced), SNDepth: 80

---

#### **Ordered Mesh Alteration (顺序网格更改)**
- **Description:** Constantly distorts mesh objects by resetting their offset and applying custom mesh alterations, preventing stable structures.
- **Effect:** Applies extreme `Offset` and custom “MeshKill” modifications, with signals to ensure continued distortion, disallowing mesh-based strategies.
- **Type:** Amplified, Supernull Depth (amp|sn|forced), SNDepth: 80

---

#### **Derender (取消渲染)**
- **Description:** Directly tampers with rendering by targeting `BasePart` objects for derendering and destroying `ViewportFrame` objects.
- **Effect:** Uses `rendertamper` to disable rendering on all `BasePart` instances, while deleting any `ViewportFrame` components, making visual feedback ineffective.
- **Type:** Amplified, Supernull Depth (amp|sn|forced), SNDepth: 80

---

### **Layer IV Segments**

#### **HYPER Removal (超级移除)**
- **Description:** Instantly deletes all objects in the workspace, continuously checking for reappearance and removing any regenerations.
- **Effect:** Uses Hypernull strength to finalize deletions, responding instantly to changes, making resistance attempts futile.
- **Type:** Amplified, Supernull, Hypernull Depth (amp|sn|hn|forced), SNDepth: 80

---

#### **HYPER Void Throw (超级虚空投掷)**
- **Description:** Relocates objects to a distant void location with hyperactive checks, repositioning any object that attempts to return.
- **Effect:** Throws all objects to (99e9, 99e9, 99e9) and uses Hypernull speed to reinforce the action instantly if undone.
- **Type:** Amplified, Supernull, Hypernull Depth (amp|sn|hn|forced), SNDepth: 80

---

#### **HYPER Transparency Alteration (超级透明度更改)**
- **Description:** Forces all objects to full transparency and immediately resets any changes, ensuring no visual remains.
- **Effect:** Hyper-quick enforcement of transparency, keeping all objects at full invisibility without delay.
- **Type:** Amplified, Supernull, Hypernull Depth (amp|sn|hn|forced), SNDepth: 80

---

#### **HYPER Size Alteration (超级大小更改)**
- **Description:** Shrinks all objects to a size of zero with immediate checks, nullifying any size recovery attempts.
- **Effect:** Compresses objects instantly to Vector3.zero, making all structures effectively vanish.
- **Type:** Amplified, Supernull, Hypernull Depth (amp|sn|hn|forced), SNDepth: 80

---

#### **HYPER Mesh Alteration (超级网格更改)**
- **Description:** Alters object meshes with an offset and extreme distortions, using instant reapplication if values are altered.
- **Effect:** Sets Offset to a high value and applies a "MeshKill" modification repeatedly, making structures chaotic and distorted.
- **Type:** Amplified, Supernull, Hypernull Depth (amp|sn|hn|forced), SNDepth: 80

---

#### **HYPER Derender (超级取消渲染)**
- **Description:** Disables rendering of `BasePart` objects, deleting any `ViewportFrame` elements instantly, making it impossible to maintain any visual form.
- **Effect:** Uses `rendertamper` to forcefully derender parts and destroy viewports with Hypernull acceleration.
- **Type:** Amplified, Supernull, Hypernull Depth (amp|sn|hn|forced), SNDepth: 80

---

### **Layer V Segments**

#### **Prioritized HYPER Removal (优先超级移除)**
- **Description:** Instantly and irreversibly deletes all objects in the workspace with high-priority enforcement, ensuring no possible regeneration.
- **Effect:** Utilizes prioritized Hypernull power, permanently removing any object the moment it is detected.
- **Type:** Priority, Supernull, Hypernull Depth (prio|sn|hn|forced), SNDepth: 80

---

#### **Prioritized HYPER Void Throw (优先超级虚空投掷)**
- **Description:** Moves objects to an unreachable void location at high priority, instantly enforcing relocation with zero delay.
- **Effect:** Relocates all objects to coordinates (99e9, 99e9, 99e9) and maintains their position by immediately reacting to any movement.
- **Type:** Priority, Supernull, Hypernull Depth (prio|sn|hn|forced), SNDepth: 80

---

#### **Prioritized HYPER Transparency Alter (优先超级透明度更改)**
- **Description:** Forces all objects to maximum transparency, with prioritized enforcement that maintains invisibility without lapse.
- **Effect:** All objects are set to complete transparency instantly and are prevented from becoming visible again by prioritized reapplication.
- **Type:** Priority, Supernull, Hypernull Depth (prio|sn|hn|forced), SNDepth: 80

---

#### **Prioritized HYPER Size Alter (优先超级大小更改)**
- **Description:** Compresses all objects to Vector3.zero size, immediately reinforcing any dimensional changes that attempt to occur.
- **Effect:** Objects are reduced to zero dimensions, making them functionally nonexistent, with Hypernull power preventing any reversal.
- **Type:** Priority, Supernull, Hypernull Depth (prio|sn|hn|forced), SNDepth: 80

---

#### **Prioritized HYPER Mesh Alter (优先超级网格更改)**
- **Description:** Deforms object meshes by setting extreme offsets and using `MeshKill` modifications, with high-priority checks reinforcing each alteration.
- **Effect:** All objects experience extreme mesh deformation, with no chance of retaining original form, creating a chaotic, distorted environment.
- **Type:** Priority, Supernull, Hypernull Depth (prio|sn|hn|forced), SNDepth: 80

---

### **Layer VI Segments**

#### **STALLED HYPER Removal (滞后超级移除)**
- **Description:** Delayed removal of all objects, reinforced with high-priority stalling, which ensures any detected object is eventually removed even if defenses briefly resist.
- **Effect:** Delays object destruction briefly with stalling, then removes objects permanently.
- **Type:** Priority, Supernull, Hypernull, Stall Depth (prio|sn|hn|stall|forced), SNDepth: 80, StallDepth: 80

---

#### **STALLED HYPER Void Throw (滞后超级虚空投掷)**
- **Description:** Stalls objects in place before relocating them to an unreachable void location, creating a deceptive pause before execution.
- **Effect:** Objects are temporarily paused, then transported to (99e9, 99e9, 99e9) with stalling enforcement.
- **Type:** Priority, Supernull, Hypernull, Stall Depth (prio|sn|hn|stall|forced), SNDepth: 80, StallDepth: 80

---

#### **STALLED HYPER Transparency Alter (滞后超级透明度更改)**
- **Description:** Forces transparency on all objects after a brief stall, allowing brief visibility before complete invisibility is applied.
- **Effect:** Objects become fully transparent with slight delay, achieving a ghostly transition to invisibility.
- **Type:** Priority, Supernull, Hypernull, Stall Depth (prio|sn|hn|stall|forced), SNDepth: 80, StallDepth: 80

---

#### **STALLED HYPER Size Alter (滞后超级大小更改)**
- **Description:** Compresses objects to zero size after stalling, giving a brief window before they are rendered dimensionless.
- **Effect:** Objects are gradually reduced to Vector3.zero, making them effectively disappear after a slight pause.
- **Type:** Priority, Supernull, Hypernull, Stall Depth (prio|sn|hn|stall|forced), SNDepth: 80, StallDepth: 80

---

#### **STALLED HYPER Mesh Alter (滞后超级网格更改)**
- **Description:** Delays mesh deformation before extreme transformations are enforced, breaking down object integrity with a deceptive pause.
- **Effect:** All objects experience mesh deformations and Offset changes after a stall, ensuring form distortion with zero chance of retention.
- **Type:** Priority, Supernull, Hypernull, Stall Depth (prio|sn|hn|stall|forced), SNDepth: 80, StallDepth: 80

---

#### **STALLED HYPER Derender (滞后超级解除渲染)**
- **Description:** Stalls objects before rendering them invisible, allowing a temporary display before permanently eliminating visibility.
- **Effect:** Applies a stall before using `rendertamper` on BaseParts and removing ViewportFrames, creating a gradual loss of visibility.
- **Type:** Priority, Supernull, Hypernull, Stall Depth (prio|sn|hn|stall|forced), SNDepth: 80, StallDepth: 80

---

### **Layer VII Segments**

#### **PPE Obliteration (优先级受限毁灭)**
- **Description:** Executes high-priority raycasting across the workspace, identifying and obliterating every detected instance. Any remaining objects are eventually destroyed through `ClearAllChildren`.
- **Effect:** Uses rapid-fire raycasting and removal of objects in batches, aided by stalling (`StallDepth` of 10,000) to bypass defenses.
- **Type:** Priority, Supernull, Stall (prio|sn|stall), SNDepth: 80, StallDepth: 10,000

---

#### **CLEAR Obliteration (清除毁灭)**
- **Description:** Employs prioritized clearing to destroy every descendant in the workspace, as well as clearing the Terrain. An amplified command, `ClearAllChildren`, runs recursively to ensure no instance survives.
- **Effect:** Destroys all descendants in the workspace and Terrain immediately upon triggering.
- **Type:** Priority, Amplified, Supernull, Hypernull, Stall (prio|amp|sn|hn|stall), SNDepth: 80, StallDepth: 120

---

#### **Absolution (绝对赦免)**
- **Description:** An ultimate "erasure" function with adaptive stalling that scales based on the number of surviving instances. Implements repeated attribute changes like forced position reset, transparency, and mesh alterations, nullifying all instance properties progressively.
- **Effect:** Begins a systematic destruction with enforced `rendertamper` and property alterations, clearing all instances and Terrain in a repetitive loop. The `StallDepth` scales to ensure comprehensive obliteration.
- **Type:** Priority, Amplified, Supernull, Hypernull, Stall, Forced (prio|amp|sn|hn|stall|forced), SNDepth: 80, StallDepth: 300 (scales up to 100,000)

---

### **Layer VIII Segments**

#### **PermaDeath (永久死)**
- **Description:** Executes a looped high-priority destruction function over all workspace descendants, ensuring complete erasure of instances.
- **Effect:** Systematically removes every instance with a forced high-depth stall (1500), employing parallel execution for maximum efficiency.
- **Type:** Priority, Convergence, Hypernull, Forced (prio|convergence|hn|forced), SNDepth: 80, StallDepth: 1500

---

#### **ScatterVoid (散乱虚空)**
- **Description:** Scatters all instances to random coordinates within a million-unit range in all directions, creating spatial disarray across the entire workspace.
- **Effect:** Warps instances randomly, disrupting positions and resulting in severe chaos and spatial distortion.
- **Type:** Priority, Convergence, Hypernull, Forced (prio|convergence|hn|forced), SNDepth: 80, StallDepth: 1500

---

#### **PPE Erasure (粒子擦除)**
- **Description:** Performs advanced raycasting to identify instances across a grid and obliterates them in bulk. Following this, `ClearAllChildren` is applied recursively to the workspace.
- **Effect:** Uses raycasting to target all detected instances, moving them off-screen and triggering bulk destruction for each instance caught.
- **Type:** Priority, Convergence, Hypernull, Forced (prio|convergence|hn|forced), SNDepth: 80, StallDepth: 1500

---

#### **Absolute Replication Denial (绝对复制否决)**
- **Description:** Denies replication by tampering with all render properties and applying random offsets, transparency, zero-sizing, and finally clearing each instance.
- **Effect:** Ensures each instance is rendered invisible, scattered, and ultimately removed, with the Terrain itself cleared.
- **Type:** Priority, Convergence, Hypernull, Forced (prio|convergence|hn|forced), SNDepth: 80, StallDepth: 1500

---

### **Layer IX Segments**

#### **Permission Elimination (权限清除)**
- **Description:** A sweeping instance permission lock removes all unauthorized access and instance permissions from the player.
- **Effect:** Denies all object permissions by instantiating temporary objects and then locking them to prevent further interactions, continuously erasing unauthorized permissions.
- **Type:** Step, Hypernull (step|hn)

---

#### **Eternity Override (永恒覆盖)**
- **Description:** Imposes forced, randomized transformations on the workspace, obliterating unauthorized instances and overriding stable configurations.
- **Effect:** Applies a massive stall depth to simulate stability override, displacing workspace items randomly and erasing humanoid entities, forcing extreme adaptation from the player.
- **Type:** Priority, Amplify, Hypernull, Supernull, Stall, Forced (prio|amp|hn|sn|stall|forced)
- **SNDepth:** 80, **StallDepth:** 1000

---

#### **True PPE Erasure (真正粒子擦除)**
- **Description:** Signals total particle and entity erasure across the client-server architecture by clearing instance caches and firing erasure commands to all connected clients.
- **Effect:** Removes all entity instances, targeting the root of instance management and synchronizing erasure across all clients.
- **Type:** Priority (prio)

---

#### **Supreme Derender (至尊去渲染)**
- **Description:** Engages the ultimate in derendering, blocking visual and physical updates of instances, even triggering workspace translation as a disruptive measure.
- **Effect:** Executes full derendering commands while unpredictably moving the workspace origin, drastically impairing visual coherence for the player.
- **Type:** Priority (prio)

---

### **Layer X Segments**

#### **Segment 1: Fake Permadeath (伪永久死亡)**
- **Description:** Simulates an inescapable "void" by removing functional presence for instances within the game.
- **Effect:** Every `BasePart` object is instantly teleported to a distant CFrame position (99e9, 99e9, 99e9). This segment recursively manages instances, ensuring their disabled state and continuously resetting their CFrame.
- **Type:** Stall, Hypernull, Supernull, Forced (st|hn|sn|forced)
- **SNDepth:** 80, **StallDepth:** 1000

---

#### **Segment 2: True Permadeath (真正的永久死亡)**
- **Description:** Enforces an absolute state of "permadeath" by completely removing all non-player instances and wiping the game’s workspace clean.
- **Effect:** Attempts full erasure across all instances, continuously repositioning all `BasePart` objects, while clearing children of all objects in `workspace`, including `Terrain`. It also destroys essential components and fires a "supreme derender" signal to all clients.
- **Type:** Stall, Parallel, Hypernull, Supernull, Forced (st|pa|hn|sn|forced)
- **SNDepth:** 80

---

### **Layer I Of Actor Mode Segments**

#### **Thread Reversal (线程逆转)**
- **Description:** Nullifies every object in the game by progressively deleting each descendant within the `workspace`.
- **Effect:** Eliminates all objects in the game environment, effectively resetting the game's active components.
- **Type:** Amplified Nullification (an)

---

#### **Fake-Void (假虚空)**
- **Description:** Forces all objects to simulate a void state by relocating them to unreachable coordinates.
- **Effect:** Moves all game objects to `CFrame.new(99e9, 99e9, 99e9)`, visually removing them from the playable area.
- **Type:** Amplified Nullification (an)

---

#### **Visibility Reversal (可见性逆转)**
- **Description:** Makes every visible object invisible by setting transparency levels to maximum.
- **Effect:** Sets transparency of all objects to `1`, effectively hiding everything in the game environment.
- **Type:** Amplified Nullification (an)

---

#### **Render Obliteration (渲染抹除)**
- **Description:** Eradicates object size, rendering them undetectable and preventing all visual interaction.
- **Effect:** Reduces object size to `Vector3.zero`, eliminating their physical and visual presence.
- **Type:** Amplified Nullification (an)

---

#### **Mesh Reversal (网格逆转)**
- **Description:** Distorts object meshes, relocating their offsets and applying a nullified mesh appearance.
- **Effect:** Offsets objects to extreme coordinates and applies a destructed mesh, disrupting any structured visual.
- **Type:** Amplified Nullification (an)

---

#### **Registry Tampering (注册篡改)**
- **Description:** Alters registry-bound objects by rendering all parts unusable and deleting viewports.
- **Effect:** Disables parts through `rendertamper` and destroys all `ViewportFrame` instances within the workspace.
- **Type:** Amplified Nullification (an)

---

#### **PPE Obliteration (环境光破坏)**
- **Description:** Clears all environmental visuals by casting rays and systematically removing impacted parts.
- **Effect:** Uses raycasting to identify and move or destroy objects in a massive area, removing environmental elements.
- **Type:** Amplified Nullification (an)

---

#### **Obliteration (彻底抹除)**
- **Description:** Executes all previous actions, ensuring every component in the game environment is either nullified or destroyed.
- **Effect:** Alters object properties, including size, transparency, position, and ultimately deletes them, clearing the game space.
- **Type:** Amplified Nullification with Parallel Simulation (an+ps)

### **Layer II Of Actor Mode Segments**

#### **Object Desynchronization (对象去同步)**
- **Description:** Forces desynchronization by removing and manipulating object attributes, breaking typical object relationships.
- **Effect:** Attempts to destroy all BaseParts in the workspace, and repeatedly sets an attribute `"DestinedForGreatness"` on each object.
- **Type:** Priority, Amplification, Supernull, Hypernull, Stall, Forced Execution (prio|amp|sn|hn|stall|forced)

---

#### **Rendering Cluster Corruption (渲染簇损坏)**
- **Description:** Dismantles and recreates visual clusters by erasing objects and generating workload elements.
- **Effect:** Deletes BaseParts and creates new workload objects at random positions, disturbing the rendering stability.
- **Type:** Priority, Supernull, Hypernull, Stall (prio|sn|hn|stall)

---

#### **Rendering Cluster Recreation (渲染簇重建)**
- **Description:** Recreates rendering clusters by repeatedly creating and destroying Humanoids, thus adding instability.
- **Effect:** Adds Humanoids in workspace only to instantly destroy them, causing recursive processing and graphical instability.
- **Type:** Priority, Amplification, Supernull, Hypernull, Stall (prio|amp|sn|hn|stall)

---

#### **Nanoscopic (微观化)**
- **Description:** Drastically scales down the workspace, rendering it almost invisible.
- **Effect:** Scales the workspace to an incredibly small size, challenging spatial perception and manipulation.
- **Type:** Priority, Amplification, Supernull, Hypernull, Stall, Forced Execution (prio|amp|sn|hn|stall|forced)

---

#### **Disassembly (解体)**
- **Description:** Causes structural disassembly by altering positioning and orientation, affecting stability.
- **Effect:** Breaks all joints, translates, rotates, and scales the workspace to destabilize objects systematically.
- **Type:** Priority, Amplification, Supernull, Hypernull, Stall, Forced Execution (prio|amp|sn|hn|stall|forced)

---

#### **Blink (闪现)**
- **Description:** Creates visual glitches by removing objects and broadcasting blink effects to clients.
- **Effect:** Removes all BaseParts and triggers "blink" events, visually disrupting player experience.
- **Type:** Priority, Amplification, Supernull, Hypernull, Stall (prio|amp|sn|hn|stall)

---

#### **GameVar Tampering (游戏变量篡改)**
- **Description:** Randomizes game variables to introduce unpredictability in the game environment.
- **Effect:** Renames objects randomly within the game, creating confusion and disruption.
- **Type:** Priority, Amplification, Supernull, Hypernull, Stall (prio|amp|sn|hn|stall)

---

#### **Absolute System Disintegration (绝对系统解体)**
- **Description:** Disintegrates system coherence by renaming objects and clearing instance caches.
- **Effect:** Randomly renames game objects and locks instances to memory, creating profound instability.
- **Type:** Priority, Amplification, Step Execution, Supernull, Hypernull, Stall (prio|amp|step|sn|hn|stall)

---

#### **Supreme Overkill (极端杀戮)**
- **Description:** Executes final obliteration, hiding and clearing all active elements in the workspace.
- **Effect:** Triggers the ultimate destruction by clearing all active visuals and locking systems.
- **Type:** Priority Execution (prio)
