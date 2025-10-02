# 🕹️ The Wumpus World AI Project (Problem)

Welcome to the **Wumpus World** AI adventure! This project implements the classic AI challenge using **Python**, featuring both human gameplay and an intelligent **NEAT-evolved AI agent**. Explore a dangerous grid world, train neural networks, and visualize the evolution of intelligence.  

---

## 🌟 Features

- **🗺️ Wumpus World Game**: 4x4 grid with hidden pits, a deadly Wumpus, and glittering gold.  
- **🤖 AI Agent**: Plays intelligently using **NEAT (NeuroEvolution of Augmenting Topologies)**.  
- **📈 Evolution & Training**: Train agents over generations, evolving better strategies.  
- **🎨 Visualization**: Neural network graphs, fitness curves, and species diversity plots.  
- **⚙️ Configurable**: Modify NEAT parameters, game rules, or world size easily.  
- **💾 Pre-trained Models**: Load `winner_genome.pkl` to see the best AI in action.  

---

## 🗂️ Project Structure

```text
main.py                  # Game launcher (Human, AI, Train)
requirements.txt         # Python dependencies
winner_genome.pkl        # Best trained genome

ai/
  ai_agent.py            # NEAT-based AI agent
  neat_evo_process.py    # NEAT evolution & fitness evaluation
  visualize.py           # Neural network & training visualization
  wumpus_world_ai.py     # Run AI agent in Wumpus World
  config/
    neat_config.txt      # NEAT parameters (mutation rates, population, etc.)

game/
  cell.py                # Cell logic: pit, Wumpus, gold
  game.py                # Game engine, scoring, rules
  instructions.py        # Player instructions & controls
  player.py              # Player state and actions
  wumpus_world.py        # Human player game loop
```

---

## 🎮 Gameplay Overview

Navigate a dark 4x4 cave:

1. **Find the gold** 💰  
2. **Avoid the Wumpus** 👹 and pits 🕳️  
3. **Escape alive** to your starting cell  

### Controls (Human Player)

| Key | Action            |
|-----|------------------|
| w   | Move forward      |
| s   | Move backward     |
| a   | Turn left         |
| d   | Turn right        |
| x   | Shoot arrow       |
| g   | Grab gold         |
| q   | Quit game         |

**Clues**: Breeze near pits 🌬️, stench near Wumpus 💨, glitter near gold ✨. Deduce safely!

---

## 🤖 AI Agent & NEAT

**Algorithm Used**: **NEAT (NeuroEvolution of Augmenting Topologies)**  

- **Inputs**:  
  Breeze, stench, glitter, bump, scream, position, direction, score, moves  
- **Outputs**:  
  Move forward/backward, turn left/right, grab, shoot arrow  
- **Training Process**:  
  - Evolution over **300 generations**  
  - Fitness rewards: survival, gold collection, escape success, exploration  
  - Best genome saved to `winner_genome.pkl`  
- **Performance**:  
  - Agents learn to navigate safely, maximize gold collection, and escape reliably  
  - Fitness improves generation over generation, balancing exploration and risk  

**Play with AI**: Load `winner_genome.pkl` and watch the NEAT agent tackle the Wumpus World!  

---

## 📊 Visualization

- **Neural Network Graphs**: Visualize evolved connections  
- **Fitness & Speciation**: Track progress and diversity  
- **Output Formats**: SVG/PNG for detailed analysis  

---

## ⚙️ Configuration

- Tweak NEAT parameters in `ai/config/neat_config.txt`  
  (population size, mutation rates, activation functions, etc.)  

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7+  
- pip  

### Installation

```bash
git clone https://github.com/mohamadnassiri/The-Wumpus-World-Problem.git
cd The-Wumpus-World-Problem
pip install -r requirements.txt
```

### Run the Game

```bash
python main.py
```

Options:  
1️⃣ Play as human  
2️⃣ Watch AI agent  
3️⃣ Train new AI agent  

---

## 📚 Key Details

- **Modular Engine**: Extendable to larger grids or new rules  
- **Scoring**: Rewards/punishments for all player actions  
- **Instructions**: Accessible in-game  
- **AI Mapping**: Neural net structure and inputs/outputs detailed in `ai/ai_agent.py`  

---

## 📝 License

MIT License  

---

## 🙏 Acknowledgements

- [NEAT-Python](https://github.com/CodeReclaimers/neat-python)  
- Original Wumpus World problem from AI literature  
---

## ✨ Enjoy the adventure! May your gold be plentiful and your Wumpus-free! ✨

