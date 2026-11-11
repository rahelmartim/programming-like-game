# Programming Like Game

A 2D platformer prototype, made with Unity, in which you control the character with code. You build small programs from visual blocks, for example a `while` loop with a `move` command, and the game runs them on the character.

The project is a learning experiment from 2018. It is a pre-alpha demo with the first tutorial phase.

![The character walks on jungle platforms](Assets/Record_2018_10_19_08_22_04_619.gif)
![The character moves and jumps between platforms](Assets/Record_2018_10_19_08_22_24_276.gif)

## How it works

The game has a block editor. The blocks use Portuguese words:

| Block | Meaning |
| --- | --- |
| `ENQUANTO <condition> FAÇA` | `while <condition> do`: repeats the blocks inside it. |
| `MOVA <speed> <direction>` | `move`: moves the character left, right, up, or down. |
| `DECLARE <variable>` | Declares an `int`, `float`, or `bool` variable. |

The game turns the blocks into a small text language, and an interpreter in C# runs it. Examples:

```text
while(true){move(left, 1)}
while(12 > 1){move(right, 0.2)}
```

Conditions support `>`, `>=`, `<`, `<=`, `==`, `!=`, `&&`, `||`, `true`, and `false`. The bodies of loops can contain moves, variable declarations, and assignments with `+`, `-`, `*`, and `/`.

The level also has a door. When you click its activator, a terminal opens. To open the door, you set the `energia` (energy) variable to `verdadeiro` (true).

![Block editor with a while loop that contains a move block](Assets/title5.png)
![Block editor with while and declare blocks](Assets/title4.png)

## Controls

| Key | Action |
| --- | --- |
| Left and right arrows, or A and D | Walk |
| Space | Jump |
| Mouse click on the door activator | Open the terminal |

## Tech stack

- [Unity](https://unity.com) 2017.3.1f1
- C#
- Pixel art assets: jungle tileset, parallax background, and character

## Getting started

1. Install Unity 2017.3.1f1 with [Unity Hub](https://unity.com/download). A newer Unity version can also open the project, but it upgrades the project files first.
2. Clone the repository.

   ```bash
   git clone https://github.com/rahelmartim/programming-like-game.git
   ```

3. In Unity Hub, select **Add**, and then select the cloned folder.
4. In the `Assets` folder, open the scene `1.unity` or `2.unity`.
5. Select **Play**.

## Project structure

| File | Description |
| --- | --- |
| `Assets/PlattaformTest.cs` | Interpreter: parses the code and runs `while`, `move`, declarations, and assignments. |
| `Assets/player.cs` | Character movement and jump. |
| `Assets/DoorActivator.cs` | Door puzzle and its terminal. |
| `Assets/EstruturarPainell.cs` | Block panel. |
| `Assets/Command.cs`, `Expression.cs`, `Operation.cs`, `Variable.cs`, `WhileForm.cs`, `Argument.cs` | Data structures of the interpreter. |
| `Assets/1.unity`, `Assets/2.unity` | Scenes. |

## Credits

The jungle tileset and the character art are by [@Jsf23Art](https://twitter.com/Jsf23Art), as the watermark in `Assets/mockup.png` shows.
