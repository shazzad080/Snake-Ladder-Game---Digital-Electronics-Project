# 🎲 Snake & Ladder Game - Hardware Edition

 A nostalgic board game brought to life with LEDs, logic circuits, and lots of engineering magic! ✨

## 📚 About This Project

Remember playing Snake & Ladder as a kid? We built a physical electronic version using digital circuits! This isn't just a game—it's a fully functional hardware implementation where LEDs light up to show player positions, snakes actually make you slide down, and ladders help you climb up. Plus, there's a buzzer that goes off when someone wins! 🎉

**Built for:** Digital Electronics Course (EEE 4307)  
**Where:** Islamic University of Technology  
**Department:** Electrical & Electronic Engineering  

## 👨‍💻 The Dream Team

| Student ID | Name |
|------------|------|
| 220021108 | Shazzad Ahmed |
| 220021116 | Faiad Faisal Sarthok |
| 220021123 | Fahim Shifat |
| 220021127 | Ahnaf Sakif |
| 220021130 | Mahib Abtahi |
| 220021151 | Abdullah Jubayer |
| 220021157 | Hasib Ahmed |

## 🎥 See It In Action!

Want to see the magic happen? Check out our demo video!

[![Watch Demo](https://img.shields.io/badge/▶️%20Watch%20Demo%20on%20YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/N2M6XJJVqV4?si=ug31wzvvWqkCk_Sj)

*Video crafted with ❤️ by Shazzad Ahmed Chowdhury (editing, recording & voice-over)*

## 🎮 What Makes This Game Special?

### The Basics
- **16-block LED board** that lights up as you play
- **2 players** competing to reach the finish line
- **Electronic dice** that rolls random numbers (1-3)
- **Automatic snake and ladder detection** - no cheating!
- **Memory system** that remembers where you were
- **Winner alert** with buzzer and LED celebration 🎊

### Cool Features We Added
1. **🎯 Must Start with 1** - Just like the real game! You need to roll a 1 to begin
2. **⚡ One-Switch Wonder** - Single button press rolls the dice AND switches players
3. **🎪 Exact Win Required** - Need to land exactly on 15 to win (no overshooting!)
4. **🪜 Ladder Gets Priority** - If a snake and ladder share the same spot, ladder wins
5. **🛡️ Smart Boundaries** - The game won't let you place impossible snakes or ladders

## 🎨 How the LED Board Works

Imagine a glowing game board with 64 LEDs arranged in 16 blocks:

- 🔴 **Red LED** = Player 1's current position
- 🔵 **Blue LED** = Player 2's current position  
- 🟢 **Green LEDs** = Ladder start and end points
- 🟡 **Yellow LEDs** = Snake head and tail

As you play, the LEDs dance around showing exactly what's happening in the game!

## 🔧 Under The Hood - The Brain Modules

Don't worry if you're not an engineer—here's what each part does in simple terms:

### 1. 🎲 Dice Module
The "random number generator" that uses a 555 timer chip to create unpredictable rolls. Press the button and watch the 7-segment display cycle through numbers until it lands on your fate!

### 2. 👥 Player Switcher
A smart flip-flop circuit that automatically knows whose turn it is. No arguments about "It's my turn!"

### 3. 📍 Position Trackers
These decoder circuits are like GPS for your game pieces—they always know where both players are on the board.

### 4. 🐍 Snake Detector
Calculates where the snake's head is and where its tail ends. If you land on a snake head... down you go!

### 5. 🪜 Ladder Detector  
Finds ladder positions and helps you climb up when you land on one. Good luck!

### 6. 🧠 Game Logic Brain
The smartest part! It takes your dice roll, checks for snakes and ladders, and figures out your new position. It even handles all those special rules we added.

### 7. 💾 Memory Bank
Uses shift registers to remember where you were when it's the other player's turn. No more "wait, where was I?"

### 8. 🏆 Winner Detector
Constantly checking if anyone reached position 15. When someone wins, BEEP BEEP! 🎺

### 9. 🔄 Reset Button
Fresh start! Clears everything and lets you play again.

## 🎯 How to Play

1. **Power it up** - Watch all the LEDs do a little dance
2. **Press reset** - Start with a clean slate
3. **Roll the dice** - Keep rolling until you get a 1
4. **Game on!** - Take turns rolling and moving
5. **Watch for snakes and ladders** - They'll trigger automatically
6. **First to 15 wins!** - But you need to roll the exact number

## 🔌 Tech Specs (For The Curious)

- **Board Size:** 16 positions (like a 4×4 grid)
- **Total LEDs:** 64 (4 per block)
- **Dice Range:** 1, 2, or 3
- **Main ICs Used:** 74154 decoders, 7483 adders, 555 timer, various flip-flops
- **Power:** Standard TTL voltage levels
- **PCB Sizes:** Optimized for each module (largest is 180×100mm)

## 🛠️ Building Your Own

Want to recreate this? Here's the journey:

1. **Get the PCB files** - All design files are in this repo
2. **Order the boards** - Send the files to a PCB manufacturer
3. **Buy components** - Check the schematics for the parts list
4. **Solder time!** - Carefully assemble each module
5. **Test individually** - Make sure each part works before connecting
6. **Connect everything** - Follow our integration guide
7. **Play and enjoy!** - You earned it! 🎮

## 📐 PCB Design Highlights

We didn't just slap components on a board—we optimized everything:

- Careful trace routing to avoid interference
- Proper clearances for easy soldering
- Through-hole vias for reliability  
- Common anode design for LED efficiency
- Noise reduction with parallel capacitors
- Clean power distribution

## 📦 What's In This Repository

Everything you need to understand or recreate the project:
- 📄 Complete PCB design files (Proteus format)
- 📋 Full project documentation (PDF)
- 🖼️ Schematic diagrams for all modules
- 🎨 3D PCB visualizations

## 💡 Design Philosophy

We followed three principles:
1. **Make it work** - Functionality first
2. **Make it reliable** - Proper engineering practices
3. **Make it fun** - Because games should be enjoyable!

## 🎓 What We Learned

This project taught us way more than just circuits:
- Digital logic design in the real world
- PCB layout and manufacturing
- Team collaboration and task distribution
- Problem-solving when things don't work the first time (or the fifth time!)
- The satisfaction of seeing LEDs light up exactly as planned

## 🤝 Contributions Breakdown

### Hardware Design
- **Shazzad Ahmed** - Memory Module, New DEMUX IC, Snake & Ladder Logic Module
- **Fahim Shifat** - Snake & Ladder position decoders, Ladder PCB
- **Ahnaf Sakif** - Player position decoder, Dice Module and PCB  
- **Abdullah Jubayer** - Board module design, boundary condition handling
- **Mahib Abtahi** - Snake position PCB
- **Faiad Faisal Sarthok** - Player position decoder PCB

### Integration & Testing
- **Shazzad Ahmed** - Problem analysis, Testing, Memory/Snake & Ladder Logic PCB, Efficiency optimization
- **Ahnaf Sakif** - Complete system integration
- **Mahib Abtahi** - Reset/Winning PCB

### Documentation & Media
- **Shazzad Ahmed, Mahib Abtahi, Ahnaf Sakif, Hasib Ahmed** - Project documentation
- **Shazzad Ahmed** - Video production (editing, recording, voice-over)

## 🐛 Known Quirks

- The dice only rolls 1-3 (we designed it that way for faster games!)
- You need to roll exactly the right number to win (feature, not a bug!)
- Reset button must be held momentarily to properly clear memory

## 🚀 Future Ideas

Imagine if we added:
- More blocks (32 or 64 squares!)
- Sound effects for snakes and ladders
- Score tracking across multiple games
- Wireless controllers
- RGB LEDs for extra flair

## 📧 Get In Touch

Questions? Suggestions? Want to collaborate?  
Reach out through Islamic University of Technology channels.

## 📜 License

This is an academic project created for educational purposes at Islamic University of Technology.

---

<div align="center">

**Project Status:** ✅ Completed & Fully Functional

**Semester:** 2024

Made with 🔧 💡 and ☕ by Team EEE 4307

*"Because every engineer needs to build a game at least once!"*

</div>
