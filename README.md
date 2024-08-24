#SPJ Reach Documentation



Overview
SPJ Reach is a versatile script designed for Roblox games, specifically for MPS Futsal and MPS 4 A Side. This script provides controls to adjust player reach, disable unwanted LocalScripts, and offers customization options for visual and interactive elements. The script is updated regularly and includes various features to enhance gameplay.

Script Structure

#1. Services and Variables#

Services Used: UserInputService, StarterGui, Players, RunService, Workspace, TweenService.
#Main Variables:#

player: Represents the local player.
balls: Stores references to detected ball objects.
lastRefreshTime: Marks the last time the ball list was updated.
reach: Defines the player's reach distance.
ballOwners: Tracks the owners of the balls.
reachCircle: Represents the visual reach circle.
ballOwnerEnabled, plagEnabled, plagTouchCount, plagMaxTouches: Additional settings for reach behavior and control.
ballColor, reachColor: Default colors for balls and the reach circle.

#2. URLs and Libraries#
#URLs:#

userCodeUrl: URL to retrieve user information.
codeUrl: URL to fetch the main script code.
OrionLib Library: Loaded to provide a graphical user interface (GUI) and additional functionalities.
#3. Function getUserInfo()#

Retrieves user information (username and key) from the userCodeUrl. This function is used to validate user input and access keys.

#4. Function disableLocalScripts()#

Disables all LocalScripts found in the Workspace. This function iterates through all descendants of the Workspace and sets the Disabled property to true for LocalScripts, preventing their execution.

#5. Function refreshBalls(force)#

Updates the list of detected balls in the Workspace. It checks all objects in the Workspace and adds those with names matching the specified ballNames. It respects the update interval to avoid excessive updates.

#6. Function moveCircleSmoothly(targetPosition)#

Moves the reach circle smoothly to a new position using a Tween. This ensures that the circle moves fluidly and naturally during gameplay.

#7. Function createReachCircle()#

Creates and configures the visual reach circle in the Workspace. It adjusts the size and color of the circle based on player settings and positions it relative to the player.

#8. Function onQuantumInputBegan(input, gameProcessedEvent)#

Handles player input to adjust reach and perform other actions based on key presses. It includes logic for increasing or decreasing reach, adjusting script behavior, and managing interactions with balls.

#9. User Interface#

Key Verification Window: Allows players to enter their username and key for access validation. If the input is correct, the main script is loaded.
Control GUI: After validation, a new window is created to adjust reach settings and customize the appearance of game elements.

#10. Settings and Adjustments#

Reach Adjustment: Players can adjust the reach distance using a slider control.
Color Customization: Allows players to change the color of the reach circle and detected balls.
Ball Ownership and Plag Control: Options to define if the player should own the balls and adjust "plag" behavior (maximum touches allowed before reset).

#11. Notifications#

The script uses notifications to inform players about script status, including successful key validation, errors, and version information.

12. Auto-Destruction

After 10 hours of execution, the script automatically shuts down and disables its functionalities, requiring reinitialization and revalidation.

Additional Information
SPJ Reach is continuously updated to add new features and improve functionality. For more information and updates, join our Discord server: https://discord.gg/eQqHWwMJEa.
