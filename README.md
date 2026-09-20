# Oswald-cctv-camera-placement-simulator
An interactive web-based CCTV camera placement and coverage simulator developed during my internship at Oswald Stack.


# 🎥 CCTV Camera Placement Simulator

An interactive web-based CCTV camera placement, coverage analysis, and building simulation tool developed during my internship at **Oswald Stack**.

The application provides a visual environment for designing building layouts, placing CCTV cameras, configuring their viewing parameters, and analyzing camera coverage through interactive **2D and 3D visualization**.

---

## 📌 Overview

The **CCTV Camera Placement Simulator** is designed to make CCTV planning and camera positioning more visual and interactive.

Instead of planning camera locations only through static floor plans, this simulator provides an interactive environment where users can:

- Design walls and rooms
- Place CCTV cameras
- Configure camera parameters
- Visualize camera fields of view
- Analyze coverage and blind spots
- Switch between 2D and 3D views
- Preview individual camera perspectives
- Use light and night vision preview modes
- Import floor plan images
- Generate editable 3D building layouts
- Enable or disable shadows
- Export the current simulation as an image

The application combines **3D visualization, interactive controls, camera geometry, building layout editing, and coverage analysis** into a single browser-based tool.

---

## ✨ Key Features

### 🎯 Simulation Mode

Simulation Mode provides the main environment for placing and managing CCTV cameras.

Users can:

- Select cameras
- Add cameras
- Delete selected cameras
- Clear all cameras
- Select multiple cameras
- View camera coverage
- Configure camera parameters
- Open camera previews
- Analyze coverage statistics

Camera placement can be performed directly on the floor area.

---

## 🏗️ Build Mode

Build Mode allows users to create and modify the building environment before placing cameras.

### Building Editor

Available tools include:

- 👆 Select
- 📏 Add Wall
- 🏠 Add Room
- 🗑️ Delete
- ✋ Move
- 🪟 Glass Wall

Walls and rooms can be created interactively using click and drag operations.

### Wall Editing

The simulator supports:

- Solid walls
- Glass walls
- Wall selection
- Wall movement
- Wall deletion
- Clear all walls
- Undo
- Redo

### Room Editing

Rooms can be created as complete structures containing:

- Floor
- Four walls

Rooms can also be selected, moved, and deleted.

---

## 📐 Grid Snap

The Build Mode includes a **Grid Snap** option.

When enabled, building elements can be aligned more consistently while designing the layout.

Grid snapping can be enabled or disabled from the Build Mode controls.

---

## 🖼️ Blueprint / Floor Plan Import

The simulator supports importing floor plan images.

Supported formats include:

- PNG
- JPG
- JPEG
- WebP

The uploaded floor plan can be processed to identify building boundaries, walls, and rooms.

The application provides a blueprint processing interface showing detected information before generating the building.

### Blueprint → 3D

The system is designed to process a floor plan image and generate an editable 3D building representation.

The blueprint processing interface displays:

- Detected rooms
- Detected walls
- Estimated area

After processing, the generated structure can be used inside the simulator.

---

## 📷 CCTV Camera Placement

Cameras can be placed directly inside the simulated environment.

Each camera maintains configurable properties such as:

- Camera height
- Pan
- Tilt
- Horizontal FOV
- Vertical FOV
- Detection range
- Camera type

The simulator uses these parameters to visualize the camera's viewing area.

---

## 🔭 Camera Field of View

Each camera displays a visual coverage region representing its field of view.

This allows users to understand:

- Which areas are visible
- Which areas remain uncovered
- How camera orientation affects coverage
- How multiple cameras overlap
- How camera placement affects the overall surveillance layout

---

## 📊 Coverage Analysis

The simulator provides real-time statistics related to the camera layout.

The interface tracks:

- 📷 Total Cameras
- 🟢 Coverage
- 🔴 Blind Spot
- 🔄 Overlap
- 🟣 Selected Cameras
- 🧱 Walls
- 🏠 Rooms

Coverage information is updated as the building and camera configuration changes.

---

## 📺 Camera Preview

The simulator includes an individual camera preview panel.

The preview allows users to inspect the scene from a camera's perspective.

The preview panel supports:

- Camera POV
- Pan
- Tilt
- Scroll zoom
- Light mode
- Night vision mode
- Minimize
- Close
- Resize

This provides a more realistic way to inspect what a selected camera can see.

---

## 🌙 Night Vision Preview

The camera preview supports two visual modes:

### ☀️ Light Mode

Displays the camera view using the normal scene appearance.

### 🌙 Night Vision

Provides a night-vision style visualization for inspecting camera visibility under darker conditions.

The preview mode can be switched directly from the camera preview panel.

---

## 🌐 2D and 3D Visualization

The simulator supports two different viewing modes.

### 📐 2D View

The 2D view provides a top-down representation of the building.

It is useful for:

- Floor-plan inspection
- Camera positioning
- Wall placement
- Room layout
- Coverage analysis

The 2D view also supports panning across the workspace.

### 🌐 3D View

The 3D view provides a perspective representation of the building.

It allows users to:

- Rotate the scene
- Zoom
- Inspect walls and rooms
- Visualize camera positions
- View camera coverage
- Analyze shadows

---

## 💡 Shadow Controls

The 3D environment includes configurable shadow controls.

Users can independently control:

- Room Shadows
- Camera Shadows

Shadows are primarily used in the 3D visualization mode to improve spatial understanding of the simulated environment.

---

## 🌓 Light and Dark Theme

The application includes theme switching.

Users can switch between:

- ☀️ Light Theme
- 🌙 Dark Theme

The interface dynamically updates its colors, panels, controls, viewport, and other visual elements according to the selected theme.

---

## 🔄 Scene Controls

The simulator includes several scene management controls.

### Reset

Resets the main 3D camera view and returns the scene to its default viewing position.

### Export

The current simulation viewport can be exported as a PNG image.

This allows users to save visual snapshots of their CCTV layout.

---

## 🖱️ Interactive Controls

The application is designed around direct manipulation.

Typical interactions include:

| Action | Operation |
|---|---|
| Select Camera | Click a camera |
| Add Camera | Select Add Camera and click the floor |
| Multi-select | Ctrl + Click |
| Rotate 3D View | Drag |
| Zoom | Scroll |
| 2D Pan | Drag empty floor |
| Create Wall | Click + Drag |
| Create Room | Click + Drag |
| Move Wall | Click + Drag |
| Create Glass Wall | Click + Drag |
| Delete | Select and delete |
| Camera Preview | Open preview from camera controls |

---

## 🧱 Building Components

The simulator represents the building environment using different structural components.

### Solid Walls

Solid walls are used to represent normal building boundaries and internal partitions.

### Glass Walls

Glass walls provide a transparent wall representation for layouts where visibility through the wall needs to be represented differently.

### Rooms

Rooms are represented using floors and surrounding walls.

---


<img width="1900" height="862" alt="2D VERSION" src="https://github.com/user-attachments/assets/686f496b-3396-488a-a0b6-6febe82ab3ba" />
<img width="1897" height="856" alt="3D VERSION" src="https://github.com/user-attachments/assets/0d6f86b0-93e2-45a9-b239-b59c3fd59ed5" />

## 🧠 Coverage Visualization

The simulator calculates and visualizes camera coverage based on the camera configuration and environment.

Important parameters include:

```text
Camera Position
Camera Height
Pan
Tilt
Horizontal FOV
Vertical FOV
Detection Range
Building Walls
Room Layout
