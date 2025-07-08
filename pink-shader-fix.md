# 🎨 How to Fix "Pink Materials" in Unity (Shader Graph Issues)

Sometimes, models or prefabs appear **pink** in your scene. This happens when Unity cannot render the material because the required shader or render pipeline setup is missing or misconfigured.

---

## 🛠 Affected Assets
This fix applies to assets like:
- 👻 Animated Ghost Shader
- 🧬 Cyber Shader and Props  
- 🎨 Abstract BG Shader  
- And other Shader Graph–based packs

---

## ✅ Solution 1: Check Your Unity Version

Ensure you're using a Unity version that supports Shader Graph and the correct Render Pipeline.

> ✅ **Recommended Version:**  
> Unity **2021.3.24f1 LTS** (or newer)  
> This asset was tested and submitted using this version.

---

## ✅ Solution 2: Install Shader Graph Package

Sometimes the pink issue happens because Shader Graph is not installed in your project.

**Steps to install Shader Graph:**

1. Go to `Window → Package Manager`
2. In the top-left dropdown, select **Unity Registry**
3. Search for **Shader Graph**
4. Click **Install** (Install version 12.1.11 or newer)

---

## ✅ Solution 3: Add Active Targets to Shader Graph

If the shader still appears pink, you may need to manually configure the **Active Targets** in the Shader Graph.

**Steps:**

1. Open the Shader Graph folder for the asset  
   _(Example: `Assets → [Asset Folder] → Shadergraph`)_

2. Double-click to open each `.shadergraph` file in Unity  
   _(There may be more than one — repeat the steps below for each)_

3. In the **Graph Inspector** window, click **Graph Settings**

4. Under **Active Targets**, click the **`+` button**  
   Add the render pipeline you're using:
   - **URP** – Add URP (Universal Render Pipeline)
   - **Built-in** – Add Built-in Render Pipeline
   - **HDRP** – Add HDRP if you're using it

5. Save the shader and return to the scene — the pink material should be gone.

---

## 💡 Still Pink?

If your issue is not solved by the steps above:

- Try right-clicking the shader file and selecting **Reimport**
- Or right-click the asset folder and select **Reimport All**
- Make sure your **Graphics settings** in `Edit → Project Settings → Graphics` are configured for the correct pipeline

---

## 📧 Need Help?

If you're stuck or the pink issue still appears, contact us at:  
**📩 srstudioskerala@gmail.com**  
Send a screenshot and mention your Unity version + Render Pipeline.

We’re happy to help!
