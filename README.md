The-Community_Cut

# 🎬 AI Audiovisual Framework: Night of the Living Dead

Welcome to the film set! This repository organizes prompts, workflows, and AI audiovisual resources for using **LTX-2** to reanimate classic scenes in any visual style you prefer.

Photorealistic, abstract, surreal, hand-painted, or our main focus: **retro 1-bit Pixel Art (Game Boy Noir style)**. The interpretation is up to you.

Use **ComfyUI**, the **open-source LTX-2 model**, or the **LTX Studio API**. As long as it works with **LTX-2**, you’re in!

---

# 📁 Studio Structure (Repository)

To keep production organized, the project is divided into the following departments:

**📁 technical_scripts/**  
Production breakdowns. Here you’ll find detailed frame-by-frame documents (timings, actions, cuts) to replicate the exact timing of each shot.

**📁 comfyui_workflows/**  
The brain of the operation. `.json` files ready to drag and drop into ComfyUI, including advanced **multi-prompt workflows** and **guide image anchoring** (LTXVAddGuide).

**📁 prompts_and_texts/**  
The script department. A collection of **positive prompts** and our **negative prompt shields** (specifically designed to block smoothing and protect the 1-bit aesthetic).

**📁 visual_resources/**  
The editing room. Contains frames extracted from the generations (**pixelart_clip_frames**) ready to be assembled, along with additional graphic assets such as **arcade machine frames**.

---

# 🚀 How to Start Filming

1. Clone or download this repository to your computer.  
2. Open **ComfyUI** and drag the master file from `02_comfyui_workflows/` into your workspace.  
3. Load the original video and adjust **`frame_load_cap`** and **`skip_first_frames`** according to the detailed instructions in `01_technical_scripts/`.  
4. Copy the **Prompts (Positive and Negative)** from the `03_prompts_and_texts/` folder to ensure maximum sharpness.  
5. Shout **“Action!”** (Queue Prompt)!

---

# 🛠️ System Requirements (Custom Nodes)

For the workflows in `02_comfyui_workflows/` to run without errors (red nodes), you must install the following packages via **ComfyUI-Manager**:

| Node / Package | Use in This Project |
|---|---|
| **ComfyUI-VideoHelperSuite** | Loading the original video, FPS control (`force_rate`), and saving results |
| **ComfyUI-LTXTricks** | LTX-2 implementation, guide nodes (`LTXVAddGuide`), and tiled decoding |
| **ComfyUI-Essentials** | Image operations such as `nearest-exact` scaling and center cropping |
| **ComfyUI-Audio** | Precise trimming and synchronization of scene audio (Shot 1 and Shot 2) |
| **ComfyUI-Custom-Scripts** | Interface improvements and KSampler node organization |

**Director’s Note:**  
If nodes are missing when loading the workflow, use **“Install Missing Custom Nodes”** in your Manager and search for the names listed in the table above.
